---
description: Execute implementation tasks for a specific agent type (api, server, or client)
scripts:
  sh: scripts/bash/check-prerequisites.sh --json --include-tasks
  ps: scripts/powershell/check-prerequisites.ps1 -Json -IncludeTasks
---

## User Input

```text
$ARGUMENTS
```

## Agent Type Selection

**REQUIRED**: You must specify exactly ONE agent type:

| Argument | Task File | Agent | Description |
|----------|-----------|-------|-------------|
| `api` | `tasks-api.md` | api-agent | Setup + API contracts |
| `server` | `tasks-server.md` | server-agent | Backend TDD implementation |
| `client` | `tasks-client.md` | client-agent | Frontend integration tests first |

**Examples**:
- `/speckit.implement api` → Execute API tasks
- `/speckit.implement server` → Execute Server tasks
- `/speckit.implement client` → Execute Client tasks

**INVALID** (do nothing and explain):
- `/speckit.implement` → No agent specified
- `/speckit.implement both` → Cannot run multiple agents
- `/speckit.implement server client` → Cannot run multiple agents
- `/speckit.implement all` → Cannot run multiple agents

## Outline

### Step 1: Validate Arguments

Parse `$ARGUMENTS` and validate:

1. **Extract agent type** from arguments (case-insensitive: "api", "server", "client")
2. **If no agent type specified**: Output error message and stop
   ```
   Error: Agent type required.

   Usage: /speckit.implement <api|server|client>

   Expected workflow:
   1. /speckit.implement api     → First (required)
   2. /speckit.implement server  → After API complete
   3. /speckit.implement client  → After API complete (can run parallel with server)
   ```
3. **If multiple agents specified**: Output error message and stop
   ```
   Error: Only one agent type allowed per session.

   To enable parallel work:
   - Session 1: /speckit.implement server
   - Session 2: /speckit.implement client

   These can run in separate terminals simultaneously.
   ```

### Step 2: Initialize and Parse Context

1. Run `{SCRIPT}` from repo root and parse FEATURE_DIR and AVAILABLE_DOCS list. All paths must be absolute.

2. **Determine task file based on agent type**:
   - `api` → `FEATURE_DIR/tasks-api.md`
   - `server` → `FEATURE_DIR/tasks-server.md`
   - `client` → `FEATURE_DIR/tasks-client.md`

3. **Verify task file exists**:
   - If not found: "Error: [task file] not found. Run /speckit.tasks first."

4. **Load implementation context**:
   - **REQUIRED**: Read the task file for this agent
   - **REQUIRED**: Read plan.md for tech stack, build commands, and subagent context
   - **IF EXISTS**: Read data-model.md for entities and relationships
   - **IF EXISTS**: Read contracts/ for API specifications

### Step 3: Check Prerequisites (for server/client only)

**For `server` or `client` agent types only**:

⚠️ **HARD GATE: ALL API Tasks Must Be Complete**

The API phase defines contracts for **ALL user stories** in the spec. This is not incremental - you cannot implement US1 client while US2 API is still pending.

1. **Verify `tasks-api.md` exists** and **EVERY task is complete** (marked with `[X]`)
2. **Scan for ANY incomplete tasks**:
   - If even ONE task has `- [ ]` (unchecked), BLOCK execution
   - This includes setup tasks, contracts for US1, US2, US3, etc., and type generation
3. If ANY API tasks are incomplete:
   ```
   ═══════════════════════════════════════════════════════════════════════════════
   ERROR: Cannot start [server/client] implementation
   ═══════════════════════════════════════════════════════════════════════════════

   ALL API tasks must be complete before ANY client or server work can begin.
   This includes contracts for ALL user stories in the spec.

   Incomplete API tasks found:
   - [ ] T010 [US1] Define User endpoints in contracts/api.yaml
   - [ ] T050 [US2] Define Order endpoints in contracts/api.yaml
   - [ ] T080 Generate TypeScript types from contracts

   Run: /speckit.implement api

   Note: The API phase must define contracts for EVERY user story before
   implementation can begin. This ensures Client and Server have complete
   type definitions to work against.
   ═══════════════════════════════════════════════════════════════════════════════
   ```

4. Verify `contracts/` directory exists with API schemas for all endpoints
5. Verify `shared/types/` directory exists with generated types

### Step 4: Verify Checklists (Optional)

If `FEATURE_DIR/checklists/` exists:

```bash
claude --print "Verify all checklists in FEATURE_DIR/checklists/ and report status" \
       --system-prompt "$(cat .specify/agents/checklist-agent.md)" \
       --allowedTools "Read,Glob,Grep"
```

**If any checklist is incomplete**:
- Display the status table
- **ASK**: "Some checklists are incomplete. Do you want to proceed anyway? (yes/no)"
- If "no", halt execution

### Step 5: Execute Tasks (Chunked Subagent Pattern)

**⚠️ IMPORTANT**: To preserve context and enable incremental progress, tasks are executed in CHUNKS using subagents.

**Chunking Rules**:
- Group tasks by User Story (US1, US2, US3...)
- Within each story, create chunks of **maximum 5 tasks**
- Spawn ONE subagent per chunk
- Mark tasks complete after EACH chunk before continuing
- Use **30 minute timeout** for each subagent (tasks can take time)

#### Step 5.1: Parse and Chunk Tasks

1. **Read the task file** and extract all incomplete tasks (lines with `- [ ]`)
2. **Group by User Story**: Tasks with `[US1]`, `[US2]`, etc.
   - Tasks without a story marker go in a "Setup" group
3. **Chunk each group** into batches of max 5 tasks

**Example chunking**:
```
Setup tasks (no [US#]):     [T001, T002, T003] → Chunk 1 (3 tasks)
US1 tasks (12 total):       [T010-T014] → Chunk 2, [T015-T019] → Chunk 3, [T020-T021] → Chunk 4
US2 tasks (8 total):        [T030-T034] → Chunk 5, [T035-T037] → Chunk 6
```

#### Step 5.2: Execute Each Chunk

For EACH chunk, follow this pattern:

**A. Announce the chunk**:
```
═══════════════════════════════════════════════════════════════════════════════
CHUNK [N] of [TOTAL]: [Story Name] ([X] tasks)
Tasks: T001, T002, T003, T004, T005
═══════════════════════════════════════════════════════════════════════════════
```

**B. Write the prompt to a temp file** (avoids shell escaping issues):

Use the Write tool to create `.specify/tmp/[agent-type]-prompt.txt` (e.g., `api-prompt.txt`, `server-prompt.txt`, `client-prompt.txt`) with:
```
You are executing a chunk of [AGENT_TYPE] tasks.

Context from plan.md:
- [Include relevant context for this agent type]

Tasks to execute (THIS CHUNK ONLY):
- [ ] T001 [Description from task file]
- [ ] T002 [Description from task file]
- [ ] T003 [Description from task file]
- [ ] T004 [Description from task file]
- [ ] T005 [Description from task file]

Instructions:
1. Execute each task in order
2. Verify each task is complete before moving to next
3. Run build/test commands after implementation tasks

After completing ALL tasks in this chunk, output this JSON:
```json
{
  "agent": "[api|server|client]",
  "chunk": [N],
  "completed": ["T001", "T002", "T003", "T004", "T005"],
  "failed": [],
  "build": "PASS",
  "tests": "PASS",
  "notes": "Any issues or observations"
}
```
```

**C. Spawn subagent with extended timeout**:

Use the **Bash tool** with **timeout: 1800000** (30 minutes):
```bash
claude --print "$(cat .specify/tmp/[agent-type]-prompt.txt)" \
       --system-prompt "$(cat .specify/agents/[agent-type]-agent.md)" \
       --allowedTools "Read,Write,Edit,Bash,Glob,Grep"
```

**Example for client agent**:
```bash
claude --print "$(cat .specify/tmp/client-prompt.txt)" \
       --system-prompt "$(cat .specify/agents/client-agent.md)" \
       --allowedTools "Read,Write,Edit,Bash,Glob,Grep"
```

**D. Parse JSON and mark tasks complete** (see Step 6)

**E. Continue to next chunk** - Repeat B-D for each chunk

#### Agent-Specific Context

Include this context in the prompt based on agent type:

**For API Agent**:
```
Context from plan.md:
- Contract Location: [from plan.md API Subagent Context]
- Type Output: [from plan.md]
- Validation Command: [from plan.md]

Pattern: Define schemas → Generate types → Create examples
Constraint: No business logic, schema definitions only
```

**For Server Agent**:
```
Context from plan.md:
- Source Location: [from plan.md Server Subagent Context]
- Test Location: [from plan.md]
- Build Command: [from plan.md]
- Test Command: [from plan.md]

Pattern: Red (failing test) → Green (minimal code) → Refactor
Constraint: Tests MUST fail first, then implement to pass
```

**For Client Agent**:
```
Context from plan.md:
- Source Location: [from plan.md Client Subagent Context]
- Test Location: [from plan.md]
- Mock Location: [from plan.md]
- Build Command: [from plan.md]
- Test Command: [from plan.md]

Pattern: Create mock HTTP responses → Write failing integration test → Implement client code
Constraint: ONLY mock at HTTP boundary (no internal service mocks)
Use common-ui components from .specify/common-ui.md
```

### Step 6: Update Task File (After EACH Chunk)

**⚠️ CRITICAL**: After EACH subagent chunk completes, YOU (the orchestrator) MUST mark tasks as complete BEFORE starting the next chunk.

This ensures:
- Incremental progress is saved
- If something fails, completed work is preserved
- You can see progress in the task file

1. **Capture the subagent output** - The Bash tool returns the subagent's output including the JSON report

2. **Find the JSON completion report** in the output - Look for:
   ```json
   {
     "agent": "api",
     "chunk": 1,
     "completed": ["T001", "T002", "T003"],
     ...
   }
   ```

3. **Use the Edit tool to mark each completed task** in the task file:

   For EACH task ID in the `completed` array, use the Edit tool:
   ```
   Edit task file:
   - old_string: "- [ ] T001"
   - new_string: "- [X] T001"
   ```

   **Example**: If subagent reports `"completed": ["T001", "T002", "T003"]`, make 3 Edit calls:
   - Edit: `- [ ] T001` → `- [X] T001`
   - Edit: `- [ ] T002` → `- [X] T002`
   - Edit: `- [ ] T003` → `- [X] T003`

4. **For failed tasks**: Leave as `- [ ]` but add a note below the task line

5. **Report chunk completion**:
   ```
   ✓ Chunk [N] complete: [X] tasks done, [Y] failed
   ```

6. **Continue to next chunk** - Go back to Step 5.2 for the next chunk

**DO NOT** skip this step. The task file must reflect completed work after EACH chunk.

### Step 7: Final Report (After ALL Chunks Complete)

After all chunks have been processed, generate final completion report:

```
═══════════════════════════════════════════════════════════════════════════════
IMPLEMENTATION COMPLETE: [AGENT TYPE]
═══════════════════════════════════════════════════════════════════════════════

Feature: [FEATURE_NAME]
Agent: [api|server|client]
Task File: [path to task file]

Chunks Processed: [N] chunks
Tasks Completed: [X] of [Y] total
Tasks Failed: [list if any]

Build Status: [PASS/FAIL/N/A]
Test Status: [PASS/FAIL/N/A]

Chunk Summary:
  ✓ Chunk 1 (Setup): 3 tasks
  ✓ Chunk 2 (US1): 5 tasks
  ✓ Chunk 3 (US1): 5 tasks
  ✓ Chunk 4 (US2): 4 tasks
  ...

═══════════════════════════════════════════════════════════════════════════════

Next Steps:
[Suggest next action based on agent type]

For API: "Run /speckit.validate server to verify server environment"
For Server: "Server implementation complete. Run /speckit.validate server"
For Client: "Client implementation complete. Run /speckit.validate client"
═══════════════════════════════════════════════════════════════════════════════
```

---

## Execution Order Reference

The expected workflow is:

```
┌─────────────────────────────────────────────────────────────────┐
│ 1. /speckit.implement api                                       │
│                                                                 │
│    ⚠️  MUST define contracts for ALL user stories:              │
│    - Setup tasks (project structure, tooling)                   │
│    - US1 contracts (endpoints, schemas)                         │
│    - US2 contracts (endpoints, schemas)                         │
│    - US3 contracts (endpoints, schemas)                         │
│    - ... ALL stories in spec.md ...                             │
│    - Type generation (shared/types/)                            │
│                                                                 │
│    This is a HARD GATE - no partial completion allowed          │
└─────────────────────────────────────────────────────────────────┘
                              │
                              ▼
┌─────────────────────────────────────────────────────────────────┐
│ 2. /speckit.validate server                                     │
│    └── Verify server can build with generated types             │
└─────────────────────────────────────────────────────────────────┘
                              │
              ┌───────────────┴───────────────┐
              ▼                               ▼
┌──────────────────────────┐    ┌──────────────────────────┐
│ 3a. /speckit.implement   │    │ 3b. /speckit.implement   │
│     server               │    │     client               │
│                          │    │                          │
│ [Can run in parallel     │    │ [Can run in parallel     │
│  in separate session]    │    │  in separate session]    │
│                          │    │                          │
│ Implements ALL stories   │    │ Implements ALL stories   │
│ using pre-defined types  │    │ using pre-defined types  │
└──────────────────────────┘    └──────────────────────────┘
              │                               │
              ▼                               ▼
┌──────────────────────────┐    ┌──────────────────────────┐
│ 4a. /speckit.validate    │    │ 4b. /speckit.validate    │
│     server               │    │     client               │
└──────────────────────────┘    └──────────────────────────┘
```

**Why ALL API tasks first?**
- Types must exist for all endpoints before any implementation
- Client and Server need complete contracts to avoid rework
- Prevents partial implementations that don't integrate

---

## Available Subagents

| Agent | File | Purpose |
|-------|------|---------|
| api-agent | .specify/agents/api-agent.md | API contracts, type generation |
| client-agent | .specify/agents/client-agent.md | Frontend, integration tests |
| server-agent | .specify/agents/server-agent.md | Backend, TDD unit tests |
| checklist-agent | .specify/agents/checklist-agent.md | Verify checklists |

---

## Notes

- Each session handles exactly ONE agent type
- Server and Client can run in parallel (separate sessions/terminals)
- API must complete before Server/Client can start
- This design prevents race conditions on task files
- Use `/speckit.validate` to run environment validation after implementation

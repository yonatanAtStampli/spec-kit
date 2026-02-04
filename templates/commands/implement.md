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

### Step 6: Process Results and Resolve Failures (Autonomous Retry Loop)

**⚠️ CRITICAL**: After EACH subagent completes, process results and resolve failures BEFORE moving to next chunk. The orchestrator should work through problems autonomously, only asking the user when truly stuck.

#### 6.1: Parse Subagent Output

1. **Capture the subagent output** - The Bash tool returns output including the JSON report

2. **Find the JSON completion report**:
   ```json
   {
     "agent": "api",
     "chunk": 1,
     "completed": ["T001", "T002", "T003"],
     "failed": ["T004"],
     "notes": "T004 failed due to missing dependency..."
   }
   ```

3. **Mark completed tasks** using the Edit tool:
   - For EACH task ID in `completed` array: `- [ ] T001` → `- [X] T001`

#### 6.2: Autonomous Failure Resolution

**If there are failed tasks**, enter the retry loop. Do NOT ask the user unless you reach a dead-end.

**Track retry state**:
- `failed_tasks`: List of task IDs that failed
- `retry_count`: Number of retry attempts for current chunk (max 3)
- `last_failed_count`: Number of failed tasks before this attempt

**Retry Loop** (repeat until resolved or dead-end):

1. **Analyze failure type** from subagent `notes`:

   **Environment-related failures**:
   - Build/compilation errors
   - Missing dependencies or packages
   - Type errors from contracts
   - Module not found
   - Port conflicts
   - Process startup failures

   **Implementation failures**:
   - Logic errors
   - Test assertion failures
   - Missing function implementations

2. **If environment-related**, run environment validation first:

   ```
   ═══════════════════════════════════════════════════════════════════════════════
   ENVIRONMENT ISSUE DETECTED - Attempting automatic fix
   Issue: [from notes]
   ═══════════════════════════════════════════════════════════════════════════════
   ```

   a. Write prompt to `.specify/tmp/validate-[target]-prompt.txt`:
      - For `api` or `server` agent → `validate-server-prompt.txt`
      - For `client` agent → `validate-client-prompt.txt`

   b. Spawn environment validation agent (Bash tool, timeout: 1800000):
   ```bash
   claude --print "$(cat .specify/tmp/validate-[target]-prompt.txt)" \
          --system-prompt "$(cat .specify/agents/environment-validation-agent.md)" \
          --allowedTools "Read,Write,Edit,Bash,Glob,Grep"
   ```

3. **Retry failed tasks** with implementation subagent:

   ```
   ═══════════════════════════════════════════════════════════════════════════════
   RETRYING FAILED TASKS (Attempt [retry_count]/3)
   Tasks: [list failed task IDs]
   ═══════════════════════════════════════════════════════════════════════════════
   ```

   a. Write retry prompt to `.specify/tmp/[agent-type]-prompt.txt` with ONLY the failed tasks
   b. Spawn implementation subagent (same as Step 5.2 C)
   c. Parse results, mark any newly completed tasks
   d. Update `failed_tasks` list

4. **Check for progress**:
   - If `failed_tasks` is empty → **SUCCESS**, continue to next chunk
   - If fewer tasks failed than `last_failed_count` → **PROGRESS**, continue retry loop
   - If same tasks keep failing after 3 attempts → **DEAD-END**, see below

5. **Check for dependency issues**:
   - If failure notes mention "requires X which is in later task" or similar
   - If task depends on code/types not yet implemented
   → **Note the dependency**, continue to next chunk (will resolve later)

#### 6.3: Dead-End Handling (Only Time to Ask User)

A dead-end is reached when:
- Same tasks fail 3 times with no progress
- Environment validation failed AND retry failed
- Subagent explicitly reports "cannot proceed without user input"

**Only then**, ask the user:
```
═══════════════════════════════════════════════════════════════════════════════
STUCK: Unable to resolve [N] failed tasks after [retry_count] attempts
═══════════════════════════════════════════════════════════════════════════════

Failed tasks:
- [ ] T004: [description] - Error: [error message]

Attempted fixes:
1. [list what was tried]

Options:
1. Skip these tasks and continue to next chunk
2. Stop implementation (go to final report)
3. Provide guidance (describe what to try)
═══════════════════════════════════════════════════════════════════════════════
```

#### 6.4: Report and Continue

After chunk is resolved (or user chooses to skip):

```
✓ Chunk [N] complete: [X] tasks done, [Y] skipped/failed
```

**Continue to next chunk** - Go back to Step 5.2 for the next chunk.

**DO NOT** skip this step. Work through problems autonomously before moving on.

### Step 7: Final Report (After ALL Chunks Complete or User Stops)

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

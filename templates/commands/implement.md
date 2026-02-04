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

### Step 5: Execute Tasks

**⚠️ IMPORTANT**: You MUST spawn subagents using the Bash tool to run `claude` CLI commands. Do NOT execute the tasks yourself directly - delegate to the specialized subagent.

Based on agent type, spawn the appropriate subagent:

#### For API Agent

1. **Execute [SHARED] setup tasks** directly (these are simple setup, no subagent needed)

2. **SPAWN API SUBAGENT** - You MUST use the Bash tool to run this command:

   First, output this message to indicate subagent spawning:
   ```
   ═══════════════════════════════════════════════════════════════════════════════
   SPAWNING API SUBAGENT
   ═══════════════════════════════════════════════════════════════════════════════
   ```

   Then use the **Bash tool** to execute:
   ```bash
   claude --print "Execute these API tasks:

   Context from plan.md:
   - Contract Location: [from plan.md API Subagent Context]
   - Type Output: [from plan.md]
   - Validation Command: [from plan.md]

   Tasks to execute:
   [formatted list of API tasks from tasks-api.md]

   After completing all tasks, output this JSON report:
   \`\`\`json
   {
     \"agent\": \"api\",
     \"completed\": [\"T010\", \"T011\", \"T012\"],
     \"failed\": [],
     \"validation\": \"PASS\",
     \"notes\": \"Any relevant notes\"
   }
   \`\`\`" \
          --system-prompt "$(cat .specify/agents/api-agent.md)" \
          --allowedTools "Read,Write,Edit,Bash,Glob,Grep"
   ```

   **DO NOT** skip the Bash tool call. The subagent handles the actual implementation work.

3. **Parse JSON report** from subagent output and update tasks-api.md

#### For Server Agent

**SPAWN SERVER SUBAGENT** - You MUST use the Bash tool to run this command:

First, output this message:
```
═══════════════════════════════════════════════════════════════════════════════
SPAWNING SERVER SUBAGENT
═══════════════════════════════════════════════════════════════════════════════
```

Then use the **Bash tool** to execute:
```bash
claude --print "Execute these Server tasks:

Context from plan.md:
- Source Location: [from plan.md Server Subagent Context]
- Test Location: [from plan.md]
- Build Command: [from plan.md]
- Test Command: [from plan.md]

Pattern: Red (failing test) → Green (minimal code) → Refactor
Constraint: Tests MUST fail first, then implement to pass

Tasks to execute:
[formatted list of tasks from tasks-server.md]

After completing all tasks, output this JSON report:
\`\`\`json
{
  \"agent\": \"server\",
  \"completed\": [\"T600\", \"T601\", \"T602\"],
  \"failed\": [],
  \"build\": \"PASS\",
  \"tests\": \"PASS\",
  \"notes\": \"Any relevant notes\"
}
\`\`\`" \
       --system-prompt "$(cat .specify/agents/server-agent.md)" \
       --allowedTools "Read,Write,Edit,Bash,Glob,Grep"
```

**DO NOT** skip the Bash tool call. The subagent handles the actual implementation work.

#### For Client Agent

**SPAWN CLIENT SUBAGENT** - You MUST use the Bash tool to run this command:

First, output this message:
```
═══════════════════════════════════════════════════════════════════════════════
SPAWNING CLIENT SUBAGENT
═══════════════════════════════════════════════════════════════════════════════
```

Then use the **Bash tool** to execute:
```bash
claude --print "Execute these Client tasks:

Context from plan.md:
- Source Location: [from plan.md Client Subagent Context]
- Test Location: [from plan.md]
- Mock Location: [from plan.md]
- Build Command: [from plan.md]
- Test Command: [from plan.md]

Pattern: Create mock HTTP responses → Write failing integration test → Implement client code
Constraint: ONLY mock at HTTP boundary (no internal service mocks)

Tasks to execute:
[formatted list of tasks from tasks-client.md]

After completing all tasks, output this JSON report:
\`\`\`json
{
  \"agent\": \"client\",
  \"completed\": [\"T300\", \"T301\", \"T302\"],
  \"failed\": [],
  \"build\": \"PASS\",
  \"tests\": \"PASS\",
  \"common_ui_components_used\": [\"TextField\", \"Button\", \"Form\"],
  \"notes\": \"Any relevant notes\"
}
\`\`\`" \
       --system-prompt "$(cat .specify/agents/client-agent.md)" \
       --allowedTools "Read,Write,Edit,Bash,Glob,Grep"
```

**DO NOT** skip the Bash tool call. The subagent handles the actual implementation work.

### Step 6: Update Task File

**⚠️ CRITICAL**: After the subagent completes, YOU (the orchestrator) MUST mark tasks as complete.

1. **Capture the subagent output** - The Bash tool returns the subagent's output including the JSON report

2. **Find the JSON completion report** in the output - Look for:
   ```json
   {
     "agent": "api",
     "completed": ["T001", "T010", "T011"],
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

   **Example**: If subagent reports `"completed": ["T001", "T010", "T020"]`, you must make 3 Edit calls:
   - Edit: `- [ ] T001` → `- [X] T001`
   - Edit: `- [ ] T010` → `- [X] T010`
   - Edit: `- [ ] T020` → `- [X] T020`

4. **For failed tasks**: Leave as `- [ ]` but add a note below the task line

**DO NOT** skip this step. The task file must reflect completed work.

### Step 7: Final Report

Generate completion report:

```
═══════════════════════════════════════════════════════════════════════════════
IMPLEMENTATION COMPLETE: [AGENT TYPE]
═══════════════════════════════════════════════════════════════════════════════

Feature: [FEATURE_NAME]
Agent: [api|server|client]
Task File: [path to task file]

Tasks Completed: [X] of [Y]
Tasks Failed: [list if any]

Build Status: [PASS/FAIL/N/A]
Test Status: [PASS/FAIL/N/A]

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

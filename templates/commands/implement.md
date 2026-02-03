---
description: Orchestrator that coordinates specialized subagents to execute the implementation plan
scripts:
  sh: scripts/bash/check-prerequisites.sh --json --require-tasks --include-tasks
  ps: scripts/powershell/check-prerequisites.ps1 -Json -RequireTasks -IncludeTasks
---

## User Input

```text
$ARGUMENTS
```

You **MUST** consider the user input before proceeding (if not empty).

## Orchestrator Overview

This command acts as an **orchestrator** that coordinates specialized subagents to implement the feature. The orchestrator:

1. Parses tasks.md and groups tasks by component marker ([API], [CLI], [SRV], [SHARED])
2. Executes [SHARED] tasks directly
3. Spawns subagents via Claude CLI for specialized work
4. Enforces the API-first execution order
5. Runs Client and Server subagents in parallel per user story

## Outline

### Step 1: Initialize and Parse Context

1. Run `{SCRIPT}` from repo root and parse FEATURE_DIR and AVAILABLE_DOCS list. All paths must be absolute.

2. **Load implementation context**:
   - **REQUIRED**: Read tasks.md for the complete task list with component markers
   - **REQUIRED**: Read plan.md for tech stack, build commands, and subagent context
   - **IF EXISTS**: Read data-model.md for entities and relationships
   - **IF EXISTS**: Read contracts/ for API specifications

### Step 2: Verify Checklists (Spawn Checklist Subagent)

If `FEATURE_DIR/checklists/` exists:

```bash
claude --print "Verify all checklists in FEATURE_DIR/checklists/ and report status" \
       --system-prompt "$(cat .specify/agents/checklist-agent.md)" \
       --allowedTools "Read,Glob,Grep"
```

**Checklist Subagent Returns**:
- Status table with PASS/FAIL per checklist
- Overall status: PASS (all complete) or FAIL (some incomplete)

**If any checklist is incomplete**:
- Display the status table
- **ASK**: "Some checklists are incomplete. Do you want to proceed with implementation anyway? (yes/no)"
- If user says "no", halt execution
- If user says "yes", proceed to Step 3

**If all checklists pass or no checklists exist**: Proceed to Step 3

### Step 3: Parse Tasks by Component

Parse tasks.md and group tasks into:

```
SHARED_SETUP_TASKS    = tasks with [SHARED] in Setup phase
API_TASKS             = tasks with [API] marker
CLI_TASKS_BY_STORY    = tasks with [CLI] marker, grouped by [US#]
SRV_TASKS_BY_STORY    = tasks with [SRV] marker, grouped by [US#]
SHARED_POLISH_TASKS   = tasks with [SHARED] in Polish phase
```

Extract user stories in priority order (P1, P2, P3...) from task organization.

### Step 4: Execute [SHARED] Setup Tasks

Execute setup tasks **directly** (no subagent needed):

For each task in SHARED_SETUP_TASKS:
1. Execute the task
2. Mark task as complete [X] in tasks.md
3. Report progress

### Step 5: Spawn API Subagent (BLOCKING)

**⚠️ CRITICAL**: This step MUST complete before any Client or Server work begins.

```bash
claude --print "Execute these API tasks: [list API task IDs and descriptions]

Context from plan.md:
- Contract Location: [from plan.md API Subagent Context]
- Type Output: [from plan.md]
- Validation Command: [from plan.md]

Tasks to execute:
[formatted list of API_TASKS]

IMPORTANT: Do NOT edit tasks.md directly. Instead, output a completion report at the end.

After completing all tasks, output this JSON report:
\`\`\`json
{
  \"agent\": \"api\",
  \"completed\": [\"T004\", \"T005\", \"T006\"],
  \"failed\": [],
  \"validation\": \"PASS\",
  \"notes\": \"Any relevant notes\"
}
\`\`\`" \
       --system-prompt "$(cat .specify/agents/api-agent.md)" \
       --allowedTools "Read,Write,Edit,Bash,Glob,Grep"
```

**WAIT** for API subagent to complete.

**Orchestrator Action**: Parse the JSON completion report and update tasks.md:
- For each task ID in `completed`: Change `- [ ]` to `- [X]`
- For each task ID in `failed`: Leave as `- [ ]` and log the failure

### Step 6: Execute User Stories (Client + Server in Parallel)

For each user story in priority order (US1 → US2 → US3...):

#### 6a. Spawn Client Subagent

```bash
claude --print "Execute these Client tasks for User Story [US#]: [list CLI task IDs]

Context from plan.md:
- Source Location: [from plan.md Client Subagent Context]
- Test Location: [from plan.md]
- Mock Location: [from plan.md]
- Build Command: [from plan.md]
- Test Command: [from plan.md]

Pattern: Create mock HTTP responses → Write failing integration test → Implement client code
Constraint: ONLY mock at HTTP boundary (no internal service mocks)

Tasks to execute:
[formatted list of CLI_TASKS for this user story]

IMPORTANT: Do NOT edit tasks.md directly. Instead, output a completion report at the end.

After completing all tasks, output this JSON report:
\`\`\`json
{
  \"agent\": \"client\",
  \"story\": \"US1\",
  \"completed\": [\"T010\", \"T011\", \"T012\"],
  \"failed\": [],
  \"build\": \"PASS\",
  \"tests\": \"PASS\",
  \"notes\": \"Any relevant notes\"
}
\`\`\`" \
       --system-prompt "$(cat .specify/agents/client-agent.md)" \
       --allowedTools "Read,Write,Edit,Bash,Glob,Grep"
```

#### 6b. Spawn Server Subagent (IN PARALLEL with Client)

```bash
claude --print "Execute these Server tasks for User Story [US#]: [list SRV task IDs]

Context from plan.md:
- Source Location: [from plan.md Server Subagent Context]
- Test Location: [from plan.md]
- Build Command: [from plan.md]
- Test Command: [from plan.md]

Pattern: Red (failing test) → Green (minimal code) → Refactor
Constraint: Tests MUST fail first, then implement to pass

Tasks to execute:
[formatted list of SRV_TASKS for this user story]

IMPORTANT: Do NOT edit tasks.md directly. Instead, output a completion report at the end.

After completing all tasks, output this JSON report:
\`\`\`json
{
  \"agent\": \"server\",
  \"story\": \"US1\",
  \"completed\": [\"T020\", \"T021\", \"T022\"],
  \"failed\": [],
  \"build\": \"PASS\",
  \"tests\": \"PASS\",
  \"notes\": \"Any relevant notes\"
}
\`\`\`" \
       --system-prompt "$(cat .specify/agents/server-agent.md)" \
       --allowedTools "Read,Write,Edit,Bash,Glob,Grep"
```

**WAIT** for BOTH Client and Server subagents to complete for this user story.

**Orchestrator Action**: After BOTH agents complete, parse their JSON reports and update tasks.md ONCE:
- Collect completed task IDs from both client and server reports
- Update tasks.md: Change `- [ ]` to `- [X]` for all completed tasks
- Log any failed tasks

**Checkpoint**: Verify User Story [US#] is complete:
- All [CLI] [US#] tasks in completed arrays
- All [SRV] [US#] tasks in completed arrays
- Report: "User Story [US#] complete"

#### 6c. Environment Validation Checkpoint

After each user story completes, spawn the Environment Validation Agent:

```bash
claude --print "Validate environment for User Story [US#]

Context from plan.md:
- Server Start Command: [from plan.md]
- Client Start Command: [from plan.md]
- Server Port: [from plan.md]
- Client Port: [from plan.md]

Scenarios to validate from quickstart.md:
[list relevant scenarios for this user story]

IMPORTANT:
- Run servers in BACKGROUND (do not block)
- Use TIMEOUTS for all commands
- ALWAYS clean up processes when done
- You have FULL AUTONOMY to fix any issues found

Output JSON completion report when done." \
       --system-prompt "$(cat .specify/agents/environment-validation-agent.md)" \
       --allowedTools "Read,Write,Edit,Bash,Glob,Grep"
```

**Orchestrator Action**: Parse the JSON report:
- If `status: "PASS"` → proceed to next user story
- If `status: "FAIL"` → halt and report issues
- Log any `fixes_applied` for the completion report

### Step 7: Execute [SHARED] Polish Tasks

Execute polish tasks **directly** (no subagent needed):

For each task in SHARED_POLISH_TASKS:
1. Execute the task
2. Mark task as complete [X] in tasks.md
3. Report progress

### Step 8: Final Environment Validation

Before reporting completion, run final environment validation:

```bash
claude --print "Final environment validation for feature [FEATURE_NAME]

Context from plan.md:
- Server Start Command: [from plan.md]
- Client Start Command: [from plan.md]
- All ports and endpoints

Run ALL scenarios from quickstart.md to verify complete system works.

IMPORTANT:
- Run servers in BACKGROUND (do not block)
- Use TIMEOUTS for all commands
- ALWAYS clean up processes when done
- You have FULL AUTONOMY to fix any issues found

This is the FINAL validation before deployment.
Output JSON completion report when done." \
       --system-prompt "$(cat .specify/agents/environment-validation-agent.md)" \
       --allowedTools "Read,Write,Edit,Bash,Glob,Grep"
```

**If validation fails**: Halt and report - do not mark implementation as complete.

### Step 9: Final Report

1. **Verify all tasks complete**:
   - Scan tasks.md for any remaining `[ ]` unchecked tasks
   - If incomplete tasks found, report which tasks failed

2. **Verify all validations passed**:
   - All user story checkpoints: PASS
   - Final environment validation: PASS

3. **Generate completion report**:
   ```
   ═══════════════════════════════════════════════════════════
   IMPLEMENTATION COMPLETE
   ═══════════════════════════════════════════════════════════

   Feature: [FEATURE_NAME]

   Phases Completed:
   ✓ Setup ([SHARED] tasks)
   ✓ API Contracts ([API] tasks)
   ✓ User Story 1 ([CLI] + [SRV] tasks)
     └── Environment Validation: PASS
   ✓ User Story 2 ([CLI] + [SRV] tasks)
     └── Environment Validation: PASS
   ...
   ✓ Polish ([SHARED] tasks)
   ✓ Final Environment Validation: PASS

   Subagents Spawned:
   - Checklist Agent: [PASS/FAIL/SKIPPED]
   - API Agent: [X] tasks completed
   - Client Agent: [X] tasks completed (per story)
   - Server Agent: [X] tasks completed (per story)
   - Environment Validation Agent: [X] checkpoints passed

   Environment Validation:
   - Server Starts: PASS
   - API Endpoints: PASS
   - Client Builds: PASS
   - Integration: PASS

   Fixes Applied by Environment Validation:
   - [list any fixes applied during validation]

   ═══════════════════════════════════════════════════════════
   ```

---

## Orchestrator Rules

### Execution Order (STRICT)

```
1. [SHARED] Setup → direct execution
2. [API] Contracts → API subagent (BLOCKING)
   └── MUST complete before step 3
3. For each User Story:
   ├── [CLI] tasks → Client subagent ─┐
   └── [SRV] tasks → Server subagent ─┴── PARALLEL, wait for both
   └── Environment Validation → verify real system works (can fix issues)
4. [SHARED] Polish → direct execution
5. Final Environment Validation → full system check before completion
```

### Subagent Constraints

- **Never 2 subagents of same type simultaneously**
- **Each subagent verifies code compiles before marking task complete**
- **Subagents read plan.md for tech-specific commands**
- **All subagent prompts include task list and context from plan.md**

### Error Handling

- If subagent fails: Report error, do NOT proceed to dependent phases
- If compilation fails: Subagent must fix before marking task complete
- If test fails unexpectedly: Report and pause for user decision
- For [P] parallel tasks: If one fails, continue others, report failures at end

### Task Tracking (Orchestrator Responsibility)

**CRITICAL**: Only the orchestrator edits tasks.md - subagents NEVER edit it directly.

```
Subagent Flow:
1. Subagent executes tasks
2. Subagent outputs JSON completion report
3. Orchestrator parses JSON report
4. Orchestrator updates tasks.md (single writer)
```

**Update Pattern**:
```
After API subagent completes:
  → Parse JSON → Update tasks.md with [API] tasks

After BOTH Client + Server complete (per user story):
  → Parse both JSON reports → Update tasks.md with [CLI] + [SRV] tasks
  → Single atomic update avoids race conditions
```

- Progress updates after each phase
- Final report summarizes all completed work

---

## Subagent Spawning Reference

### Claude CLI Syntax

```bash
claude --print "[PROMPT]" \
       --system-prompt "$(cat .specify/agents/[agent-name].md)" \
       --allowedTools "Read,Write,Edit,Bash,Glob,Grep"
```

### Available Subagents

| Agent | File | Purpose |
|-------|------|---------|
| checklist-agent | .specify/agents/checklist-agent.md | Verify checklists |
| api-agent | .specify/agents/api-agent.md | API contracts, type generation |
| client-agent | .specify/agents/client-agent.md | Frontend, integration tests |
| server-agent | .specify/agents/server-agent.md | Backend, TDD unit tests |
| environment-validation-agent | .specify/agents/environment-validation-agent.md | Verify real system works, fix issues |

---

## Notes

- This command requires tasks.md with component markers ([API], [CLI], [SRV], [SHARED])
- If tasks are missing markers, suggest running `/speckit.tasks` to regenerate
- Subagent system prompts are in `.specify/agents/` directory
- Build/test commands come from plan.md "Build & Test Commands" section

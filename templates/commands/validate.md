---
description: Run environment validation for server or client
scripts:
  sh: scripts/bash/check-prerequisites.sh --json
  ps: scripts/powershell/check-prerequisites.ps1 -Json
---

## User Input

```text
$ARGUMENTS
```

## Target Selection

**REQUIRED**: You must specify exactly ONE target:

| Argument | What it validates |
|----------|-------------------|
| `server` | Server starts, API endpoints respond, dependencies work |
| `client` | Client builds, dev server starts, can access pages |

**Examples**:
- `/speckit.validate server` → Validate server environment
- `/speckit.validate client` → Validate client environment

**INVALID** (do nothing and explain):
- `/speckit.validate` → No target specified
- `/speckit.validate both` → Cannot validate multiple targets
- `/speckit.validate all` → Cannot validate multiple targets

## Outline

### Step 1: Validate Arguments

Parse `$ARGUMENTS` and validate:

1. **Extract target** from arguments (case-insensitive: "server", "client")
2. **If no target specified**: Output error message and stop
   ```
   Error: Target required.

   Usage: /speckit.validate <server|client>

   Examples:
   - /speckit.validate server  → Validate server starts and APIs respond
   - /speckit.validate client  → Validate client builds and dev server works
   ```
3. **If multiple targets specified**: Output error message and stop
   ```
   Error: Only one target allowed per session.

   Run validation separately:
   - /speckit.validate server
   - /speckit.validate client
   ```

### Step 2: Initialize Context

1. Run `{SCRIPT}` from repo root and parse FEATURE_DIR and AVAILABLE_DOCS list. All paths must be absolute.

2. **Load validation context**:
   - **REQUIRED**: Read plan.md for build/test commands, ports, start commands
   - **REQUIRED**: Read quickstart.md for integration scenarios
   - **IF EXISTS**: Read contracts/api.yaml for expected endpoints

### Step 3: Spawn Environment Validation Agent

```bash
claude --print "Validate [TARGET] environment

Target: [server|client]

Context from plan.md:
[For server:]
- Server Start Command: [from plan.md]
- Server Port: [from plan.md]
- Server Build Command: [from plan.md]
- Server Test Command: [from plan.md]

[For client:]
- Client Start Command: [from plan.md]
- Client Port: [from plan.md]
- Client Build Command: [from plan.md]
- Client Test Command: [from plan.md]

Scenarios to validate from quickstart.md:
[list relevant scenarios for this target]

IMPORTANT:
- Target is [server|client] - validate ONLY this target
- Run processes in BACKGROUND (do not block)
- Use TIMEOUTS for all commands
- ALWAYS clean up processes when done
- You have FULL AUTONOMY to fix any issues found

Output JSON completion report when done." \
       --system-prompt "$(cat .specify/agents/environment-validation-agent.md)" \
       --allowedTools "Read,Write,Edit,Bash,Glob,Grep"
```

### Step 4: Process Results

Parse the JSON completion report from the agent:

**If status is "PASS"**:
```
═══════════════════════════════════════════════════════════════════════════════
VALIDATION PASSED: [TARGET]
═══════════════════════════════════════════════════════════════════════════════

All validations passed:
✓ Dependencies installed
✓ [Server starts / Client builds]
✓ [API endpoints respond / Dev server accessible]
✓ Integration scenarios work

Fixes applied: [list any fixes or "None"]

═══════════════════════════════════════════════════════════════════════════════
```

**If status is "FAIL"**:
```
═══════════════════════════════════════════════════════════════════════════════
VALIDATION FAILED: [TARGET]
═══════════════════════════════════════════════════════════════════════════════

Failed validations:
✗ [list failed items]

Attempted fixes: [list any attempted fixes]

Please resolve the issues above and run validation again.
═══════════════════════════════════════════════════════════════════════════════
```

---

## When to Run Validation

| After | Run |
|-------|-----|
| `/speckit.implement api` | `/speckit.validate server` (verify types work) |
| `/speckit.implement server` | `/speckit.validate server` |
| `/speckit.implement client` | `/speckit.validate client` |

---

## Notes

- Validation runs the real system, not mocks
- The agent has autonomy to fix issues it finds
- Always cleans up processes after validation
- Uses timeouts to prevent getting stuck

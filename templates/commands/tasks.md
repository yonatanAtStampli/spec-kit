---
description: Generate actionable, dependency-ordered task files for the feature based on available design artifacts.
handoffs:
  - label: Analyze For Consistency
    agent: speckit.analyze
    prompt: Run a project analysis for consistency
    send: true
  - label: Implement API Contracts
    agent: speckit.implement
    prompt: Start with API contract implementation
    send: true
scripts:
  sh: scripts/bash/check-prerequisites.sh --json
  ps: scripts/powershell/check-prerequisites.ps1 -Json
---

## User Input

```text
$ARGUMENTS
```

You **MUST** consider the user input before proceeding (if not empty).

## Outline

1. **Setup**: Run `{SCRIPT}` from repo root and parse FEATURE_DIR and AVAILABLE_DOCS list. All paths must be absolute. For single quotes in args like "I'm Groot", use escape syntax: e.g 'I'\''m Groot' (or double-quote if possible: "I'm Groot").

2. **Load design documents**: Read from FEATURE_DIR:
   - **Required**: plan.md (tech stack, libraries, structure), spec.md (user stories with priorities)
   - **Optional**: data-model.md (entities), contracts/ (API endpoints), research.md (decisions), quickstart.md (test scenarios)
   - Note: Not all projects have all documents. Generate tasks based on what's available.

3. **Execute task generation workflow**:
   - Load plan.md and extract tech stack, libraries, project structure
   - Load spec.md and extract user stories with their priorities (P1, P2, P3, etc.)
   - If data-model.md exists: Extract entities and map to user stories
   - If contracts/ exists: Map endpoints to user stories
   - If research.md exists: Extract decisions for setup tasks
   - Generate tasks organized by user story (see Task Generation Rules below)
   - Generate dependency graph showing user story completion order
   - Create parallel execution examples per user story
   - Validate task completeness (each user story has all needed tasks, independently testable)

4. **Generate THREE separate task files**:

   Create these files in FEATURE_DIR using the templates in `templates/`:

   | File | Template | Contains |
   |------|----------|----------|
   | `tasks-api.md` | `tasks-api-template.md` | [SHARED] Setup + [API] tasks |
   | `tasks-client.md` | `tasks-client-template.md` | [CLI] tasks per user story |
   | `tasks-server.md` | `tasks-server-template.md` | [SRV] tasks per user story |

   **Why separate files?**
   - Enables parallel sessions (one working on client, another on server)
   - Clear ownership and no merge conflicts
   - Independent progress tracking

5. **Report**: Output paths to generated task files and summary:
   - Total task count per file
   - Task count per user story
   - Parallel opportunities identified
   - Independent test criteria for each story
   - Suggested MVP scope (typically just User Story 1)
   - Format validation: Confirm ALL tasks follow the checklist format

Context for task generation: {ARGS}

The task files should be immediately executable - each task must be specific enough that an LLM can complete it without additional context.

## Task Generation Rules

**CRITICAL**: Tasks MUST be organized by user story to enable independent implementation and testing.

**Tests are OPTIONAL**: Only generate test tasks if explicitly requested in the feature specification or if user requests TDD approach.

### Checklist Format (REQUIRED)

Every task MUST strictly follow this format:

```text
- [ ] [TaskID] [P?] [Story?] Description with file path
```

**Format Components**:

1. **Checkbox**: ALWAYS start with `- [ ]` (markdown checkbox)
2. **Task ID**: Sequential number within file (T001, T002, T003...)
3. **[P] marker**: Include ONLY if task is parallelizable (different files, no dependencies on incomplete tasks)
4. **[Story] label**: REQUIRED for user story tasks
   - Format: [US1], [US2], [US3], etc. (maps to user stories from spec.md)
   - API file: Setup tasks have no label, then [US1], [US2] etc. for story-specific contracts
   - Client/Server files: ALL tasks should have story labels
5. **Description**: Clear action with exact file path

**Task ID Ranges** (to avoid conflicts between files):
- API tasks: T001-T299
- Client tasks: T300-T599
- Server tasks: T600-T899

**Examples**:

- ✅ CORRECT (API): `- [ ] T001 Create project structure per implementation plan`
- ✅ CORRECT (API): `- [ ] T010 [US1] Define User endpoints in contracts/api.yaml`
- ✅ CORRECT (Client): `- [ ] T300 [P] [US1] Create mock HTTP responses in client/tests/mocks/`
- ✅ CORRECT (Server): `- [ ] T600 [P] [US1] Write failing unit test for User model`
- ❌ WRONG: `- [ ] Create User model` (missing ID and Story label)
- ❌ WRONG: `T001 [US1] Create model` (missing checkbox)

### File Organization

**tasks-api.md**:
- Phase 1: Setup [SHARED] - Project initialization
- Phase 2: API Contracts [API] - OpenAPI schemas, type generation for **ALL user stories**
- **CRITICAL**: ALL API contracts for ALL user stories must be defined here
- Client and Server implementation CANNOT begin until every task in this file is complete

**tasks-client.md**:
- Organized by user story (US1, US2, US3...)
- Each story: Mocks → Integration tests → Implementation
- Pattern: Integration Tests First

**tasks-server.md**:
- Organized by user story (US1, US2, US3...)
- Each story: Unit tests → Models → Services → Endpoints
- Pattern: TDD (Tests First)

### Phase Structure

- **API File**: Setup → Contracts → Type Generation
- **Client File**: Per User Story (Mocks → Tests → Implementation)
- **Server File**: Per User Story (Tests → Implementation)

## Workflow After Task Generation

After running `/speckit.tasks`, the expected workflow is:

```
1. /speckit.implement api     → Execute API tasks
2. /speckit.validate server   → Verify server can build
3. [Mark API tasks done, stop]

4a. Session A: /speckit.implement server   → Execute Server tasks
4b. Session B: /speckit.implement client   → Execute Client tasks
    [These can run in PARALLEL in separate terminals/sessions]

5. /speckit.validate server   → Final server validation
6. /speckit.validate client   → Final client validation
```

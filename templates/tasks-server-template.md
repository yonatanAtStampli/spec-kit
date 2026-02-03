---
description: "Server task list for feature implementation"
---

# Server Tasks: [FEATURE NAME]

**Input**: Design documents from `/specs/[###-feature-name]/`
**Prerequisites**: tasks-api.md MUST be complete, contracts/ must exist, shared/types/ must be generated
**Executor**: `/speckit.implement server`

## Format: `[ID] [P?] [Story] Description`

- **[P]**: Can run in parallel (different files, no dependencies)
- **[Story]**: Which user story this task belongs to (REQUIRED for all tasks)
- **Task ID Range**: T600-T899 (reserved for Server tasks)

## Development Pattern

**TDD (Test-Driven Development)**:
1. Write failing unit test → Red phase
2. Implement minimum code to pass → Green phase
3. Refactor if needed → Refactor phase

**Constraint**: Tests MUST fail first, then implement to pass

<!--
  ============================================================================
  IMPORTANT: The tasks below are SAMPLE TASKS for illustration purposes only.

  The /speckit.tasks command MUST replace these with actual tasks based on:
  - User stories from spec.md (with their priorities P1, P2, P3...)
  - Data model from data-model.md
  - API contracts from contracts/

  DO NOT keep these sample tasks in the generated file.
  ============================================================================
-->

## User Story 1 - [Title] (Priority: P1)

**Goal**: [Brief description of what this story delivers]
**Independent Test**: [How to verify this story works on its own]

### Models

- [ ] T600 [P] [US1] Write failing unit test for User model in server/tests/unit/
- [ ] T601 [US1] Implement User model to pass test in server/src/models/

### Services

- [ ] T602 [P] [US1] Write failing unit test for UserService in server/tests/unit/
- [ ] T603 [US1] Implement UserService to pass test in server/src/services/

### API Endpoints

- [ ] T604 [US1] Implement GET /api/users endpoint in server/src/api/
- [ ] T605 [US1] Implement POST /api/users endpoint in server/src/api/
- [ ] T606 [US1] Write contract tests for User endpoints in server/tests/contract/

**Checkpoint**: Run server tests - all US1 tests should pass

---

## User Story 2 - [Title] (Priority: P2)

**Goal**: [Brief description of what this story delivers]
**Independent Test**: [How to verify this story works on its own]

### Models

- [ ] T620 [P] [US2] Write failing unit tests for US2 models

### Services

- [ ] T621 [US2] Implement services for US2

### API Endpoints

- [ ] T622 [US2] Implement endpoints for US2
- [ ] T623 [US2] Write contract tests for US2 endpoints

**Checkpoint**: Run server tests - all US1 and US2 tests should pass

---

[Add more user story sections as needed]

---

## Polish

- [ ] T890 [P] Code cleanup and optimization
- [ ] T891 [P] Add missing error handling
- [ ] T892 Final test run and build verification

---

## Completion Checklist

Before marking Server phase complete:

- [ ] All unit tests pass
- [ ] All contract tests pass
- [ ] Server builds without errors (run build command from plan.md)
- [ ] No TypeScript/compilation errors
- [ ] API responses match contract schemas

---

## Notes

- Task IDs T600-T899 are reserved for this file
- ALL tasks must have [Story] label (US1, US2, etc.)
- This file can be worked on in a SEPARATE session from client tasks
- **Depends on: ALL tasks in tasks-api.md must be complete** (contracts for ALL user stories)
- TDD pattern: Write test FIRST, verify it FAILS, then implement

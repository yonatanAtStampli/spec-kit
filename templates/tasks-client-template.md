---
description: "Client task list for feature implementation"
---

# Client Tasks: [FEATURE NAME]

**Input**: Design documents from `/specs/[###-feature-name]/`
**Prerequisites**: tasks-api.md MUST be complete, contracts/ must exist, shared/types/ must be generated
**Executor**: `/speckit.implement client`

## Format: `[ID] [P?] [Story] Description`

- **[P]**: Can run in parallel (different files, no dependencies)
- **[Story]**: Which user story this task belongs to (REQUIRED for all tasks)
- **Task ID Range**: T300-T599 (reserved for Client tasks)

## Development Pattern

**Integration Tests First**:
1. Create mock HTTP responses → Based on API contracts
2. Write failing integration test → Test real user flows with mocked HTTP
3. Implement client code → Make tests pass using common-ui components

**Constraint**: ONLY mock at HTTP boundary - no internal service mocks

<!--
  ============================================================================
  IMPORTANT: The tasks below are SAMPLE TASKS for illustration purposes only.

  The /speckit.tasks command MUST replace these with actual tasks based on:
  - User stories from spec.md (with their priorities P1, P2, P3...)
  - API contracts from contracts/
  - UI specifications from contracts/ui/ (if Figma provided)

  DO NOT keep these sample tasks in the generated file.
  ============================================================================
-->

## User Story 1 - [Title] (Priority: P1)

**Goal**: [Brief description of what this story delivers]
**Independent Test**: [How to verify this story works on its own]

### Mocks

- [ ] T300 [P] [US1] Create mock HTTP responses for GET /api/users in client/tests/mocks/
- [ ] T301 [P] [US1] Create mock HTTP responses for POST /api/users in client/tests/mocks/

### Integration Tests

- [ ] T302 [US1] Write integration test for user list display in client/tests/integration/
- [ ] T303 [US1] Write integration test for user creation flow in client/tests/integration/

### Implementation

- [ ] T304 [US1] Implement UserService client in client/src/services/
- [ ] T305 [US1] Implement UserList component using common-ui DataGrid in client/src/components/
- [ ] T306 [US1] Implement UserForm component using common-ui Form in client/src/components/

**Checkpoint**: Run client tests - all US1 tests should pass

---

## User Story 2 - [Title] (Priority: P2)

**Goal**: [Brief description of what this story delivers]
**Independent Test**: [How to verify this story works on its own]

### Mocks

- [ ] T320 [P] [US2] Create mock HTTP responses for US2 endpoints

### Integration Tests

- [ ] T321 [US2] Write integration test for US2 flow

### Implementation

- [ ] T322 [US2] Implement components for US2

**Checkpoint**: Run client tests - all US1 and US2 tests should pass

---

[Add more user story sections as needed]

---

## Polish

- [ ] T590 [P] Code cleanup and component optimization
- [ ] T591 [P] Accessibility improvements
- [ ] T592 Final build verification

---

## Completion Checklist

Before marking Client phase complete:

- [ ] All integration tests pass
- [ ] Client builds without errors (run build command from plan.md)
- [ ] All common-ui components used correctly
- [ ] UI contracts applied (if Figma was provided)
- [ ] No TypeScript errors

---

## Notes

- Task IDs T300-T599 are reserved for this file
- ALL tasks must have [Story] label (US1, US2, etc.)
- This file can be worked on in a SEPARATE session from server tasks
- **Depends on: ALL tasks in tasks-api.md must be complete** (contracts for ALL user stories)
- Mock only at HTTP boundary - never mock internal services

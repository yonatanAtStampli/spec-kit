---

description: "Task list template for feature implementation"
---

# Tasks: [FEATURE NAME]

**Input**: Design documents from `/specs/[###-feature-name]/`
**Prerequisites**: plan.md (required), spec.md (required for user stories), research.md, data-model.md, contracts/

**Tests**: The examples below include test tasks. Tests are OPTIONAL - only include them if explicitly requested in the feature specification.

**Organization**: Tasks are grouped by phase and component type to enable orchestrated implementation with specialized subagents.

## Format: `[ID] [P?] [AgentType] [Story?] Description`

- **[P]**: Can run in parallel (different files, no dependencies)
- **[AgentType]**: Component marker for orchestrator routing:
  - **[API]** - API contract/specification tasks (OpenAPI schemas, contract tests, type generation)
  - **[CLI]** - Client-side tasks (frontend, integration tests with mocked HTTP responses)
  - **[SRV]** - Server-side tasks (backend, TDD unit tests, services, endpoints)
  - **[SHARED]** - Setup/foundational tasks (orchestrator handles directly)
- **[Story]**: Which user story this task belongs to (e.g., US1, US2, US3)
- Include exact file paths in descriptions

## Path Conventions

- **Single project**: `src/`, `tests/` at repository root
- **Web app**: `backend/src/`, `frontend/src/`
- **Mobile**: `api/src/`, `ios/src/` or `android/src/`
- Paths shown below assume single project - adjust based on plan.md structure

<!--
  ============================================================================
  IMPORTANT: The tasks below are SAMPLE TASKS for illustration purposes only.

  The /speckit.tasks command MUST replace these with actual tasks based on:
  - User stories from spec.md (with their priorities P1, P2, P3...)
  - Feature requirements from plan.md
  - Entities from data-model.md
  - Endpoints from contracts/

  Tasks MUST be organized by phase with correct [AgentType] markers so that:
  - API tasks complete FIRST (blocking)
  - Client and Server tasks can run in parallel per user story
  - SHARED tasks are handled by orchestrator directly

  DO NOT keep these sample tasks in the generated tasks.md file.
  ============================================================================
-->

## Phase 1: Setup [SHARED]

**Purpose**: Project initialization and basic structure
**Executor**: Orchestrator (direct execution)

- [ ] T001 [SHARED] Create project structure per implementation plan
- [ ] T002 [SHARED] Initialize monorepo with client/ and server/ directories
- [ ] T003 [P] [SHARED] Configure linting and formatting tools

---

## Phase 2: API Contracts [API]

**Purpose**: Define all API contracts before implementation begins
**Executor**: API Subagent
**⚠️ CRITICAL**: This phase MUST complete before Client and Server phases can begin

- [ ] T004 [API] Define OpenAPI schema for core endpoints in contracts/api.yaml
- [ ] T005 [P] [API] Generate TypeScript types from contracts to shared/types/
- [ ] T006 [P] [API] Generate server-side types from contracts
- [ ] T007 [API] Create contract test stubs in tests/contract/

**CHECKPOINT: API contracts finalized - Client and Server can proceed in parallel**

---

## Phase 3+: User Stories

### User Story 1 - [Title] (Priority: P1) 🎯 MVP

**Goal**: [Brief description of what this story delivers]

#### Client Tasks [CLI] - Integration Tests First

**Executor**: Client Subagent
**Pattern**: Create mock HTTP responses → Write failing integration test → Implement client code
**Constraint**: ONLY mock at HTTP boundary (no internal service mocks)

- [ ] T010 [P] [CLI] [US1] Create mock HTTP responses in client/tests/mocks/user.ts
- [ ] T011 [CLI] [US1] Write integration test for user flow in client/tests/integration/
- [ ] T012 [CLI] [US1] Implement UserService client in client/src/services/

#### Server Tasks [SRV] - TDD (Tests First)

**Executor**: Server Subagent
**Pattern**: Red (failing test) → Green (minimal code) → Refactor
**Constraint**: Tests MUST fail first, implement to pass

- [ ] T020 [P] [SRV] [US1] Write failing unit test for User model in server/tests/unit/
- [ ] T021 [SRV] [US1] Implement User model to pass test in server/src/models/
- [ ] T022 [SRV] [US1] Write failing unit test for UserService in server/tests/unit/
- [ ] T023 [SRV] [US1] Implement UserService to pass test in server/src/services/
- [ ] T024 [SRV] [US1] Implement User endpoint in server/src/api/

**Checkpoint**: User Story 1 - Client and Server should both work independently

---

### User Story 2 - [Title] (Priority: P2)

**Goal**: [Brief description of what this story delivers]

#### Client Tasks [CLI]

- [ ] T030 [P] [CLI] [US2] Create mock HTTP responses for US2 in client/tests/mocks/
- [ ] T031 [CLI] [US2] Write integration test for US2 flow
- [ ] T032 [CLI] [US2] Implement client components for US2

#### Server Tasks [SRV]

- [ ] T040 [P] [SRV] [US2] Write failing unit tests for US2
- [ ] T041 [SRV] [US2] Implement models/services to pass tests
- [ ] T042 [SRV] [US2] Implement endpoints for US2

**Checkpoint**: User Stories 1 AND 2 should both work independently

---

[Add more user story phases as needed, following the same pattern]

---

## Phase N: Polish & Cross-Cutting Concerns [SHARED]

**Purpose**: Improvements that affect multiple components
**Executor**: Orchestrator (direct execution)

- [ ] TXXX [P] [SHARED] Documentation updates in docs/
- [ ] TXXX [SHARED] Code cleanup and refactoring
- [ ] TXXX [SHARED] Performance optimization across all components
- [ ] TXXX [P] [SHARED] Additional tests (if requested)
- [ ] TXXX [SHARED] Security hardening
- [ ] TXXX [SHARED] Run quickstart.md validation

---

## Dependencies & Execution Order

### Phase Dependencies (Orchestrator Controls)

- **Setup (Phase 1) [SHARED]**: No dependencies - orchestrator executes directly
- **API Contracts (Phase 2) [API]**: Depends on Setup - **BLOCKS all Client/Server tasks**
- **User Stories (Phase 3+)**: All depend on API Contracts completion
  - Client [CLI] and Server [SRV] tasks can run in **PARALLEL** for same user story
  - User stories execute sequentially in priority order (P1 → P2 → P3)
- **Polish (Final Phase) [SHARED]**: Depends on all user stories being complete

### Orchestrator Execution Flow

```
1. Parse tasks.md → group by [API], [CLI], [SRV], [SHARED]
2. Execute [SHARED] Setup tasks directly
3. Spawn API subagent → execute all [API] tasks
   └── WAIT for completion (BLOCKING)
4. For each User Story (in priority order):
   ├── Spawn CLIENT subagent → [CLI] tasks
   └── Spawn SERVER subagent → [SRV] tasks
   └── Run in PARALLEL, wait for both
5. Execute [SHARED] Polish tasks
6. Report completion
```

### Subagent Constraints

- **Never 2 subagents of same type simultaneously**
- **Each subagent verifies code compiles before marking complete**
- **Subagents use plan.md for tech-specific build/test commands**

### Within Each User Story

- Tests (if included) MUST be written and FAIL before implementation
- Models before services
- Services before endpoints
- Core implementation before integration
- Story complete before moving to next priority

### Parallel Opportunities

- All [P] marked tasks within same phase can run in parallel
- Client [CLI] and Server [SRV] tasks run in parallel per user story
- Different parallel markers don't cross component boundaries

---

## Component Marker Reference

| Marker | Subagent | Focus | Constraint |
|--------|----------|-------|------------|
| [API] | api-agent | OpenAPI schemas, type generation, contract tests | No business logic |
| [CLI] | client-agent | Frontend, integration tests with HTTP mocks | Mock only at HTTP boundary |
| [SRV] | server-agent | Backend, TDD unit tests, services, endpoints | Tests must fail first |
| [SHARED] | orchestrator | Setup, polish, cross-cutting | Direct execution |

---

## Implementation Strategy

### API-First Pattern

1. All API contracts defined in `contracts/` before implementation
2. Types generated from contracts to `shared/types/`
3. Both Client and Server depend on these contracts

### MVP First (User Story 1 Only)

1. Complete Phase 1: Setup [SHARED]
2. Complete Phase 2: API Contracts [API] (CRITICAL - blocks all stories)
3. Complete Phase 3: User Story 1 ([CLI] + [SRV] in parallel)
4. **STOP and VALIDATE**: Test User Story 1 independently
5. Deploy/demo if ready

### Incremental Delivery

1. Setup + API Contracts → Foundation ready
2. Add User Story 1 → Test independently → Deploy/Demo (MVP!)
3. Add User Story 2 → Test independently → Deploy/Demo
4. Each story adds value without breaking previous stories

---

## Notes

- [P] tasks = different files, no dependencies within same component
- [AgentType] markers route tasks to specialized subagents
- [Story] label maps task to specific user story for traceability
- Each user story should be independently completable and testable
- Verify tests fail before implementing
- Commit after each task or logical group
- Stop at any checkpoint to validate story independently

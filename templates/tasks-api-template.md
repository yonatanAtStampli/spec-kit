---
description: "API and Setup task list for feature implementation"
---

# API Tasks: [FEATURE NAME]

**Input**: Design documents from `/specs/[###-feature-name]/`
**Prerequisites**: plan.md (required), spec.md (required for user stories), research.md, data-model.md
**Executor**: `/speckit.implement api`

## Format: `[ID] [P?] [Story?] Description`

- **[P]**: Can run in parallel (different files, no dependencies)
- **[Story]**: Which user story this task belongs to (e.g., US1, US2)
- **Task ID Range**: T001-T299 (reserved for API tasks)

## ⚠️ CRITICAL: Complete API for ALL User Stories

**ALL API contracts for ALL user stories in the spec MUST be defined in this file.**

Client and Server implementation CANNOT begin until:
- Every task in this file is marked `[X]` complete
- Contracts exist for every endpoint needed by every user story
- Types are generated for both client and server

This is a hard gate - there is no partial API completion.

<!--
  ============================================================================
  IMPORTANT: The tasks below are SAMPLE TASKS for illustration purposes only.

  The /speckit.tasks command MUST replace these with actual tasks based on:
  - Project setup requirements from plan.md
  - API contracts needed for user stories from spec.md
  - Entities from data-model.md

  DO NOT keep these sample tasks in the generated file.
  ============================================================================
-->

## Phase 1: Setup

**Purpose**: Project initialization and basic structure
**Executor**: Implement command (direct execution)

- [ ] T001 Create project structure per implementation plan
- [ ] T002 Initialize monorepo with client/ and server/ directories
- [ ] T003 [P] Configure linting and formatting tools
- [ ] T004 [P] Set up shared types directory structure

---

## Phase 2: API Contracts

**Purpose**: Define all API contracts before implementation begins
**⚠️ CRITICAL**: This phase MUST complete before Client and Server implementation can begin

### Core Contracts

- [ ] T010 Define OpenAPI schema for core endpoints in contracts/api.yaml
- [ ] T011 [P] Create request/response schemas in contracts/schemas/
- [ ] T012 [P] Create example payloads in contracts/examples/

### User Story Contracts

- [ ] T020 [US1] Define endpoints for User Story 1 in contracts/api.yaml
- [ ] T021 [US2] Define endpoints for User Story 2 in contracts/api.yaml

### Type Generation

- [ ] T030 Generate TypeScript types from contracts to shared/types/
- [ ] T031 [P] Generate server-side types from contracts
- [ ] T032 [P] Create contract test stubs in tests/contract/

---

## Completion Checklist

Before marking API phase complete:

- [ ] All OpenAPI schemas are valid (run validation command from plan.md)
- [ ] Types generated successfully to shared/types/
- [ ] Contract examples cover all endpoints
- [ ] No circular dependencies in schemas

---

## Notes

- Task IDs T001-T299 are reserved for this file
- Setup tasks have no [Story] label
- Contract tasks should be labeled with [US#] when story-specific
- **ALL user stories must have their API contracts defined here**
- After completion, run `/speckit.validate server` before proceeding

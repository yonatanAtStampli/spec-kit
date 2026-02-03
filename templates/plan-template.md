# Implementation Plan: [FEATURE]

**Branch**: `[###-feature-name]` | **Date**: [DATE] | **Spec**: [link]
**Input**: Feature specification from `/specs/[###-feature-name]/spec.md`

**Note**: This template is filled in by the `/speckit.plan` command. See `.specify/templates/commands/plan.md` for the execution workflow.

## Summary

[Extract from feature spec: primary requirement + technical approach from research]

## Technical Context

<!--
  ACTION REQUIRED: Replace the content in this section with the technical details
  for the project. The structure here is presented in advisory capacity to guide
  the iteration process.
-->

**Language/Version**: [e.g., Python 3.11, Swift 5.9, Rust 1.75 or NEEDS CLARIFICATION]
**Primary Dependencies**: [e.g., FastAPI, UIKit, LLVM or NEEDS CLARIFICATION]
**Storage**: [if applicable, e.g., PostgreSQL, CoreData, files or N/A]
**Testing**: [e.g., pytest, XCTest, cargo test or NEEDS CLARIFICATION]
**Target Platform**: [e.g., Linux server, iOS 15+, WASM or NEEDS CLARIFICATION]
**Project Type**: [single/web/mobile - determines source structure]
**Performance Goals**: [domain-specific, e.g., 1000 req/s, 10k lines/sec, 60 fps or NEEDS CLARIFICATION]
**Constraints**: [domain-specific, e.g., <200ms p95, <100MB memory, offline-capable or NEEDS CLARIFICATION]
**Scale/Scope**: [domain-specific, e.g., 10k users, 1M LOC, 50 screens or NEEDS CLARIFICATION]

### Build & Test Commands

<!--
  IMPORTANT: These commands are used by subagents to verify their work compiles/passes.
  Fill in based on the actual tech stack chosen.
-->

| Context | Command | Description |
|---------|---------|-------------|
| Client Build | `[e.g., npm run build]` | Verify client code compiles |
| Client Test | `[e.g., npm test]` | Run client integration tests |
| Server Build | `[e.g., cargo build]` | Verify server code compiles |
| Server Test | `[e.g., cargo test]` | Run server unit tests |
| Contract Gen | `[e.g., npm run generate:types]` | Generate types from contracts |
| Full Validation | `[e.g., npm run validate]` | Run all checks |

## Constitution Check

*GATE: Must pass before Phase 0 research. Re-check after Phase 1 design.*

[Gates determined based on constitution file]

## Project Structure

### Documentation (this feature)

```text
specs/[###-feature]/
├── spec.md              # Feature specification (/speckit.specify command output)
├── plan.md              # This file (/speckit.plan command output)
├── research.md          # Phase 0 output (/speckit.plan command)
├── data-model.md        # Phase 1 output (/speckit.plan command)
├── quickstart.md        # Phase 1 output (/speckit.plan command)
├── designs/             # UI screenshots (from /speckit.specify if Figma provided)
│   ├── main-view.png
│   ├── component-states.png
│   └── responsive-mobile.png
├── contracts/           # Phase 1 output - API-FIRST and UI artifacts
│   ├── api.yaml         # OpenAPI specification (REQUIRED before implementation)
│   ├── types/           # Generated types from contracts
│   └── ui/              # UI contracts (from Figma or manual)
│       ├── design-tokens.json
│       ├── components/
│       └── screens/
├── checklists/          # Quality checklists
│   ├── requirements.md
│   └── ui.md            # UI requirements checklist (if Figma provided)
├── tasks-api.md         # API + Setup tasks (/speckit.tasks output)
├── tasks-client.md      # Client tasks (/speckit.tasks output)
└── tasks-server.md      # Server tasks (/speckit.tasks output)
```

### Source Code (repository root)

<!--
  ACTION REQUIRED: Replace the placeholder tree below with the concrete layout
  for this feature. Delete unused options and expand the chosen structure with
  real paths (e.g., apps/admin, packages/something). The delivered plan must
  not include Option labels.

  NOTE: For Stampli Core projects, the web application structure is typical.
-->

```text
# [REMOVE IF UNUSED] Option 1: Single project (DEFAULT)
src/
├── models/
├── services/
├── cli/
└── lib/

tests/
├── contract/
├── integration/
└── unit/

# [REMOVE IF UNUSED] Option 2: Web application (RECOMMENDED for Stampli/core)
contracts/                    # API-FIRST: Contracts defined here FIRST
├── api.yaml                  # OpenAPI specification
└── schemas/                  # Shared JSON schemas

shared/                       # Generated from contracts
└── types/                    # TypeScript types for both client/server

client/                       # Frontend (Client Subagent domain)
├── src/
│   ├── components/
│   ├── pages/
│   └── services/
└── tests/
    ├── integration/          # Integration tests with HTTP mocks
    └── mocks/                # Mock HTTP responses

server/                       # Backend (Server Subagent domain)
├── src/
│   ├── models/
│   ├── services/
│   └── api/
└── tests/
    ├── unit/                 # TDD unit tests
    └── contract/             # Contract compliance tests

# [REMOVE IF UNUSED] Option 3: Mobile + API (when "iOS/Android" detected)
api/
└── [same as server above]

ios/ or android/
└── [platform-specific structure: feature modules, UI flows, platform tests]
```

**Structure Decision**: [Document the selected structure and reference the real
directories captured above]

## API-First Development Pattern

### Contracts Directory Structure

```text
contracts/
├── api.yaml                  # Main OpenAPI specification
├── schemas/                  # Reusable JSON schemas
│   ├── user.json
│   └── common.json
├── examples/                 # Request/response examples for mocking
│   ├── user-create.json
│   └── user-list.json
└── ui/                       # UI contracts (from Figma or manual)
    ├── design-tokens.json    # Colors, typography, spacing, effects
    ├── components/           # Component specifications
    │   ├── button.json
    │   ├── card.json
    │   └── input.json        # Form input states and styling
    ├── forms/                # Form specifications (fields, validation, behavior)
    │   ├── login-form.json
    │   └── user-form.json
    ├── screens/              # Screen layout specifications
    │   ├── user-list.json
    │   └── user-detail.json
    └── breakpoints.json      # Responsive breakpoint definitions
```

### UI Contracts Structure

**IMPORTANT**: If Figma designs were provided during `/speckit.specify`, UI contracts are auto-generated.
These contracts are the source of truth for visual implementation.

#### design-tokens.json
```json
{
  "source": "figma|manual",
  "figmaFile": "[file_key if from Figma]",
  "colors": {
    "primary": { "value": "#1a73e8", "usage": "Primary actions, links" },
    "error": { "value": "#d93025", "usage": "Error states, destructive actions" },
    "success": { "value": "#1e8e3e", "usage": "Success states, valid inputs" },
    "warning": { "value": "#f9ab00", "usage": "Warning states" }
  },
  "typography": {
    "heading-1": { "fontFamily": "Inter", "fontSize": "32px", "fontWeight": 700 },
    "body": { "fontFamily": "Inter", "fontSize": "16px", "fontWeight": 400 },
    "label": { "fontFamily": "Inter", "fontSize": "14px", "fontWeight": 500 },
    "error": { "fontFamily": "Inter", "fontSize": "12px", "fontWeight": 400 }
  },
  "spacing": {
    "xs": "4px", "sm": "8px", "md": "16px", "lg": "24px", "xl": "32px"
  },
  "effects": {
    "shadow-sm": "0 1px 2px rgba(0,0,0,0.1)",
    "shadow-md": "0 4px 6px rgba(0,0,0,0.1)",
    "focus-ring": "0 0 0 2px rgba(26,115,232,0.4)"
  },
  "borderRadius": {
    "sm": "4px", "md": "8px", "lg": "16px", "full": "9999px"
  }
}
```

#### Component Spec Example (components/button.json)
```json
{
  "name": "Button",
  "figmaNodeId": "[node_id if from Figma]",
  "variants": {
    "primary": { "background": "colors.primary", "text": "#ffffff" },
    "secondary": { "background": "transparent", "border": "colors.primary" }
  },
  "states": {
    "default": {},
    "hover": { "opacity": 0.9 },
    "active": { "transform": "scale(0.98)" },
    "disabled": { "opacity": 0.5, "cursor": "not-allowed" },
    "loading": { "opacity": 0.7, "cursor": "wait" }
  },
  "sizes": {
    "sm": { "padding": "spacing.xs spacing.sm", "fontSize": "14px" },
    "md": { "padding": "spacing.sm spacing.md", "fontSize": "16px" },
    "lg": { "padding": "spacing.md spacing.lg", "fontSize": "18px" }
  }
}
```

#### Form Input Spec Example (components/input.json)
```json
{
  "name": "Input",
  "figmaNodeId": "[node_id if from Figma]",
  "states": {
    "default": {
      "border": "1px solid #dadce0",
      "background": "#ffffff"
    },
    "focused": {
      "border": "2px solid colors.primary",
      "boxShadow": "effects.focus-ring"
    },
    "filled": {
      "border": "1px solid #dadce0"
    },
    "valid": {
      "border": "1px solid colors.success",
      "icon": "checkmark"
    },
    "invalid": {
      "border": "1px solid colors.error",
      "icon": "error",
      "errorMessageColor": "colors.error"
    },
    "disabled": {
      "background": "#f1f3f4",
      "cursor": "not-allowed"
    }
  },
  "elements": {
    "label": { "typography": "label", "marginBottom": "spacing.xs" },
    "helperText": { "typography": "body", "color": "#5f6368", "marginTop": "spacing.xs" },
    "errorMessage": { "typography": "error", "color": "colors.error", "marginTop": "spacing.xs" },
    "requiredIndicator": { "content": "*", "color": "colors.error" }
  }
}
```

#### Form Spec Example (forms/login-form.json)
```json
{
  "name": "LoginForm",
  "figmaNodeId": "[node_id if from Figma]",
  "fields": {
    "email": {
      "type": "email",
      "required": true,
      "label": "Email address",
      "placeholder": "Enter your email",
      "constraints": {
        "maxLength": 255
      },
      "validation": {
        "pattern": "^[^@]+@[^@]+\\.[^@]+$",
        "validateOn": "blur"
      },
      "errorMessages": {
        "required": "Email is required",
        "pattern": "Please enter a valid email address"
      }
    },
    "password": {
      "type": "password",
      "required": true,
      "label": "Password",
      "placeholder": "Enter your password",
      "constraints": {
        "minLength": 8,
        "maxLength": 128
      },
      "validation": {
        "rules": ["minLength", "maxLength"],
        "validateOn": "blur"
      },
      "errorMessages": {
        "required": "Password is required",
        "minLength": "Password must be at least 8 characters"
      }
    }
  },
  "submitButton": {
    "label": "Sign in",
    "loadingLabel": "Signing in..."
  },
  "states": {
    "pristine": { "submitEnabled": false },
    "dirty": { "submitEnabled": true },
    "submitting": { "submitEnabled": false, "fieldsDisabled": true, "showSpinner": true },
    "success": { "action": "redirect", "target": "/dashboard" },
    "error": { "showErrorBanner": true, "bannerMessage": "from-server" }
  },
  "dynamicBehavior": []
}
```

### Type Generation

**CRITICAL**: Types MUST be generated from contracts before any implementation begins.

| Source | Target | Command |
|--------|--------|---------|
| contracts/api.yaml | shared/types/api.ts | `[type generation command]` |
| contracts/api.yaml | server/src/types/ | `[server type generation]` |

### Contract-First Workflow

```
1. /speckit.implement api     → Define contracts, generate types
2. /speckit.validate server   → Verify server can build with types
3. [API phase complete - stop here]

4a. Session A: /speckit.implement server  ─┐
4b. Session B: /speckit.implement client  ─┴─ Can run in PARALLEL

5a. /speckit.validate server  → Verify server works
5b. /speckit.validate client  → Verify client works
```

**Why Separate Sessions?**
- No race conditions on task files
- Server and Client work on their own files
- Can be done by different developers/terminals

## Complexity Tracking

> **Fill ONLY if Constitution Check has violations that must be justified**

| Violation | Why Needed | Simpler Alternative Rejected Because |
|-----------|------------|-------------------------------------|
| [e.g., 4th project] | [current need] | [why 3 projects insufficient] |
| [e.g., Repository pattern] | [specific problem] | [why direct DB access insufficient] |

## Subagent Context

<!--
  This section provides context for specialized subagents during /speckit.implement.
  Each subagent reads this to understand tech stack and constraints.

  IMPORTANT: Each agent type has its own task file:
  - API Agent → tasks-api.md
  - Client Agent → tasks-client.md
  - Server Agent → tasks-server.md
-->

### API Subagent Context

- **Task File**: tasks-api.md
- **Contract Location**: contracts/api.yaml
- **Type Output**: shared/types/
- **Validation Command**: [e.g., npm run validate:contracts]
- **Constraints**: No business logic, schema definitions only

### Client Subagent Context

- **Task File**: tasks-client.md
- **Source Location**: client/src/
- **Test Location**: client/tests/
- **Mock Location**: client/tests/mocks/
- **Build Command**: [from Build & Test Commands table]
- **Test Command**: [from Build & Test Commands table]
- **Constraints**: Mock ONLY at HTTP boundary, no internal service mocks

#### UI Implementation Context

- **Design Tokens**: contracts/ui/design-tokens.json
- **Component Specs**: contracts/ui/components/
- **Screen Layouts**: contracts/ui/screens/
- **Reference Screenshots**: specs/[feature]/designs/
- **UI Checklist**: specs/[feature]/checklists/ui.md (if exists)

**UI Implementation Rules**:
1. Import design tokens and use token references (not hardcoded values)
2. Follow component specs for states, variants, and sizing
3. Reference screenshots when implementing layouts
4. Validate against UI checklist before marking tasks complete

### Server Subagent Context

- **Task File**: tasks-server.md
- **Source Location**: server/src/
- **Test Location**: server/tests/
- **Build Command**: [from Build & Test Commands table]
- **Test Command**: [from Build & Test Commands table]
- **Constraints**: TDD approach, tests must fail before implementation

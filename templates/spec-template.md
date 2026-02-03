# Feature Specification: [FEATURE NAME]

**Feature Branch**: `[###-feature-name]`  
**Created**: [DATE]  
**Status**: Draft  
**Input**: User description: "$ARGUMENTS"

## User Scenarios & Testing *(mandatory)*

<!--
  IMPORTANT: User stories should be PRIORITIZED as user journeys ordered by importance.
  Each user story/journey must be INDEPENDENTLY TESTABLE - meaning if you implement just ONE of them,
  you should still have a viable MVP (Minimum Viable Product) that delivers value.
  
  Assign priorities (P1, P2, P3, etc.) to each story, where P1 is the most critical.
  Think of each story as a standalone slice of functionality that can be:
  - Developed independently
  - Tested independently
  - Deployed independently
  - Demonstrated to users independently
-->

### User Story 1 - [Brief Title] (Priority: P1)

[Describe this user journey in plain language]

**Why this priority**: [Explain the value and why it has this priority level]

**Independent Test**: [Describe how this can be tested independently - e.g., "Can be fully tested by [specific action] and delivers [specific value]"]

**Acceptance Scenarios**:

1. **Given** [initial state], **When** [action], **Then** [expected outcome]
2. **Given** [initial state], **When** [action], **Then** [expected outcome]

---

### User Story 2 - [Brief Title] (Priority: P2)

[Describe this user journey in plain language]

**Why this priority**: [Explain the value and why it has this priority level]

**Independent Test**: [Describe how this can be tested independently]

**Acceptance Scenarios**:

1. **Given** [initial state], **When** [action], **Then** [expected outcome]

---

### User Story 3 - [Brief Title] (Priority: P3)

[Describe this user journey in plain language]

**Why this priority**: [Explain the value and why it has this priority level]

**Independent Test**: [Describe how this can be tested independently]

**Acceptance Scenarios**:

1. **Given** [initial state], **When** [action], **Then** [expected outcome]

---

[Add more user stories as needed, each with an assigned priority]

### Edge Cases

<!--
  ACTION REQUIRED: The content in this section represents placeholders.
  Fill them out with the right edge cases.
-->

- What happens when [boundary condition]?
- How does system handle [error scenario]?

## Requirements *(mandatory)*

<!--
  ACTION REQUIRED: The content in this section represents placeholders.
  Fill them out with the right functional requirements.
-->

### Functional Requirements

- **FR-001**: System MUST [specific capability, e.g., "allow users to create accounts"]
- **FR-002**: System MUST [specific capability, e.g., "validate email addresses"]  
- **FR-003**: Users MUST be able to [key interaction, e.g., "reset their password"]
- **FR-004**: System MUST [data requirement, e.g., "persist user preferences"]
- **FR-005**: System MUST [behavior, e.g., "log all security events"]

*Example of marking unclear requirements:*

- **FR-006**: System MUST authenticate users via [NEEDS CLARIFICATION: auth method not specified - email/password, SSO, OAuth?]
- **FR-007**: System MUST retain user data for [NEEDS CLARIFICATION: retention period not specified]

### Key Entities *(include if feature involves data)*

- **[Entity 1]**: [What it represents, key attributes without implementation]
- **[Entity 2]**: [What it represents, relationships to other entities]

## Success Criteria *(mandatory)*

<!--
  ACTION REQUIRED: Define measurable success criteria.
  These must be technology-agnostic and measurable.
-->

### Measurable Outcomes

- **SC-001**: [Measurable metric, e.g., "Users can complete account creation in under 2 minutes"]
- **SC-002**: [Measurable metric, e.g., "System handles 1000 concurrent users without degradation"]
- **SC-003**: [User satisfaction metric, e.g., "90% of users successfully complete primary task on first attempt"]
- **SC-004**: [Business metric, e.g., "Reduce support tickets related to [X] by 50%"]

## UI Design References *(include if Figma designs provided)*

<!--
  This section captures UI requirements from Figma designs.
  If Figma MCP is available, design tokens and component specs are auto-extracted.
  If not, manually document the key visual requirements here.

  IMPORTANT: These references flow through to:
  - plan.md (UI contracts structure)
  - contracts/ui/ (design tokens, component specs)
  - client agent (implementation reference)
  - UI checklist (requirements validation)
-->

### Figma Source Files

| Screen/Component | Figma Link | Node ID | Status |
|------------------|------------|---------|--------|
| [Screen Name] | [https://figma.com/file/xxx] | [node-id] | [Draft/Final] |
| [Component Name] | [https://figma.com/file/xxx?node-id=123] | [node-id] | [Draft/Final] |

### Design Token Requirements

<!--
  Key visual specifications that MUST be followed.
  These will be extracted to contracts/ui/design-tokens.json during planning.
-->

**Colors**:
- Primary: [color value or Figma style name]
- Secondary: [color value]
- Error/Warning/Success: [color values]
- Background/Surface: [color values]

**Typography**:
- Headings: [font family, sizes, weights]
- Body: [font family, sizes, weights]
- Labels/Captions: [font family, sizes, weights]

**Spacing**:
- Component padding: [values]
- Section margins: [values]
- Grid/layout spacing: [values]

**Effects**:
- Shadows: [shadow specifications]
- Border radius: [values]
- Transitions: [animation specs if any]

### Component Specifications

<!--
  Key components that have specific visual requirements.
  Reference Figma frames/components for exact specifications.
-->

| Component | Figma Reference | Key Visual Requirements |
|-----------|-----------------|------------------------|
| [Button] | [Figma link] | [States: default, hover, active, disabled] |
| [Card] | [Figma link] | [Layout, spacing, shadow] |
| [Form Input] | [Figma link] | [States, validation styles] |

### Form Specifications *(include if feature has forms)*

<!--
  Detailed form behavior specifications.
  CRITICAL for proper implementation - forms are a major source of bugs.
-->

#### Form Fields

| Field | Type | Required | Constraints | Validation | Error Message |
|-------|------|----------|-------------|------------|---------------|
| [Email] | email | Yes | max: 255 | Valid email format | "Please enter a valid email address" |
| [Password] | password | Yes | min: 8, max: 128 | 1 uppercase, 1 number, 1 special | "Password must contain..." |
| [Name] | text | Yes | min: 1, max: 100 | Non-empty | "Name is required" |
| [Phone] | tel | No | pattern: [regex] | Valid phone format | "Please enter a valid phone number" |

#### Field States

| State | Visual Treatment | When Applied |
|-------|------------------|--------------|
| Default/Empty | [placeholder text, border color] | Initial render |
| Focused | [border color, shadow] | User clicks/tabs into field |
| Filled | [text color, border] | Field has value |
| Valid | [success color, checkmark icon] | Validation passes |
| Invalid/Error | [error color, error icon, error message below] | Validation fails |
| Disabled | [gray background, no interaction] | Field not editable |
| Read-only | [no border, text only] | Display only |

#### Form-Level States

| State | Visual Treatment | Behavior |
|-------|------------------|----------|
| Pristine | Submit button [enabled/disabled] | No fields touched yet |
| Dirty | [unsaved changes indicator?] | At least one field modified |
| Submitting | [loading spinner, disabled inputs, disabled button] | Form being submitted |
| Submit Success | [success message, redirect?] | Submission completed |
| Submit Error | [error banner, field errors highlighted] | Submission failed |

#### Validation Behavior

- **When to validate**: [on-blur / on-change / on-submit]
- **Real-time validation**: [Yes/No - which fields?]
- **Show errors**: [immediately / on-blur / on-submit]
- **Clear errors**: [on-focus / on-change / manual]

#### Dynamic Behavior

<!--
  Conditional logic, dependent fields, auto-formatting
-->

| Condition | Action |
|-----------|--------|
| [When Country = "US"] | [Show State dropdown with US states] |
| [When "Other" selected] | [Show "Please specify" text field] |
| [When Password field focused] | [Show password requirements checklist] |

#### Auto-Formatting

| Field | Format | Example |
|-------|--------|---------|
| [Phone] | (###) ###-#### | (555) 123-4567 |
| [Credit Card] | #### #### #### #### | 4111 1111 1111 1111 |
| [Date] | MM/DD/YYYY | 12/31/2024 |

### Responsive Breakpoints

<!--
  If designs include responsive variants, document breakpoints here.
-->

| Breakpoint | Width | Figma Frame | Key Layout Changes |
|------------|-------|-------------|-------------------|
| Mobile | < 768px | [Figma link] | [Layout description] |
| Tablet | 768px - 1024px | [Figma link] | [Layout description] |
| Desktop | > 1024px | [Figma link] | [Layout description] |

### Design Screenshots

<!--
  Screenshots are stored in specs/[feature]/designs/
  These are auto-captured if Figma MCP is available, or manually added.
-->

| Screen | Screenshot Path | Description |
|--------|-----------------|-------------|
| [Main View] | `./designs/main-view.png` | [Brief description] |
| [Component States] | `./designs/component-states.png` | [All states documented] |

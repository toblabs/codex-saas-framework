# Feature Specification

## Metadata

- **Feature ID:** `PROJ-<id>`
- **Title:** `<feature title>`
- **Status:** `Draft`
- **Owner:** `<optional>`
- **Related PRD sections:** `<reference>`
- **Related architecture sections:** `<reference>`


## Problem

Describe the concrete user or business problem this feature solves.


## Goal

Describe the intended outcome of the feature in one concise paragraph.


## User Stories

### Primary story
As a `<user type>`  
I want `<capability>`  
So that `<benefit>`

### Additional stories
- As a `<user type>`, I want `<capability>`, so that `<benefit>`
- As a `<user type>`, I want `<capability>`, so that `<benefit>`


## Scope

### In Scope
- item
- item
- item

### Out of Scope
- item
- item


## Functional Requirements

- The system must ...
- The system must ...
- The system must ...


## Acceptance Criteria

- [ ] Criterion 1
- [ ] Criterion 2
- [ ] Criterion 3


## UI / UX

### Screens or routes affected
- route or screen
- route or screen

### Components
- Reuse existing **shadcn/ui** components wherever possible
- Do **not** recreate installed shadcn/ui primitives
- List any new feature-specific components that are required

### States
- loading
- empty
- success
- error


## Frontend Notes

- Implementation target: **Next.js App Router**
- Language: **TypeScript**
- Styling: **Tailwind CSS**
- Forms should prefer **react-hook-form** when structured form handling is needed
- Runtime validation should prefer **Zod** where user input or API payload validation is involved


## Backend Notes

Only fill this section if backend work is required.

- Does this feature require **Supabase**? `<yes/no>`
- Does it require database changes? `<yes/no>`
- Does it require auth or authorization changes? `<yes/no>`
- Does it require storage, realtime, or edge logic? `<yes/no>`

### Data / API requirements
- entity or table
- endpoint or server action
- validation requirement

### Security / access
- required auth checks
- required authorization checks
- required RLS considerations, if applicable


## Data Model Impact

List schema changes, tables, relationships, indexes, or migrations if needed.


## Validation Rules

List the expected input and output validation requirements.  
Prefer **Zod** for runtime validation.


## Non-Functional Requirements

### Performance
- target or expectation

### Security
- auth / authorization / secret handling / data exposure considerations

### Reliability
- expected failure handling and recovery behaviour


## Dependencies

- dependent feature
- external service
- design decision


## Edge Cases

- edge case
- edge case
- edge case


## Open Questions

- unresolved question
- unresolved question


## Implementation Notes

Use this section during implementation to document key technical decisions without replacing the formal architecture.

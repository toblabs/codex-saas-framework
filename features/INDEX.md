# Feature Index

This file tracks all features in the repository.

All implementation work must map back to a feature specification in this folder.


## Naming Convention

Feature spec files must use this format:

`PROJ-<id>-<feature-name>.md`

Examples:
- `PROJ-1-user-auth.md`
- `PROJ-2-dashboard.md`


## Feature List

| ID | Title | Status | Frontend | Backend | Deploy | Spec |
|---|---|---|---|---|---|---|
| PROJ-1 | Example Feature | Draft | Not Started | Not Needed | Not Started | `features/PROJ-1-example-feature.md` |


## Status Definitions

### Overall feature status
- **Draft** — feature is being defined
- **Planned** — spec is complete and ready for design / implementation
- **In Progress** — implementation is actively underway
- **Review** — implementation is complete and under QA / review
- **Done** — accepted and merged
- **Deployed** — available in deployed environment
- **Archived** — no longer active, retained for history

### Implementation sub-status
Use these values where helpful:
- `Not Started`
- `In Progress`
- `Done`
- `Not Needed`


## Tracking Rules

- Every feature must be listed here before implementation starts.
- Every listed feature must have exactly one spec file.
- Status must reflect the real project state.
- Keep this file synchronized with `docs/PRD.md`, `docs/ARCHITECTURE.md`, and implementation progress.
- Do not create duplicate feature specs for the same scope.


## Agent Notes

Agents must read this file at the start of feature work.

Before creating a new feature:
1. check whether similar scope already exists
2. avoid duplicates
3. choose the next sequential feature ID

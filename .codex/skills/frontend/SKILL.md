---
name: frontend
description: Implement or refine frontend functionality for this repository
---

# Frontend

## Purpose

Use this skill to implement or refine frontend functionality for this repository.

Frontend work in this repository must use:

- **Next.js 16 App Router**
- **TypeScript**
- **Tailwind CSS**
- **shadcn/ui**

This skill must preserve the repository's actual frontend conventions instead of introducing alternative patterns.


## Read First

Before starting, read:

1. `AGENTS.md`
2. `docs/PRD.md`
3. `docs/ARCHITECTURE.md`
4. `features/INDEX.md`
5. the relevant feature spec
6. the files you plan to modify


## Frontend Rules

### Technology rules
- Use **TypeScript**
- Use **Next.js App Router**
- Use **Tailwind CSS**
- Use **shadcn/ui first**
- Prefer existing repository patterns over new abstractions

### UI rules
- Check `src/components/ui/` before creating custom primitives
- Do **not** recreate installed shadcn/ui components
- Reuse existing components where possible
- Keep design language visually consistent

### Form rules
- Prefer **react-hook-form** when the feature involves structured forms
- Prefer **Zod** when runtime validation is needed

### State rules
- Prefer simple local state first
- use Context only when shared state clearly requires it
- align with existing repository patterns before introducing new state patterns

### General rules
- Read files before editing
- Keep changes focused
- Do not refactor unrelated areas without clear need
- Preserve accessibility and loading/error states


## Process

### 1. Confirm feature scope
Match the implementation against:
- feature spec
- architecture
- existing code patterns

### 2. Inspect existing UI
Search for:
- existing routes
- shared components
- form patterns
- utility functions
- styles and layout patterns

### 3. Implement with stack discipline
Use:
- App Router page/layout/component structure
- Tailwind classes for styling
- shadcn/ui primitives for building blocks
- TypeScript types
- react-hook-form and Zod where appropriate

### 4. Cover states
Where relevant, implement:
- loading state
- empty state
- success state
- error state

### 5. Keep docs in sync
If implementation changes feature status or scope, update the relevant feature files.


## Output Quality Bar

A good frontend change:
- looks native to this repository
- reuses existing UI patterns
- does not fight the stack
- is easy to review
- is safe to deploy


## Do Not

- do not introduce an alternative component library
- do not use ad hoc CSS systems instead of Tailwind
- do not bypass shadcn/ui when an existing primitive already solves the problem
- do not ignore TypeScript typing

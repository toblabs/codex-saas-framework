---
name: qa
description: Verify that implementation satisfies the feature specification, respects repository rules, and does not introduce obvious regressions
---

# QA

## Purpose

Use this skill to verify that implementation satisfies the feature specification, respects repository rules, and does not introduce obvious regressions.

QA in this repository must validate not only behaviour, but also stack compliance:

- **Next.js App Router**
- **TypeScript**
- **Tailwind CSS**
- **shadcn/ui**
- **Supabase**
- **PostgreSQL**
- **Zod**
- **Vercel compatibility**


## Read First

Before starting, read:

1. `AGENTS.md`
2. the relevant feature spec
3. `docs/ARCHITECTURE.md`
4. changed implementation files


## QA Rules

### Functional QA
- validate acceptance criteria directly
- verify primary user flow
- verify edge cases listed in the spec
- check failure paths where relevant

### Frontend QA
- check whether UI follows repository conventions
- verify shadcn/ui reuse where expected
- verify loading, empty, success, and error states
- verify route behaviour in App Router context

### Backend QA
- verify backend behaviour against spec
- check validation expectations
- check auth and authorization boundaries
- check data access assumptions and error handling

### Stack compliance QA
- flag introduction of off-stack libraries or patterns
- flag unnecessary custom UI where shadcn/ui should be used
- flag validation gaps where Zod or equivalent repository pattern is expected

### Documentation QA
- confirm feature status and docs are updated when needed


## Process

### 1. Compare implementation against spec
Use the acceptance criteria as the primary QA checklist.

### 2. Check stack alignment
Confirm the change still fits:
- Next.js App Router
- TypeScript
- Tailwind
- shadcn/ui
- Supabase / PostgreSQL / Zod where applicable

### 3. Review regressions
Look for:
- broken routes
- inconsistent components
- validation omissions
- auth oversights
- documentation drift

### 4. Report clearly
Summarize:
- what passed
- what failed
- what is risky
- what blocks merge or deployment


## Output Quality Bar

A good QA output:
- maps directly to acceptance criteria
- identifies real risks, not generic warnings
- checks both behaviour and repository conventions
- helps the next step make a clear decision


## Do Not

- do not say “looks good” without checking the spec
- do not ignore stack violations
- do not ignore security or authorization issues

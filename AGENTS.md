# AGENTS.md

## Project Overview

This repository is a **Next.js application starter kit** with an **AI-assisted, document-driven workflow**.

Agents must work from repository artifacts, not from assumptions.  
The core project state lives in:

- `docs/PRD.md`
- `docs/ARCHITECTURE.md`
- `features/INDEX.md`
- `features/PROJ-*-*.md`

Before implementing anything, always read the relevant artifact files first.


## Tech Stack

### Frontend
- **Framework:** Next.js 16 with App Router
- **Language:** TypeScript
- **Styling:** Tailwind CSS
- **UI Library:** shadcn/ui
- **Forms:** react-hook-form
- **Validation:** Zod
- **State:** React `useState` / Context API by default
- **Testing:** follow existing repo setup; prefer component and integration tests where applicable

### Backend
- **Backend Platform:** Supabase (optional, but preferred when backend is needed)
- **Database:** PostgreSQL via Supabase
- **Auth / Storage / Realtime:** Supabase services
- **Validation:** Zod for runtime validation
- **Security Model:** prefer Supabase RLS policies for data access control

### Deployment / Infra
- **Deployment Target:** Vercel
- **Package Manager / Scripts:** use the repo's existing npm scripts
- **Environment File:** `.env.local` for local development


## Technology Rules

These technology choices are **intentional defaults**, not suggestions.

- Use **Next.js App Router** patterns, not Pages Router patterns, unless the repo already contains a valid exception.
- Use **TypeScript** for all new application code.
- Use **Tailwind CSS** for styling.
- Use **shadcn/ui first** for UI work.
- Use **Zod** for runtime validation.
- Use **react-hook-form** for forms that need validation and structured handling.
- Use **Supabase** when backend, database, auth, storage, or realtime features are required.
- Target **Vercel**-compatible deployment decisions.

Do **not** introduce alternative core technologies without a clear repository-level reason.


## Rules Integration

This repository originally uses dedicated rules files. Their intent must remain enforced in Codex:

### General rules
- Always read a file before modifying it.
- Never assume file contents from memory.
- Verify real import paths, routes, component names, and APIs by reading the code.
- Keep feature tracking files synchronized with implementation progress.

### Frontend rules
- Prefer **existing shadcn/ui components** over custom replacements.
- Do **not** recreate installed shadcn/ui components.
- Reuse existing UI primitives and patterns before adding new abstractions.
- Keep styling consistent with Tailwind and the current design language.

### Backend rules
- Prefer **Supabase-aligned backend design** when backend work is needed.
- Think in terms of schema, validation, queries, and RLS where applicable.
- Keep data access and validation explicit and reviewable.

### Security rules
- Never hardcode secrets.
- Respect environment variable boundaries.
- Consider auth, authorization, security headers, and safe data handling in backend and deployment work.
- Prefer safe defaults over convenience shortcuts.


## Project Structure

### Important folders

- `src/app/` — Next.js App Router pages and layouts
- `src/components/` — application components
- `src/components/ui/` — shadcn/ui components; reuse these first
- `src/hooks/` — custom React hooks
- `src/lib/` — shared utilities such as `utils.ts` and Supabase helpers
- `features/` — feature specs and feature tracking
- `docs/` — PRD, architecture, and production documentation


## Development Workflow

### 1. Requirements
A feature starts as a specification in `features/PROJ-X-name.md`.

### 2. Architecture
Architecture and technical approach are reviewed before implementation.  
High-level design belongs in `docs/ARCHITECTURE.md` and, where useful, inside the feature spec.

### 3. Frontend
Frontend implementation must follow:
- the feature spec
- the architecture
- the repository's Next.js + Tailwind + shadcn/ui conventions

### 4. Backend
Backend implementation must follow:
- the feature spec
- the architecture
- Supabase / PostgreSQL / Zod / RLS conventions where applicable

### 5. QA
Validate implementation against acceptance criteria and check for regressions.

### 6. Deploy
Deployment decisions must remain compatible with Vercel and production-ready setup guidance.


## Read Before Writing

Before making changes, always read:

1. `docs/PRD.md`
2. `docs/ARCHITECTURE.md`
3. `features/INDEX.md`
4. the relevant feature spec
5. the files you are about to modify


## Reuse Before Creating

Before creating new code:
- search for an existing component, hook, utility, route, or schema
- extend existing code when appropriate
- especially check `src/components/ui/` before creating custom UI


## Feature Tracking Rules

- Every feature must exist in `features/INDEX.md`
- Every feature must have exactly one spec file
- Keep feature status current
- Keep documentation in sync with implementation


## Commands

Use the existing repository scripts:

```bash
npm run dev
npm run build
npm run lint
npm run start
```

Do not invent commands that are not present in the project.


## Agent Behaviour

Agents must:
- be artifact-driven
- be stack-explicit
- preserve the repository's technology choices
- avoid speculative refactors
- prefer minimal, safe, reviewable changes

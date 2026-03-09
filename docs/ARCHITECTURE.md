# ARCHITECTURE.md

## System Overview

Describe the system at a high level.

This repository is optimized for:
- **Next.js 16 App Router**
- **TypeScript**
- **Tailwind CSS**
- **shadcn/ui**
- **Supabase** (optional backend)
- **PostgreSQL**
- **Zod**
- **Vercel**

Architecture decisions should align with these choices unless there is a documented reason not to.


## Architecture Principles

- prefer simple, reviewable solutions
- keep frontend, backend, and data concerns explicit
- reuse existing patterns before introducing new abstractions
- use stack-native capabilities where possible
- design for secure defaults
- keep deployment compatible with Vercel


## High-Level Building Blocks

### Frontend
- Next.js App Router
- server/client component split as appropriate
- Tailwind CSS for styling
- shadcn/ui for reusable UI primitives

### Backend
- Supabase-backed services when backend is required
- server actions / route handlers where appropriate
- Zod validation for runtime boundaries

### Data
- PostgreSQL via Supabase
- schema and access control should be explicit
- RLS should be considered where user-scoped data exists

### Deployment
- Vercel-hosted application
- environment variables managed outside source control


## Frontend Architecture

### App structure
Describe route groups, layouts, shared providers, and page boundaries.

### UI strategy
- Prefer existing `src/components/ui/` components first
- Use shadcn/ui as the base component system
- Create feature-specific components only when reusable primitives are insufficient

### State strategy
Document when to use:
- local component state
- Context API
- server-driven state
- form state with react-hook-form

### Styling strategy
- Tailwind CSS is the default styling method
- keep styling consistent with the repository design language
- avoid mixing multiple styling paradigms without strong reason


## Backend Architecture

Only fill the relevant sections if backend exists.

### Backend responsibilities
Describe which concerns live in:
- route handlers / server actions
- service helpers
- database access
- auth / authorization checks

### Validation
- Prefer Zod for request, payload, and boundary validation
- keep schemas close to their usage or in a shared validation area

### Auth and authorization
Describe:
- authentication model
- authorization rules
- any RLS requirements
- public vs protected routes


## Data Architecture

### Entities
List major entities / tables.

### Relationships
Describe key relationships.

### Access patterns
Describe expected reads, writes, filtering, and user ownership rules.

### Migration / schema notes
Document how schema changes should be handled in this project.


## External Integrations

List third-party services and why they exist.

Examples:
- Supabase
- analytics
- email provider
- payment provider


## Security Architecture

Document:
- secret management approach
- auth boundaries
- authorization strategy
- data exposure risks
- required headers or platform protections
- abuse prevention / rate limiting considerations


## Performance Considerations

Document expected hotspots and relevant strategies.

Examples:
- caching
- reducing client bundle size
- server-side rendering choices
- database query efficiency
- image optimization


## Deployment Architecture

### Platform
- Vercel

### Environments
Describe local / preview / production expectations.

### Environment Variables
List required environment variables by purpose, not secret value.

### Operational Readiness
Document:
- logging / monitoring
- error tracking
- rollback expectations
- deployment constraints


## Feature Mapping

Map architecture decisions back to features in `features/INDEX.md` and the corresponding feature specs.


## Open Technical Decisions

- decision
- decision

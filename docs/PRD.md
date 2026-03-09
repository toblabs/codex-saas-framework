# Product Requirements Document (PRD)

## Product Overview

### Product Name
`<project name>`

### Summary
Describe the product in 2–5 sentences.

### Product Vision
Describe the long-term vision and why this product should exist.


## Problem Statement

What user or business problem does the product solve?  
Why does this problem matter now?


## Target Users

### Primary users
Describe the most important users.

### Secondary users
Describe secondary or future user groups.


## Value Proposition

Why should users choose this product?  
What is the main value compared with alternatives or the status quo?


## Goals

### Business goals
- goal
- goal

### User goals
- goal
- goal

### Product goals
- goal
- goal


## Non-Goals

Explicitly list what the product is **not** trying to solve right now.


## MVP Scope

Describe the minimum viable product clearly.

### Included in MVP
- feature area
- feature area
- feature area

### Not included in MVP
- feature area
- feature area


## Core Product Areas

List the major functional areas that the product will contain.

Example:
- authentication
- dashboard
- data entry
- reporting
- settings


## User Journey Overview

Describe the main end-to-end journey a typical user takes through the product.


## Functional Themes / Epics

Break the product into major themes that can later become feature specs.

For each theme, provide:
- theme name
- short description
- why it matters


## UX / Frontend Constraints

This repository is optimized for:

- **Next.js App Router**
- **TypeScript**
- **Tailwind CSS**
- **shadcn/ui**

Implications:
- UI should favour reusable shadcn/ui primitives
- avoid unnecessary custom UI primitives
- design should be implementable with Tailwind and shadcn/ui patterns


## Backend / Data Constraints

When backend is required, this repository is optimized for:

- **Supabase**
- **PostgreSQL**
- **Zod**
- **Vercel-compatible architecture**

Implications:
- backend scope should fit Supabase capabilities where possible
- validation expectations should be explicit
- auth / authorization requirements should be stated clearly
- data access assumptions should be reviewable


## Security / Compliance Considerations

List requirements related to:
- authentication
- authorization
- data sensitivity
- secrets handling
- auditability
- abuse prevention


## Success Metrics

Define measurable signals of success.

Examples:
- activation rate
- task completion rate
- conversion
- response time
- retention


## Risks and Assumptions

### Risks
- risk
- risk

### Assumptions
- assumption
- assumption


## Open Questions

- question
- question


## Initial Feature Roadmap

List likely first features.  
These should later be broken into `features/PROJ-X-*.md`.

| Priority | Candidate Feature | Why |
|---|---|---|
| P1 | Example Feature | reason |
| P2 | Example Feature | reason |

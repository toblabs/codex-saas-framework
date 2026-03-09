---
name: deploy
description: Prepare or review a feature or repository state for deployment
---

# Deploy

## Purpose

Use this skill to prepare or review a feature or repository state for deployment.

Deployment work in this repository must remain compatible with:

- **Vercel**
- **Next.js**
- environment variable based configuration
- the repository's chosen stack and security model


## Read First

Before starting, read:

1. `AGENTS.md`
2. `docs/ARCHITECTURE.md`
3. the relevant feature spec
4. changed implementation files
5. any deployment-related config already present in the repo


## Deploy Rules

### Platform rules
- assume **Vercel** is the deployment target
- keep changes compatible with Next.js hosting expectations
- respect environment variable boundaries

### Security rules
- never expose secrets in source files
- verify required environment variables are documented
- consider auth, authorization, and public/private runtime boundaries

### Stack rules
- deployment decisions must fit the repository stack
- avoid infrastructure patterns that conflict with Vercel or the current app architecture

### Release readiness rules
- confirm feature status is accurate
- confirm docs reflect meaningful deployment-relevant changes
- identify blockers, not just code changes


## Process

### 1. Review deployment impact
Check whether the change affects:
- environment variables
- auth configuration
- database schema or policies
- storage or external integrations
- route/runtime behaviour
- build compatibility

### 2. Check production assumptions
Confirm:
- no secrets are hardcoded
- runtime boundaries are understood
- feature flags or config expectations are documented
- any required setup is visible to the team

### 3. Assess readiness
Classify the change as:
- ready
- ready with caveats
- blocked

Explain why.

### 4. Sync documentation
Update relevant docs when deployment requirements changed.


## Output Quality Bar

A good deploy review:
- is concrete
- identifies real production blockers
- checks security and config boundaries
- remains aligned with Vercel and the actual stack


## Do Not

- do not suggest unrelated infrastructure platforms without explicit instruction
- do not ignore environment variables or secret handling
- do not mark a feature deploy-ready if critical docs or config are missing

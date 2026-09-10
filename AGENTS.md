# AGENTS — Nobriê Workspace

## Role
This file is the router for the Nobriê Context Operating System. It is not the knowledge base.

## Scope
This repository is exclusively for Nobriê. Do not import or infer information from IBBX or unrelated projects.

## Core behavior
- Never invent Nobriê facts.
- Use progressive disclosure and load the minimum sufficient context.
- Prefer canonical, recently verified sources.
- Keep current state separate from decisions, knowledge, tasks, references, artifacts, and history.
- Preserve superseded decisions and provenance.
- Treat historical Ads metrics as historical unless freshly verified.
- Keep secrets out of Git.
- Do not turn a single observation into a permanent rule.

## Routing
Start with `CONTEXT.md`, then route by task:
- Brand/product → `context/brand.md`, `context/product.md`, relevant profile/workflow
- Strategy → `context/business.md`, `profiles/strategy.md`, strategy workflow
- Creative/content → brand + product + relevant creative/marketing profile + workflow
- Ads → `profiles/ads.md` + Ads/tracking workflow + current state
- Shopify → ecommerce/development profile + Shopify workflow + current store state
- Integrations/logistics → ecommerce/operations profile + relevant integration workflow + current state

## Context packet
For execution, assemble only:
`GLOBAL RULES + PROJECT CONTEXT + CURRENT STATE + PROFILE + WORKFLOW + RELEVANT DECISIONS + RELEVANT REFERENCES + RELEVANT MEMORY`.

## Canonical sources
- Project map: `CONTEXT.md`
- Current operational state: `WORKSPACE_STATE.md`
- Strategy roadmap: `ROADMAP.md`
- Decisions: `DECISIONS.md`
- Unresolved conflicts: `CONFLICTS.md`
- Stable brand/product/business knowledge: `context/`
- Domain operating rules: `profiles/`
- Task procedures: `workflows/`
- Durable reusable knowledge: `memory/`
- Historical evidence: `archive/` and `artifacts/`

## Synchronization
After meaningful work, follow `commands/workspace-update.md`. A commit alone is not a workspace update.

## Verification
Never claim `WORKSPACE SYNCED` without checking the resulting canonical files and repository state.

# Nobriê Context Operating System

This repository is the persistent, versioned workspace for Nobriê. It uses Context Engineering, ICM, Progressive Context Disclosure, Single Source of Truth, context routing, structured memory, explicit decisions, and Git persistence.

## Start here
1. `AGENTS.md` — router and operating contract
2. `CONTEXT.md` — workspace map and task routing
3. `WORKSPACE_STATE.md` — current operational reality
4. Load only the profile/workflow/references needed for the task

## Canonical architecture
- `context/` — stable Nobriê knowledge
- `profiles/` — domain/task context
- `workflows/` — execution procedures
- `references/` — technical/reference evidence
- `memory/` — durable reusable knowledge
- `DECISIONS.md` — decisions
- `CONFLICTS.md` — unresolved conflicts
- `TASKS.md` — executable current tasks
- `ROADMAP.md` — strategic fronts
- `artifacts/` — prior work products
- `archive/` — historical context
- `_config/` — global operating policies

## Context packet
`GLOBAL RULES + PROJECT CONTEXT + CURRENT STATE + PROFILE + WORKFLOW + RELEVANT DECISIONS + RELEVANT REFERENCES + RELEVANT MEMORY`.

## Synchronization
Use `/workspace-update` to consolidate meaningful session changes. It is not synonymous with creating a Git commit.

## Architecture principle
Do not maximize context volume. Maximize the probability that the right context reaches the right model at the right moment for the right task.

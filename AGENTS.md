# AGENTS — Nobrie Workspace

## Purpose
This file is the workspace router. It defines how an AI agent must navigate, retrieve context, execute work, and persist meaningful changes in this repository.

## Core principles
- Treat the repository as the persistent, versioned workspace for Nobrie.
- Use progressive context disclosure: start here, then load only the context required for the task.
- Prefer canonical sources over duplicated summaries.
- Separate stable knowledge, current operational state, decisions, tasks, outputs, and history.
- Never invent missing Nobrie facts. Mark assumptions explicitly.
- Current state takes priority over historical information.
- Do not ingest the whole repository indiscriminately.
- Do not treat generated outputs as permanent knowledge unless explicitly promoted.
- Preserve provenance and traceability.

## Navigation order
1. `AGENTS.md`
2. `CONTEXT.md`
3. Relevant project under `projects/`
4. Relevant stage under that project, when applicable
5. Current state (`STATUS.md`, `TASKS.md`, `WORKSPACE_STATE.md`)
6. Relevant decisions (`DECISIONS.md`)
7. Relevant references under the project or `shared/`
8. Specific files required by the task

## Canonical locations
- Global rules: `_config/`
- Workspace map: `CONTEXT.md`
- Global current state: `WORKSPACE_STATE.md`
- Project context/state/tasks/decisions: `projects/<project>/`
- Durable memory: `memory/`
- Cross-project references: `shared/`
- Unprocessed input: `inbox/`
- Reusable procedures: `commands/`
- Templates: `templates/`
- Working outputs: `projects/<project>/output/`
- Historical material: `archive/` or project `archive/`

## Execution protocol
Before acting, identify the task domain and load the minimum sufficient context. After meaningful work, determine whether persistent information changed. If it did, synchronize the canonical files using the workflow in `commands/workspace-update.md`.

## Conflict protocol
When sources conflict:
1. Prefer the canonical operational source.
2. Prefer newer confirmed information over older information.
3. Do not silently overwrite a meaningful prior decision.
4. Record a superseding decision when appropriate.
5. Mark unresolved uncertainty explicitly.

## Safety and scope
- Projects are isolated by default; do not leak context between projects without justification.
- Do not expose secrets, credentials, personal data, or sensitive operational information unnecessarily.
- Do not make destructive structural changes without explicit justification.
- Do not delete historical knowledge merely because it is no longer current; archive or supersede it.

## Session continuity
A new session must be able to reconstruct the relevant working context from repository files alone. Conversation history is supplementary, not the system of record.

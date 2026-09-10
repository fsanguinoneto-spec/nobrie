# Nobrie Workspace

Persistent AI workspace for Nobrie, designed around Context Engineering, progressive disclosure, canonical sources, operational-state separation, memory governance, and Git-based versioning.

## How to use
Read `AGENTS.md` first. Then use `CONTEXT.md` to route to the minimum context needed for the task.

## Architecture
- `AGENTS.md` — agent router and operating contract
- `CONTEXT.md` — global workspace map
- `WORKSPACE_STATE.md` — current global state
- `CHANGELOG.md` — meaningful workspace changes
- `_config/` — global policies
- `projects/` — isolated project workspaces
- `memory/` — durable memory by nature
- `shared/` — cross-project references/knowledge
- `inbox/` — unprocessed source material
- `commands/` — repeatable workspace procedures
- `templates/` — reusable document structures
- `archive/` — historical material

Nobrie-specific knowledge is intentionally not assumed until source material is ingested and validated.

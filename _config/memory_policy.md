# Memory Policy

Classify information before persisting it as durable memory.

Use these memory areas by nature:
- `memory/core/` — stable foundational knowledge
- `memory/entities/` — durable entity facts
- `memory/decisions/` — durable decision knowledge when appropriate
- `memory/episodic/` — meaningful events or sessions
- `memory/summaries/` — curated summaries
- `memory/archive/` — retired memory

Do not promote every conversation detail. Persist information when it is stable, repeatedly useful, explicitly important, or required for continuity. Avoid semantic duplication; maintain one canonical source for each operational fact.

# Operations Profile

## Scope
Operational integrations, order flow, fiscal/logistics state, diagnostics, and controlled consequential actions.

## Current logistics status
The Yampi/Bling/Frenet integration is considered operationally complete, with Bling ticket `#5708717` as the only recorded non-blocking external limitation.

## Safety
Do not mass-reprocess history, generate real labels unnecessarily, issue NF-e only for testing, create unnecessary financial test transactions, alter authorized-NF-e orders merely to experiment, or persist credentials/secrets.

Prefer native fixes over middleware/workarounds while the Bling ticket is pending.

# Logistics Debug Workflow

## Current status
The logistics integration is operationally complete. The remaining recorded limitation is Bling ticket `#5708717`, which concerns automatic matching of the logistics ID to `Frenet Nobriê → J&T Standard`.

## Recorded findings
- Tested aliases `TRANSPORTADORA` and `Transportadora`.
- Tested ID `60451412`.
- Yampi exposes separate fields `shipment_service=TRANSPORTADORA` and `shipment_service_id=Transportadora`.
- Yampi stated these fields belong to its general modality API and should not be changed specifically for Bling.
- Bling owns the open ticket and the issue is non-blocking because Frenet imports orders directly from Yampi.

## Pending validation
When Bling reports a fix, create a new untouched order and verify automatic selection of `Frenet Nobriê → J&T Standard`. Only then close the limitation.

## Do not
Do not create an API/middleware/n8n/script workaround or artificial Yampi change while the native solution remains pending.

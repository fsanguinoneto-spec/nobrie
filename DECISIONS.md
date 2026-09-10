# Nobriê Decisions

## D-001 — Meta Purchase canonical origin
- Date: recorded in source material; exact date not provided
- Status: CONFIRMED
- Decision: Yampi CAPI is the current canonical source for Meta Purchase from checkout.
- Reason: duplicate Purchase from Yampi CAPI + Meta browser Purchase was identified; `[Stape] Meta - Purchase` in GTM Web was paused and the correction was operationally confirmed.
- Guardrail: do not reactivate a second Purchase origin without investigating deduplication.

## D-002 — Yampi as final order source for Frenet
- Date: recorded in source material; exact date not provided
- Status: CONFIRMED
- Decision: Frenet currently imports orders directly from Yampi; Bling remains fiscal/NF-e layer.
- Reason: Yampi → Frenet was validated to import the NF-e access key and preserve Frenet → Yampi tracking return.
- Supersedes: the earlier configuration that had disabled direct Yampi → Frenet order import.

## D-003 — Bling ticket #5708717 ownership
- Date: recorded in source material; exact date not provided
- Status: CONFIRMED / PENDING EXTERNAL
- Decision: leave the logistics-ID matching issue with Bling and prefer the native fix.
- Impact: non-blocking because Frenet imports orders from Yampi.
- Rule: do not create workaround via API, middleware, n8n, script, or artificial Yampi changes while native resolution is pending.

## D-004 — Commercial truth for price/discount
- Date: recorded in source material; exact date not provided
- Status: CONFIRMED
- Decision: Yampi remains the commercial truth for price and discount values.
- Consequence: do not create artificial fixed discounts in Bling to correct commercial-value discrepancies.

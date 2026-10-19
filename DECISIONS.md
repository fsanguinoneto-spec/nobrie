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


## D-005 — Google Ads planning baseline
- Date: 2026-10-19
- Status: CONFIRMED BY USER
- Decision: For campaign planning, treat Merchant Center as configured and tracking as resolved. Do not reopen either workstream without new evidence of a problem.
- Guardrail: Confirm product/feed eligibility before product campaigns; monitor real attributed purchases after launch without rebuilding the validated tracking stack by default.

## D-006 — Google Ads daily budget
- Date: 2026-10-19
- Status: CONFIRMED BY USER
- Decision: Plan around a total average daily Google Ads budget of R$300 across campaigns, not R$300 per campaign.
- Planning equivalent: approximately R$9,000 over 30 days; actual daily spend may fluctuate under Google Ads billing rules.
- Guardrail: Allocate the total budget based on the agreed campaign architecture and evidence; do not treat the initial split as permanently fixed.


## D-007 — Initial Google Ads campaign architecture and budget
- Date: 2026-10-19
- Status: CONFIRMED BY USER
- Decision: Start with three campaigns and a total average daily budget of R$130: Performance Max R$100/day, Demand Gen R$20/day, and brand-protection Search R$10/day.
- Planning equivalent: approximately R$3,900 over 30 days; actual daily spend may fluctuate under Google Ads billing rules.
- Strategy: use one Performance Max campaign with relevant available audience signals, including eligible Analytics remarketing audiences and customer data where available. Do not activate the new-customer optimization setting at initial launch unless new evidence supports it.
- Search scope: brand protection only; do not initially bid on expensive generic terms such as “camisa polo” or “camisa polo masculina”.
- YouTube: no separate YouTube campaign at launch; Demand Gen is the limited demand-generation test.
- Guardrail: this records the approved plan, not a claim that live campaigns have been created or changed. Check feed/product eligibility and campaign setup before launch.

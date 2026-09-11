# Google Ads Workflow — Nobriê

## Scope
This workflow is exclusively for Google Ads at Nobriê. It is distinct from the broader Ads profile and should be loaded only for Google Ads work.

## Operating principle
Build Google Ads from the ground up. Existing account data is not a strategic baseline when tracking/history is insufficient. Historical material may be retained as evidence, but must not silently become strategy, benchmark, targeting, budget, bidding, campaign structure, or performance assumptions.

## Context discipline
Use progressive disclosure and minimum sufficient context. For Google Ads work, assemble only the relevant global rules, Nobriê context, current state, this workflow, relevant decisions/references/memory, and task-specific evidence. Do not load unrelated Meta Ads history merely because it exists in the Ads profile.

## Evidence before action
Never infer a root cause from a Google Ads status, alert, zero conversions, or automated recommendation alone. Before changing configuration, classify the evidence across separate layers:
1. Configuration — what conversion/action/account setting is defined.
2. Implementation — whether the expected tag/event is actually implemented.
3. Reception — whether Google Ads can detect/receive the event.
4. Attribution — whether a real event can be attributed to eligible Google Ads interaction.
5. Performance — whether traffic/conversions produce acceptable business results.

Do not treat a problem in one layer as proof of a problem in another.

## Conversion diagnostic gate
For conversion issues, follow:
`IDENTIFY ACTION → READ STATUS → DO NOT INFER CAUSE → CHECK CONFIGURATION → CHECK IMPLEMENTATION → TEST → CONFIRM RECEPTION → SEPARATE ATTRIBUTION FROM TECHNICAL VALIDATION → DECIDE KEEP/CORRECT/RECREATE`.

A status such as Inactive, Unverified, Needs attention, or similar is a diagnostic signal, not by itself a root-cause finding. Zero recorded conversions are not, by themselves, proof that tracking is broken. Use the platform's diagnostic/testing tools when appropriate, including Tag Assistant, without making unnecessary configuration changes first.

## Validated infrastructure guardrail
Tracking/configuration that was previously implemented and tested is treated as `VALIDATED` until new evidence contradicts it. Do not recreate, delete, or modify validated Google tags/conversion infrastructure solely because a dashboard status is concerning.

## Tracking vs performance
Always distinguish:
- Tracking health: whether events are technically implemented, detected, and received.
- Attribution: whether conversions are credited to Google Ads.
- Performance: whether Google Ads actually generates economically viable business results.

A technically valid tracking system can legitimately show zero Google Ads conversions when there is insufficient eligible Google Ads conversion activity. Conversely, broken tracking can make performance unknowable.

## Historical data policy
The recorded Google Ads account history is sparse and not a reliable strategic baseline. The only durable historical observation currently relevant to this workflow is: the provided latest 30-day campaign report recorded 0 conversions despite spend. Treat this only as a historical diagnostic fact. Do not infer from it that Google Ads cannot sell, that prior campaigns were poorly structured, or that tracking was necessarily broken.

The account also lacks a usable product-performance history for this workflow because the Merchant Center was disconnected, preventing the requested Products export. Do not fabricate product history or substitute unrelated data.

## Build-from-zero rule
The ideal Google Ads architecture must be designed from current business economics, product/feed availability, tracking validity, commercial truth, campaign objectives, and fresh evidence—not inherited from the old campaign structure.

## Merchant Center dependency
Product-based campaign architecture (Shopping/PMax with products) must wait for a valid Merchant Center/feed foundation. A disconnected Merchant Center is a current dependency/blocker, not a reason to invent product data.

## Decision discipline
Every meaningful recommendation must state the evidence supporting it. Record confirmed facts separately from assumptions, hypotheses, historical observations, and deprecated/superseded information. Never turn a single observation into a permanent rule.

## Step sequence
Work one step at a time. Do not jump from diagnosis to campaign creation. The workflow should progress from foundation/measurement → account/feed readiness → architecture → campaign construction → controlled launch → measurement → optimization → experiments → durable learnings.

## Current known Google Ads context
- No native Google Ads integration is available in the connected workspace, so history must be obtained through exports or direct platform evidence when needed.
- Existing 30-day report: 0 recorded conversions.
- Merchant Center: currently disconnected; product export unavailable.
- Google Ads conversion `Compra - SS`: currently shown in Google Ads as a Principal website conversion with manual event source and Inactive status; this status is not, by itself, proof of broken tracking.
- Google tags/tracking infrastructure had previously been implemented and tested according to the Nobriê tracking workflow; do not overwrite that state without contradictory evidence.

## Anti-duplication / attribution guardrail
Do not create additional Purchase sources merely because a Google Ads conversion is inactive. First map the existing event path and identifiers, then validate whether the Google Ads action receives the intended event. Do not disturb the canonical Meta Purchase architecture when working on Google Ads.

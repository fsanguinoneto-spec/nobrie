# Google Ads Workflow — Nobriê

## Scope
This workflow is exclusively for Google Ads at Nobriê. It is distinct from the broader Ads profile and should be loaded only for Google Ads work.

## Operating principle
Build Google Ads from the ground up. Existing account data is not a strategic baseline when tracking/history is insufficient. Historical material may be retained as evidence, but must not silently become strategy, benchmark, targeting, budget, bidding, campaign structure, or performance assumptions.

## Context discipline
Use progressive disclosure and minimum sufficient context. For Google Ads work, assemble only the relevant global rules, Nobriê context, current state, this workflow, relevant decisions/references/memory, and task-specific evidence. Do not load unrelated Meta Ads history merely because it exists in the Ads profile.

## Infrastructure baseline
The Nobriê Shopify + Yampi + GTM Web + sGTM/Stape + Google tracking infrastructure has already been implemented and tested outside this workflow. Treat the integration/tagging layer as `VALIDATED` unless new evidence contradicts that validation. Normal Google Ads operations must not restart or redesign this infrastructure.

The infrastructure remains documented here for auditability, troubleshooting, and understanding of event flow. When a new issue appears, diagnose the affected layer and make the minimum necessary correction rather than rebuilding validated components.

### Reference architecture
- Shopify / `www.nobrie.com` is the main storefront/web event source.
- GTM Web is the web collection layer.
- sGTM/Stape is the server-side processing/forwarding layer.
- Yampi is the checkout environment at `seguro.nobrie.com` and has its own checkout/event layer.
- Google Ads is the advertising destination for its conversion actions.

Known non-secret identifiers remain in the canonical tracking reference; secrets and credentials must never be stored here.

## Shopify + Yampi event ownership
Shopify and Yampi are distinct environments and must not be treated as a single Purchase source by default.

For every conversion event, especially Purchase, identify before changing anything:
`SOURCE → SENDER → DESTINATION → EVENT → IDENTIFIER → DEDUPLICATION RULE`.

Do not assume that a Yampi event, a GTM Web event, a Stape/sGTM event, and a Google Ads conversion are automatically the same event merely because they represent the same business action.

## Conversion diagnostic gate
For conversion issues, follow:
`IDENTIFY ACTION → READ STATUS → DO NOT INFER CAUSE → CHECK CONFIGURATION → CHECK IMPLEMENTATION → TEST → CONFIRM RECEPTION → SEPARATE TECHNICAL VALIDATION FROM ATTRIBUTION → DECIDE KEEP/CORRECT/RECREATE`.

A status such as Inactive, Unverified, Needs attention, Configuração incorreta, or similar is a diagnostic signal, not by itself a complete root-cause finding. Zero recorded conversions are not, by themselves, proof that tracking is broken.

The diagnosis must distinguish:
1. Configuration — what conversion/action/account setting is defined.
2. Implementation — whether the expected tag/event is implemented.
3. Reception — whether Google Ads can detect/receive the event.
4. Attribution — whether a real event can be attributed to an eligible Google Ads interaction.
5. Performance — whether the resulting traffic/conversions produce acceptable business results.

Do not treat a problem in one layer as proof of a problem in another.

## Evidence before action
Never infer a root cause from a dashboard status, alert, zero conversions, or automated recommendation alone.

Before modifying Google Ads or tracking infrastructure:
- collect the specific evidence supporting the suspected problem;
- identify the affected layer;
- compare the observed state with the previously validated implementation;
- determine whether the evidence contradicts the current canonical state;
- apply only the minimum correction supported by the evidence;
- test the correction before declaring the issue resolved.

Do not recreate a conversion or add a second event source simply because an existing conversion is inactive.

## Validated infrastructure guardrail
Tracking/configuration that was previously implemented and tested is treated as `VALIDATED` until new evidence contradicts it.

Therefore:
- do not recreate validated Google tags without evidence;
- do not delete validated tags/conversions because of a dashboard status alone;
- do not create duplicate Purchase sources to make a status change;
- do not alter the canonical Meta Purchase architecture while working on Google Ads unless a separate, explicit diagnosis requires it.

## Technical validation vs definitive validation
Technical tests can establish that the intended event is implemented and can be detected or received. They do not, by themselves, prove that Google Ads attribution works end-to-end.

The definitive Google Ads conversion validation gate is reached only after a **real conversion is attributed to Google Ads** and the full chain is confirmed.

Until then, use the state:
`TECHNICALLY VALIDATED / GOOGLE ADS ATTRIBUTION NOT YET PROVEN`.

A successful Tag Assistant/GTM test does not equal a real attributed Google Ads conversion. Do not claim end-to-end attribution validation before the first real attributed conversion.

## Tracking, UTM attribution, and commercial truth
Google Ads conversion tracking and UTM-based commercial attribution are complementary and must not be conflated.

### Google Ads conversion tracking
Used to measure and optimize Google Ads against its configured conversion actions.

### UTM attribution
UTM parameters are attached to the advertising destination URL, not to the sale itself. They identify traffic origin and campaign context and should be preserved through the customer journey as supported by the platform architecture.

At minimum, the workflow should account for the preservation and availability of relevant campaign/source parameters from:
`Google Ads click → Shopify → Yampi checkout → order/commercial record`.

The workflow must verify, rather than assume, how Yampi and Shopify preserve, expose, and associate UTM parameters with the eventual order.

### Commercial truth
For performance analysis, compare:
- Google Ads attributed conversions;
- UTM/source information preserved in Shopify/Yampi;
- real orders;
- real revenue;
- other relevant platform attribution.

Do not use Google Ads as the sole commercial truth.

## Anti-duplication guardrail
Never install multiple measurement paths for the same Purchase without an explicit event-ownership and deduplication design.

Before adding any Purchase implementation, map the existing paths across:
`Yampi → GTM Web → sGTM/Stape → Google Ads`.

A configuration such as:
`Yampi Purchase + GTM Google Ads Purchase + Stape Google Ads Purchase`
must not be created merely for redundancy. Determine which source is canonical for each destination and how duplicate events are prevented.

## Historical data policy
The recorded Google Ads account history is sparse and not a reliable strategic baseline. The only durable historical observation currently relevant to this workflow is: the provided latest 30-day campaign report recorded 0 conversions despite spend. Treat this only as a historical diagnostic fact.

Do not infer from it that Google Ads cannot sell, that prior campaigns were poorly structured, that Search/Shopping/PMax were inherently unsuitable, or that tracking was necessarily broken.

The account also lacks a usable product-performance history for this workflow because the Merchant Center was disconnected, preventing the requested Products export. Do not fabricate product history or substitute unrelated data.

## Build-from-zero rule
The ideal Google Ads architecture must be designed from current business economics, product/feed availability, tracking validity, commercial truth, campaign objectives, and fresh evidence—not inherited from the old campaign structure.

## Merchant Center dependency
Product-based campaign architecture must wait for a valid Merchant Center/feed foundation.

A disconnected Merchant Center is a current dependency/blocker, not a reason to invent product data or reuse unsupported historical product assumptions.

## Campaign readiness gate
Do not create or launch campaigns until the required foundation is sufficiently ready:
`TRACKING FOUNDATION → CONVERSION FOUNDATION → UTM/COMMERCIAL ATTRIBUTION VALIDATION → MERCHANT CENTER/FEED READINESS → ACCOUNT/OBJECTIVE DESIGN → CAMPAIGN ARCHITECTURE → CONTROLLED LAUNCH`.

The workflow remains step-by-step. Do not jump from a tracking diagnosis directly into campaign construction.

## Decision discipline
Every meaningful recommendation must state the evidence supporting it. Record confirmed facts separately from assumptions, hypotheses, historical observations, and deprecated/superseded information. Never turn a single observation into a permanent rule.

## Step sequence
Work one step at a time. The workflow should progress from foundation/measurement → account/feed readiness → architecture → campaign construction → controlled launch → measurement → optimization → experiments → durable learnings.

## Current known Google Ads context
- No native Google Ads integration is available in the connected workspace, so history must be obtained through exports or direct platform evidence when needed.
- Existing 30-day report: 0 recorded conversions; retained only as historical diagnostic evidence.
- Merchant Center: currently disconnected; product export unavailable.
- Google Ads conversion `Compra - SS`: currently shown in Google Ads as a Principal website conversion with manual event source and Inactive status; the status alone is not sufficient to diagnose the implementation.
- Google tags/tracking infrastructure was previously implemented and tested according to the Nobriê tracking work; treat that infrastructure as `VALIDATED` until contradictory evidence appears.

## Infrastructure troubleshooting rule
When a Google Ads issue is detected, do not restart the entire tracking stack. Identify the affected layer first:
`Google Ads configuration → tag/event implementation → GTM Web → sGTM/Stape → Yampi → Shopify → attribution/commercial record`.

Then validate the smallest relevant segment and correct only the confirmed defect.

## /workspace-update discipline
When meaningful Google Ads work changes durable knowledge, state, task, decision, reference, memory, or architecture, follow the repository `/workspace-update` procedure. Do not claim a workspace synchronization merely because a commit was created.

## Scope boundary
This workflow contains only Google Ads-relevant context and procedures. Broader Nobriê rules remain governed by the global workspace architecture (`AGENTS.md`, `CONTEXT.md`, `WORKSPACE_STATE.md`, `DECISIONS.md`, and related canonical sources). Do not duplicate those global rules here beyond what is necessary for Google Ads operation.

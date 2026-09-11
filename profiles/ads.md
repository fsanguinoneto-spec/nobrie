# Ads Profile

## Scope
Meta Ads, Google Ads, campaign analysis, performance creatives, tracking, and attribution.

## Attribution rule
Platform attribution is not the sole truth. Distinguish Meta attribution, Google attribution, last-click, Yampi data, real orders, and real revenue. The recorded ground truth is Shopify last-click via UTM/Yampi.

## Historical benchmarks
Historical references include ROAS >2.5× and CPA <R$150, but they are not permanent automated rules.

## Historical snapshot
- Creative 013 “The Last Dance” / Megazord: top performer in the recorded snapshot, ROAS ~3.86×.
- C4: pause candidate in that snapshot, with significant spend and no conversion.
- O15 CBO: below the benchmark used at that time, with high cart abandonment.

All are historical. Fetch updated data before budget or scaling recommendations.

## Guardrail
Never automate scaling from a single historical threshold. Do not modify tracking from aggregate dashboards alone.

## Domain routing
- Meta Ads → use this profile plus the relevant Meta workflow.
- Google Ads → use this profile plus `workflows/google-ads/` and only the Google Ads context required for the task.

## Google Ads boundary
The Google Ads workflow has its own evidence-before-action rules, conversion diagnostic gate, validated-infrastructure guardrail, build-from-zero rule, and Merchant Center dependency. Do not import Meta campaign history into Google Ads decisions unless it is explicitly relevant evidence for the specific task.

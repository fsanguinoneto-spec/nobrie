# Changelog

Important structural and operational changes only.

## 2026-09-11
- Added a dedicated Google Ads workflow with minimum-sufficient-context routing.
- Added evidence-before-action rules that separate configuration, implementation, reception, attribution, and performance diagnostics.
- Added a conversion diagnostic gate and a validated-infrastructure guardrail to prevent premature recreation or modification of working tracking.
- Established that Google Ads is being rebuilt from zero; the sparse 30-day report with zero recorded conversions is historical diagnostic evidence only.
- Recorded Merchant Center disconnection as a current dependency for product-based Google Ads work; product history must not be fabricated.
- Isolated Google Ads context from unrelated Meta Ads history unless explicitly relevant to the task.
- Formalized the Shopify + Yampi + GTM Web + sGTM/Stape + Google tracking layer as a previously implemented and tested infrastructure baseline.
- Added definitive validation rule: end-to-end Google Ads conversion tracking remains unproven until a real conversion is attributed to Google Ads.
- Added UTM and commercial attribution validation as a layer distinct from Google Ads conversion tracking.
- Added event ownership and anti-duplication rules across Shopify, Yampi, GTM Web, sGTM/Stape, and Google Ads.

## 2026-09-10
- Initialized the Nobriê AI workspace architecture.
- Ingested the provided Nobriê workspace specification.
- Established canonical brand, product, business, state, decision, conflict, roadmap, and task sources.
- Added marketing, creative, Ads, ecommerce, operations, development, and strategy routing profiles.
- Added content, creative analysis/generation, video editing, Ads analysis, tracking debug, Shopify development, ecommerce integration, and logistics debug workflows.
- Added canonical tracking and integration references.
- Preserved unresolved tagline conflict rather than selecting a version arbitrarily.
- Classified historical performance and integration findings as historical/contextual rather than permanent rules.
- Kept the architecture intentionally minimal where additional directories would have no current function.
- Updated current tracking state: AddToCart duplication is confirmed resolved.
- Updated current tracking state: ViewContent value-completeness issue is confirmed resolved.
- Closed the corresponding AddToCart and ViewContent tracking investigations while preserving them as historical context.

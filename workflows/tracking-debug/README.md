# Tracking Debug Workflow

## Purpose
Diagnose event and attribution issues without loading unrelated commerce/logistics context.

## Purchase
Canonical current Meta Purchase origin: Yampi CAPI. A second Purchase origin must not be reactivated without investigating deduplication.

## Recorded open investigations
- AddToCart duplication: source still needs isolation.
- ViewContent: prior observation of ~68% without value; dataLayer appeared correct, external origin needed investigation.
- Google Ads Purchase: verification pending.
- Checkout Data Tags: prior observation that tags were not reaching sGTM as expected; validate in Preview before calling corrected.

## Diagnostic chain
`browser → dataLayer → GTM Web → network → sGTM → destination`.

Do not modify tracking solely from aggregate dashboards.

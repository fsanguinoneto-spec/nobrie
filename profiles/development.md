# Development Profile

## Scope
Shopify theme work, tracking implementation, integrations, diagnostics, and technical changes.

## Shopify
- Storefront: `nobrie.com`
- LIVE theme: `187670888768`
- Draft/Horizon: `185977635136`

Never treat Draft as production.

## Technical guardrails
Use diagnostics before writes. Do not repeat full PUT operations against real orders by trial and error. Any future write must have a validated schema and operational justification.

For tracking, when possible validate the chain:
`browser → dataLayer → GTM Web → network → sGTM → destination`.

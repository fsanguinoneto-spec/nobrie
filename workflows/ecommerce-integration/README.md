# Ecommerce Integration Workflow

## Purpose
Maintain and diagnose the boundaries between Shopify, Yampi, Bling, Frenet, and J&T.

## Canonical responsibilities
- Shopify: storefront/catalog
- Yampi: commercial origin/checkout and Frenet order source
- Bling: fiscal/NF-e and fiscal order state
- Frenet: logistics/fulfillment/labels
- J&T Standard: carrier/service

## Canonical flow
`Yampi → Bling (fiscal/NF-e) → return fiscal/status → Yampi → Frenet → J&T → tracking → Yampi`.

## Freight quotation
Treat checkout freight quotation as separate from Yampi ↔ Frenet operational synchronization.

## Diagnostic discipline
Prefer native solutions. Validate schemas before writes. Do not change commercial fields in Yampi to compensate for downstream mapping unless explicitly justified and verified.

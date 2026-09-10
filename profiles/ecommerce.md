# Ecommerce Profile

## System responsibilities
- Shopify: storefront and catalog; not a competing order source for Bling/Frenet.
- Yampi: commercial origin and checkout; final order source used by Frenet.
- Bling: fiscal layer, NF-e, and operational/fiscal order state.
- Frenet: logistics, fulfillment, labels, carrier integration.
- J&T Standard: recorded carrier/service.

## Canonical logistics architecture
`Yampi → Bling (fiscal/NF-e) → return fiscal/status → Yampi → Frenet → J&T → tracking → Yampi`.

Frenet currently imports orders directly from Yampi. Bling remains essential for fiscal processing but is not the final logistics order source for Frenet.

## Important distinction
Freight quotation in checkout is separate from operational Yampi ↔ Frenet order synchronization.

## Commercial truth
Yampi is the commercial truth for price and discounts.

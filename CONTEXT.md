# Nobriê Workspace Context

## Workspace Purpose
This repository is the persistent, versioned Context Operating System for Nobriê. It is designed for continuity across AI sessions while keeping each task's context short, precise, relevant, and traceable.

## Scope
Nobriê only. Do not load or infer from IBBX or unrelated projects.

## Context Layers
- `context/` — stable Nobriê brand, product, and business knowledge
- `profiles/` — domain-specific operating rules used for routing
- `workflows/` — task procedures
- `WORKSPACE_STATE.md` — current operational reality
- `DECISIONS.md` — decision source of truth
- `CONFLICTS.md` — unresolved conflicts only
- `ROADMAP.md` — strategic fronts
- `references/` — technical/reference material
- `memory/` — durable reusable knowledge
- `artifacts/` — prior work products consulted only when needed
- `archive/` — historical material not loaded by default

## Current Context
Brand: Nobriê. Men's fashion positioned around old money / elite / premium. Main profile: `@nobrie.wear`. Strategic relationship with `@alejandro.tonin`.

Current canonical product: Camisa Polo Piquet Nobriê. See `context/product.md` for product details.

## Routing examples
- Creative analysis → brand + creative profile + creative-analysis workflow + validated references
- New ad → brand + product + marketing/creative + relevant Ads/creative workflow
- Google Ads → `profiles/ads.md` + `workflows/google-ads/` + only the relevant current tracking/business state and evidence
- AddToCart duplication → Ads + tracking-debug + current tracking state
- Bling issue → ecommerce + operations + ecommerce-integration/logistics-debug + current state + decision log
- Shopify work → ecommerce/development profile + Shopify workflow + current store state

## Context Packet
`GLOBAL RULES → PROJECT CONTEXT → CURRENT STATE → PROFILE → WORKFLOW → RELEVANT DECISIONS → RELEVANT REFERENCES → RELEVANT MEMORY`

## Current status
The Nobriê source material has been classified into canonical architecture. Dated/current operational claims must still be freshly verified before consequential changes. Google Ads is treated as a dedicated domain workflow with a from-zero strategic baseline, evidence-before-action diagnostics, and no automatic import of unrelated Meta Ads history.

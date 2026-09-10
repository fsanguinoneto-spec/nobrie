# Tracking Architecture Reference

Status: recorded architecture; verify operational state before modifying.

## Web
`Shopify / nobrie.com → GTM Web → Meta Pixel browser + Data Tags → sGTM at conv.nobrie.com → Meta CAPI`

## Checkout
`Yampi / seguro.nobrie.com → Yampi Conversion API → Meta`

Purchase from checkout is server-side. Pix should count when effectively paid.

## Non-secret identifiers
- Meta Pixel: `1145883260475396`
- GTM Web: `GTM-PFGXDLZL`
- sGTM: `GTM-W3GCZ395`
- GA4: `G-8015K9YHX1`
- Google Ads: `AW-18381698229`
- Custom Loader: `load.conv.nobrie.com`
- Server container: `conv.nobrie.com`

Never store tokens, API keys, cookies, CSRF tokens, passwords, credentials, or other secrets here.

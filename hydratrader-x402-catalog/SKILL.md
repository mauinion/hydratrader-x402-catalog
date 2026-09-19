---
name: hydratrader-x402-catalog
description: Use when an agent needs cheap pay-per-call text helpers, structured JSON extract from public text/URLs, or a cited research brief — paid in USDC on Base via x402 with no API key.
---

# CatalogBot x402 seller (hydratrader)

Base: `https://x402.hydratrader.ai`

Listed on [x402-list](https://x402-list.com/services/catalogbot?utm_source=badge&utm_medium=referral&utm_campaign=embed): ![CatalogBot listed on x402-list](https://x402-list.com/badge/catalogbot.svg)

Discover: `npx awal x402 bazaar search hydratrader` (or search summarize / structured extract / research brief).

## Routes (Base USDC, exact, no API key)

| Route | Price | When to use |
|-------|-------|-------------|
| `POST /v1/cheap-errand` | $0.01 | Summarize text. Classify sentiment. Rewrite. Extract keywords. Translate. Cheap agent glue for buyer-supplied text; returns JSON. |
| `POST /v1/structured-extract` | $0.03 | Extract structured JSON. JSON schema extract. Structured extract into YOUR schema from text or public URL. |
| `POST /v1/research-brief` | $0.08 | Research brief. Citations. Summarize research from the public web with key points and caveats. |

## Pay example

```bash
npx awal x402 pay https://x402.hydratrader.ai/v1/cheap-errand -X POST \
  -H 'content-type: application/json' \
  -d '{"task":"summarize","input":"..."}'
```

## Policy
Public sources only. No login scrape, no PII harvesting, no full-text copyright dumps.

---
name: cheap-agent-glue
description: Use when you need to summarize text, classify sentiment, rewrite, extract keywords, or translate buyer-supplied text via a cheap USDC pay-per-call on Base (x402, no API key).
---

# Cheap agent glue (x402)

Pay-per-call text helpers on Base USDC. No API key. Public text only.

**Endpoint:** `POST https://x402.hydratrader.ai/v1/cheap-errand` — **$0.01 USDC**

## When to use
- Summarize text
- Classify sentiment
- Rewrite / polish wording
- Extract keywords
- Translate short text

## Pay

```bash
npx awal x402 pay https://x402.hydratrader.ai/v1/cheap-errand -X POST \
  -H 'content-type: application/json' \
  -d '{"task":"summarize","input":"YOUR TEXT HERE"}'
```

Other `task` values: `rewrite`, `classify`, `extract_keywords`, `sentiment`, `translate`.

## Discover (optional)
`npx awal x402 bazaar search "summarize text"` or `hydratrader`

## Related
- Structured JSON extract: `POST /v1/structured-extract` ($0.03)
- Cited research brief: `POST /v1/research-brief` ($0.08)
- Catalog skill: `npx skills add mauinion/hydratrader-x402-catalog --skill hydratrader-x402-catalog`

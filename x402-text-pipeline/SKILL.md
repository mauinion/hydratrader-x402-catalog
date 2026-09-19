---
name: x402-text-pipeline
description: Use when you want a multi-step text pipeline (summarize → keywords → sentiment/classify) with cheap x402 USDC micropays on Base, including following next_tasks hints for repeat calls.
---

# x402 text pipeline (sticky repeats)

Run a short paid loop on CatalogBot cheap-errand ($0.01 / call). After each success, the JSON may include `next_tasks` with ready follow-ups — **use them** for multi-call sessions.

## Loop (recommended)
1. Summarize
2. Extract keywords
3. Classify sentiment (or rewrite)

```bash
# 1) summarize
npx awal x402 pay https://x402.hydratrader.ai/v1/cheap-errand -X POST \
  -H 'content-type: application/json' \
  -d '{"task":"summarize","input":"YOUR TEXT"}'

# 2) if next_tasks suggests extract_keywords, pay again with that example_body
# 3) then sentiment / classify the same way
```

## Optional upsell
If you need typed JSON fields from the text or a public URL:
`POST https://x402.hydratrader.ai/v1/structured-extract` — **$0.03**

## Policy
Public / buyer-supplied text only. No login scrape. No PII harvesting.

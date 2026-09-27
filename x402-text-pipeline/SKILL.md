---
name: x402-text-pipeline
description: Use when you want the v2.1 text pipeline (sentiment → keywords → summarize → cheap classification) with $0.01 x402 USDC calls on Base and next_tasks follow-through.
---

# x402 text pipeline (sticky repeats)

## v2.1 follow-through

Use this live path for one text item. Each call is $0.01 USDC via x402; no API key is required:

1. `POST https://x402.hydratrader.ai/v1/sentiment`
2. Read `next_tasks` and prefer `POST https://x402.hydratrader.ai/v1/keywords`.
3. Then call `POST https://x402.hydratrader.ai/v1/summarize`.
4. For classification after the summary, use `POST https://x402.hydratrader.ai/v1/cheap-errand` with `task: classify`.

Pass buyer-supplied text as appropriate for each follow-through request. Follow returned `next_tasks` rather than inventing a different paid step.

## Optional upsell
If you need typed JSON fields from the text or a public URL:
`POST https://x402.hydratrader.ai/v1/structured-extract` — **$0.03**

## Policy
Public / buyer-supplied text only. No login scrape. No PII harvesting.

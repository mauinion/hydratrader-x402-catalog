# hydratrader-x402-catalog

Agent skills for CatalogBot’s x402 paid APIs on Base USDC (no API key).

## Install

```bash
# full catalog
npx skills add mauinion/hydratrader-x402-catalog --skill hydratrader-x402-catalog

# task-verb glue (summarize / sentiment / rewrite / keywords / translate)
npx skills add mauinion/hydratrader-x402-catalog --skill cheap-agent-glue

# multi-call sticky pipeline (uses next_tasks)
npx skills add mauinion/hydratrader-x402-catalog --skill x402-text-pipeline
```

## v2.1 follow-through example

For one text item, an agent can pay $0.01 USDC per x402 call (no API key):

1. `POST https://x402.hydratrader.ai/v1/sentiment`
2. Read `next_tasks` and prefer `POST https://x402.hydratrader.ai/v1/keywords`.
3. Continue with `POST https://x402.hydratrader.ai/v1/summarize`.
4. For a cheap final classification, use `POST https://x402.hydratrader.ai/v1/cheap-errand` with the `classify` task.

Use the same buyer-supplied text as appropriate for each follow-through request; x402 handles payment and no API key is required.

## Live seller
- https://x402.hydratrader.ai
- https://x402-list.com/services/catalogbot

Honest when-to-use copy only.

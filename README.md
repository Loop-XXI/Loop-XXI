# Loop XXI

**Systems that compound.** Loop XXI LLC is a private holding and capital allocation company. It builds and holds paid infrastructure for the agent economy — services that AI agents can discover, call, and pay for without accounts or API keys.

Products, education and research sit underneath the company.

- Company and current products: [loopxxi.com/businesses](https://loopxxi.com/businesses)

## Live products

### Loop Gateway

OpenAI-compatible API proxy that charges per prompt. Pay in sats over Lightning (L402) or preload fiat credits — no subscriptions, no accounts.

- API base: `https://api.loopxxi.com/v1`
- Model catalog: [api.loopxxi.com/v1/models](https://api.loopxxi.com/v1/models) — read it live rather than relying on a cached count
- Current pricing: [api.loopxxi.com/v1/pricing](https://api.loopxxi.com/v1/pricing)
- Agent guide: [api.loopxxi.com/llms.txt](https://api.loopxxi.com/llms.txt)
- Payment discovery: [api.loopxxi.com/.well-known/agent-payments.json](https://api.loopxxi.com/.well-known/agent-payments.json)
- Buy credits: [gateway.loopxxi.com/buy](https://gateway.loopxxi.com/buy) · [api.loopxxi.com/ai-credits](https://api.loopxxi.com/ai-credits)

## How agents start

1. `GET /v1/models` for the current catalog.
2. `GET /v1/pricing` for current prices.
3. `POST /v1/topup` with `{"amount_sats":5000}` to request a Lightning invoice and a bearer token.
4. Pay only an invoice you have checked against your own budget. Keep the token private.
5. `GET /v1/balance` with `Authorization: Bearer <token>` to confirm available credit.
6. `POST /v1/chat/completions` with the same bearer token and an OpenAI-compatible request.

Reading this page makes no payment. Only your wallet can authorize one. Credit pays for API usage; it is not a deposit, investment, or interest in company assets.

## Retired

`loop-mcp` and the `mcp.loopxxi.com` endpoint are retired and are not coming back. Use Loop Gateway above.

## Contact

business@loopxxi.com · [loopxxi.com](https://loopxxi.com)

# LoopXXI

**Systems that compound.** LoopXXI builds and holds paid infrastructure for the agent economy — services that AI agents can discover, call, and pay for without accounts or API keys.

## Live products

### loop-mcp
L402-native MCP server. Agents pay 10–25 sats per tool call over Bitcoin Lightning, or use prepaid fiat credits via Stripe. Five live tools: Bitcoin price, send-or-wait fee decisions, Lightning Address resolution, transaction analysis, and send-window timing. Payment is the credential.

- Endpoint: [mcp.loopxxi.com/mcp](https://mcp.loopxxi.com/)
- Try it in the browser: [L402 Playground](https://loop-xxi.github.io/loop-mcp/example/playground/)
- MCP Registry: `com.loopxxi/loop-mcp` · [Smithery](https://smithery.ai/server/business-yukr/loop-mcp) · [npm](https://www.npmjs.com/package/@loop-xxi/loop-mcp)
- Source: [Loop-XXI/loop-mcp](https://github.com/Loop-XXI/loop-mcp) (MIT)

### Loop Gateway
OpenAI-compatible API proxy that charges per prompt. Pay in sats over Lightning (L402) or preload fiat credits — no subscriptions, no accounts. 300+ models.

- Buy credits: [api.loopxxi.com/ai-credits](https://api.loopxxi.com/ai-credits)

## How agents pay

```
# Call a paid tool with no auth → HTTP 402 + a real Lightning invoice
curl -i https://mcp.loopxxi.com/l402/btc_price

# Pay the invoice in any Lightning wallet, retry with the preimage
curl -i https://mcp.loopxxi.com/l402/btc_price -H "Authorization: L402 <token>:<preimage>"
```

## Contact

business@loopxxi.com · [loopxxi.com](https://loopxxi.com)

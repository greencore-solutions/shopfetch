# shopfetch

> Did your AI pick the right product? Give the product your AI chose (its name and size, or its barcode) and your country, or the receipt on your order confirmation. shopfetch checks it is the real thing — same product, same size, same pack — against the record for your country, and says Barcode verified only when it is, with what was verified, where, when and under which rules. Price and stock are never taken from the record. Free for shoppers.

Built and run by [wefetch](https://wefetch.ai/). This is the public connect kit, MIT. It holds no deploy code and no keys.

## Connect

- Endpoint: `https://shopfetch.ai/mcp` (MCP, streamable HTTP)
- Agent card: `https://shopfetch.ai/.well-known/agent-card.json` (copy in this repo, `agent-card.json`)
- For agents: https://shopfetch.ai/llms.txt
- Site: https://shopfetch.ai/
- Official MCP Registry: `ai.shopfetch/shopfetch` (`server.json` in this repo)

Any client that speaks streamable HTTP:

```json
{
  "url": "https://shopfetch.ai/mcp",
  "transport": "streamable-http"
}
```

Claude Code:

```bash
claude mcp add --transport http shopfetch https://shopfetch.ai/mcp
```

List the tools with `python examples/generic_mcp_client.py`.

## Tools

| Tool | What it does |
|---|---|
| `check_pick` | Did your AI pick the right product? |

Artificial intelligence makes mistakes. Check what matters.

# Slack

Search, read, and send Slack messages. Runtime injects `${SLACK_MCP_TOKEN}` — never commit secrets.

**Category:** Featured  
**Auth:** `oauth` via `SLACK_MCP_TOKEN`  
**Wired:** true

Account-owned auth stays product-side. `mcp.json` uses `${ENV}` placeholders only.

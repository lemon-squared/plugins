# Notion

Work with Notion pages, databases, and wikis via MCP. Runtime injects `${NOTION_TOKEN}` — never commit secrets.

**Category:** Featured  
**Auth:** `secret` via `NOTION_TOKEN`  
**Wired:** true

Account-owned auth stays product-side. `mcp.json` uses `${ENV}` placeholders only.

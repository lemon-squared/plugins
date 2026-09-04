# Gmail

Search, read, draft, and manage Gmail. Runtime injects `${GMAIL_OAUTH_TOKEN}` from account auth — never commit secrets.

**Category:** Featured  
**Auth:** `oauth` via `GMAIL_OAUTH_TOKEN`  
**Wired:** true

Account-owned auth stays product-side. `mcp.json` uses `${ENV}` placeholders only.

# Granola

Search Granola meeting notes and transcripts. Runtime injects `${GRANOLA_OAUTH_TOKEN}` — never commit secrets.

**Category:** Featured  
**Auth:** `oauth` via `GRANOLA_OAUTH_TOKEN`  
**Wired:** true

Account-owned auth stays product-side. `mcp.json` uses `${ENV}` placeholders only.

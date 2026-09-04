# Google Drive

Search, read, create, and share Google Drive files. Runtime injects `${GOOGLE_DRIVE_OAUTH_TOKEN}` — never commit secrets.

**Category:** Featured  
**Auth:** `oauth` via `GOOGLE_DRIVE_OAUTH_TOKEN`  
**Wired:** true

Account-owned auth stays product-side. `mcp.json` uses `${ENV}` placeholders only.

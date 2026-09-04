# Google Calendar

Search events and schedule meetings on Google Calendar. Runtime injects `${GOOGLE_CALENDAR_OAUTH_TOKEN}` — never commit secrets.

**Category:** Featured  
**Auth:** `oauth` via `GOOGLE_CALENDAR_OAUTH_TOKEN`  
**Wired:** true

Account-owned auth stays product-side. `mcp.json` uses `${ENV}` placeholders only.

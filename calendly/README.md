# Calendly

Check Calendly availability and manage bookings. Runtime injects `${CALENDLY_OAUTH_TOKEN}` — never commit secrets. Category stub.

**Category:** Scheduling  
**Auth:** `oauth` via `CALENDLY_OAUTH_TOKEN`  
**Wired:** false

Account-owned auth stays product-side. `mcp.json` uses `${ENV}` placeholders only.

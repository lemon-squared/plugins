# GitHub

Manage GitHub repos, issues, PRs, and Actions. Runtime injects `${GITHUB_TOKEN}` — never commit secrets. Stub until fully wired.

**Category:** Infrastructure  
**Auth:** `github_app` via `GITHUB_TOKEN`  
**Wired:** false

Account-owned auth stays product-side. `mcp.json` uses `${ENV}` placeholders only.

---
name: create-plugin-scaffold
description: Scaffold a new Runtime plugin directory with .runtime-plugin/plugin.json and optional mcp.json.
---

# Create Runtime plugin scaffold

## Steps

1. Create `<plugin-name>/` at the marketplace root.
2. Add `.runtime-plugin/plugin.json` with at least `name` (kebab-case). Recommended fields:
   - `displayName`, `version` (semver), `description`
   - `author`: `{ "name": "Runtime", "email": "plugins@lemonsquared.com" }`
   - `license`: `MIT`
   - `category`, `tags`, `keywords`
   - `mcpServers`: `"./mcp.json"` when shipping an MCP connector
   - Runtime extras: `authKind` (`oauth` | `secret` | `github_app`), `secretField`, `wired`
3. If MCP: add `mcp.json` with `${ENV}` placeholders only — never real secrets.
4. Add a short `README.md` documenting auth injection (account-owned, product-side).
5. Register in `.runtime-plugin/marketplace.json` with only:
   - Required: `name`, `source`
   - Optional: `description`, `minClientVersions`
   - Do **not** put `keywords`, `category`, or `tags` on marketplace entries.
6. Run `node scripts/validate.mjs` and fix any schema errors.

## Auth note

Runtime clients inject secrets from the signed-in account. Manifests and `mcp.json` stay templates.

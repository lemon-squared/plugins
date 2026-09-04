# Runtime plugins

Official Runtime plugin specification and marketplace: MCP connectors, skills, and agent tools.


Monorepo companion: [lemon-squared/Runtime-Monorepo](https://github.com/lemon-squared/Runtime-Monorepo).

## Plugins

| `name` | Plugin | Author | Category | Description |
|:-------|:-------|:-------|:---------|:------------|
| `gmail` | [Gmail](gmail/) | Runtime | Featured | Search, read, draft, and manage email. |
| `google-calendar` | [Google Calendar](google-calendar/) | Runtime | Featured | Search events and schedule meetings. |
| `google-drive` | [Google Drive](google-drive/) | Runtime | Featured | Search, read, create, and share files. |
| `granola` | [Granola](granola/) | Runtime | Featured | Search meeting notes and transcripts. |
| `notion` | [Notion](notion/) | Runtime | Featured | Skills and MCP for pages, databases, and wikis. |
| `slack` | [Slack](slack/) | Runtime | Featured | Search, read, and send Slack messages over MCP. |
| `github` | [GitHub](github/) | Runtime | Infrastructure | Manage repos, issues, pull requests, and Actions. |
| `todoist` | [Todoist](todoist/) | Runtime | Productivity | Create, find, and complete tasks and projects. |
| `calendly` | [Calendly](calendly/) | Runtime | Scheduling | Check availability and book, cancel, or reschedule. |
| `create-plugin` | [Create Plugin](create-plugin/) | Runtime | MCP | Scaffold and validate new Runtime agent plugins. |

Author values match each plugin's `plugin.json` `author.name` (`plugins@lemonsquared.com`).

## Repository structure

This is a multi-plugin marketplace repository. The root `.runtime-plugin/marketplace.json` lists all plugins, and each plugin has its own manifest:

```
plugins/
├── .runtime-plugin/
│   └── marketplace.json       # Marketplace manifest (lists all plugins)
├── schemas/
│   ├── marketplace.schema.json
│   └── plugin.schema.json
├── .github/workflows/validate-plugins.yml
├── scripts/validate.mjs
├── plugin-name/
│   ├── .runtime-plugin/
│   │   └── plugin.json        # Per-plugin manifest
│   ├── mcp.json               # MCP server template (${ENV} placeholders)
│   ├── README.md
│   └── assets/                # Optional logo / media
└── ...
```

## How Runtime clients consume this marketplace

1. Clients fetch `.runtime-plugin/marketplace.json` from this repository (or a pinned ref).
2. For each entry, they load `<source>/.runtime-plugin/plugin.json` and merge marketplace + plugin metadata (plugin wins on conflicts).
3. When `mcpServers` points at `./mcp.json`, the client loads that template and **injects account secrets** into `${ENV}` placeholders. Secrets never live in this repo.
4. Optional Runtime fields on the plugin manifest:
   - `authKind`: `oauth` | `secret` | `github_app`
   - `secretField`: env var name the account injects
   - `wired`: whether the MCP transport is verified for Runtime

Auth stays account-owned and product-side. Plugin authors only ship templates.

## Add a plugin

1. Copy an existing Featured plugin directory (e.g. `gmail/`) or use the [create-plugin](create-plugin/) skill.
2. Fill `.runtime-plugin/plugin.json` (`name`, `displayName`, `version`, `description`, `author`, `license`, `category`, `tags`, `mcpServers`, plus Runtime fields as needed).
3. Add `mcp.json` with `${ENV}` placeholders — **never commit real keys**.
4. Register the plugin in `.runtime-plugin/marketplace.json` with `name`, `source`, and optional `description` only.
5. Run validation locally:

```bash
npm install --no-save ajv ajv-formats
node scripts/validate.mjs
```

CI runs the same check on push/PR via `.github/workflows/validate-plugins.yml`.

## Schemas

JSON Schema (draft-07) definitions live under [`schemas/`](schemas/). They are Runtime-owned manifests adapted for `.runtime-plugin/` layout.

## Assets

Plugin logos live under each plugin's `assets/` directory (`logo` in `plugin.json`). Brand marks remain their respective owners'. Slack, Notion, and Granola keep `assets/.gitkeep` until official marks are available.

## License

MIT

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
| `ahrefs` | [Ahrefs](ahrefs/) | Runtime | Research | Research keywords, backlinks, rankings, and site health. |
| `amplemarket` | [Amplemarket](amplemarket/) | Runtime | Sales | Search people and companies, enrich leads, run sequences. |
| `ashby` | [Ashby](ashby/) | Runtime | Sales | Search candidates, prep interviews, and manage pipeline tasks. |
| `brevo` | [Brevo](brevo/) | Runtime | Sales | Manage contacts, email and SMS campaigns, and CRM deals. |
| `brex` | [Brex](brex/) | Runtime | Finance And Legal | Query expenses, receipts, bills, cards, and travel. |
| `circleback` | [Circleback](circleback/) | Runtime | Productivity | Search meetings, transcripts, action items, and emails. |
| `clay` | [Clay](clay/) | Runtime | Sales | Enrich people and companies, run AI research agents. |
| `coda` | [Coda](coda/) | Runtime | Documents And Files | Search docs, read pages, and update tables. |
| `craft` | [Craft](craft/) | Runtime | Documents And Files | Search, create, and update documents and daily notes. |
| `customer-io` | [Customer.io](customer-io/) | Runtime | Sales | Build campaigns, manage segments, and query people. |
| `docusign` | [Docusign](docusign/) | Runtime | Finance And Legal | Manage envelopes, templates, workflows, and agreements. |
| `fathom` | [Fathom](fathom/) | Runtime | Productivity | Search meetings and pull transcripts and summaries. |
| `fireflies` | [Fireflies](fireflies/) | Runtime | Productivity | Search meeting transcripts, summaries, and action items. |
| `godaddy` | [GoDaddy](godaddy/) | Runtime | Infrastructure | Brainstorm domain names and check availability. |
| `gong` | [Gong](gong/) | Runtime | Sales | Pull account summaries, deal insights, and call briefs. |
| `guru` | [Guru](guru/) | Runtime | Documents And Files | Search company knowledge and draft verified answers. |
| `hubspot` | [HubSpot](hubspot/) | Runtime | Sales | Search and update contacts, companies, deals, and tickets. |
| `intercom` | [Intercom](intercom/) | Runtime | Customer Support | Search conversations, contacts, and Help Center articles. |
| `jotform` | [Jotform](jotform/) | Runtime | Productivity | Create and edit forms, then read submissions. |
| `juicebox` | [Juicebox](juicebox/) | Runtime | Sales | Query recruiting analytics, shortlists, and sourcing agents. |
| `klaviyo` | [Klaviyo](klaviyo/) | Runtime | Sales | Manage profiles, segments, campaigns, and flows. |
| `mailerlite` | [MailerLite](mailerlite/) | Runtime | Sales | Manage subscribers, groups, campaigns, and automations. |
| `mem` | [Mem](mem/) | Runtime | Productivity | Capture, search, and organize notes and collections. |
| `mercury` | [Mercury](mercury/) | Runtime | Finance And Legal | Read balances, transactions, statements, and cards. |
| `navan` | [Navan](navan/) | Runtime | Scheduling | Query expenses, travel bookings, policies, and cards. |
| `onedrive` | [OneDrive](onedrive/) | Runtime | Documents And Files | Browse, search, and read Microsoft OneDrive files. |
| `otter` | [Otter.ai](otter/) | Runtime | Productivity | Search meeting history and pull full transcripts. |
| `outlook` | [Outlook](outlook/) | Runtime | Inbox And Collaboration | Search, read, and send Microsoft Outlook email, and look up contacts. |
| `outlook-calendar` | [Outlook Calendar](outlook-calendar/) | Runtime | Scheduling | List, create, update, and cancel Microsoft Outlook calendar events. |
| `outreach` | [Outreach](outreach/) | Runtime | Sales | Search sequences, prospects, and Kaia meetings. |
| `playwright` | [Playwright](playwright/) | Runtime | Infrastructure | Navigate, click, screenshot, and test in a real browser. |
| `profound` | [Profound](profound/) | Runtime | Research | Track AI visibility, sentiment, and citations. |
| `readwise` | [Readwise](readwise/) | Runtime | Productivity | Search highlights and Reader documents, save articles. |
| `salesforce` | [Salesforce](salesforce/) | Runtime | Sales | Query, create, and update records in your org. |
| `semrush` | [Semrush](semrush/) | Runtime | Research | Research keywords, backlinks, traffic, and competitors. |
| `similarweb` | [Similarweb](similarweb/) | Runtime | Research | Analyze website traffic, audiences, and competitors. |
| `smartsheet` | [Smartsheet](smartsheet/) | Runtime | Documents And Files | Query and update sheets, rows, and workspaces. |
| `typeform` | [Typeform](typeform/) | Runtime | Productivity | Build forms, analyze responses, and manage contacts. |
| `upwork` | [Upwork](upwork/) | Runtime | Productivity | Search talent, post jobs, and manage contracts. |
| `workable` | [Workable](workable/) | Runtime | Sales | Search candidates, move pipelines, and manage HR records. |
| `wrike` | [Wrike](wrike/) | Runtime | Productivity | Search projects, create tasks, and post comments. |
| `x` | [X](x/) | Runtime | Inbox And Collaboration | Search posts, read timelines, pull trends, and manage bookmarks. |
| `x-ads` | [X Ads](x-ads/) | Runtime | Sales | Manage ad campaigns, create ads, track conversions, and pull performance stats. |
| `xero` | [Xero](xero/) | Runtime | Finance And Legal | Read and write invoices, contacts, reports, and payroll. |
| `zoom` | [Zoom](zoom/) | Runtime | Scheduling | Search meetings, pull transcripts, and work with Zoom Docs. |

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

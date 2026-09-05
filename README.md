# Runtime plugins

Official Runtime plugin marketplace: **first-party** agent kits (skills / agent briefs) and **third-party** MCP connectors.


Monorepo companion: [lemon-squared/Runtime-Monorepo](https://github.com/lemon-squared/Runtime-Monorepo).

## Layout

```
plugins/
├── .runtime-plugin/marketplace.json   # full index (source may be nested)
├── teaching/                          # first-party kit
├── continual-learning/                # first-party kit
├── create-plugin/                     # first-party kit
└── third_party/                       # MCP connectors (Gmail, Slack, HubSpot, …)
    ├── gmail/
    └── …
```

Runtime clients resolve `source` from marketplace.json (e.g. `third_party/gmail` or `teaching`).

## First-party

| `name` | Plugin | Author | Category | Description |
|:-------|:-------|:-------|:---------|:------------|
| `teaching` | [Teaching](teaching/) | Runtime | Agent Orchestration | Learning paths, practice checkpoints, and retrospectives for person coaching. |
| `continual-learning` | [Continual Learning](continual-learning/) | Runtime | Agent Orchestration | Mine person transcripts and update durable Runtime memory via a dedicated updater brief. |
| `create-plugin` | [Create Plugin](create-plugin/) | Runtime | Agent Orchestration | Scaffold and validate new Runtime agent plugins. |

## Third-party (MCP)

| `name` | Plugin | Author | Category | Description |
|:-------|:-------|:-------|:---------|:------------|
| `gmail` | [Gmail](third_party/gmail/) | Runtime | Featured | Search, read, draft, and manage email. |
| `google-calendar` | [Google Calendar](third_party/google-calendar/) | Runtime | Featured | Search events and schedule meetings. |
| `google-drive` | [Google Drive](third_party/google-drive/) | Runtime | Featured | Search, read, create, and share files. |
| `granola` | [Granola](third_party/granola/) | Runtime | Featured | Search meeting notes and transcripts. |
| `notion` | [Notion](third_party/notion/) | Runtime | Featured | Skills and MCP for pages, databases, and wikis. |
| `slack` | [Slack](third_party/slack/) | Runtime | Featured | Search, read, and send Slack messages over MCP. |
| `github` | [GitHub](third_party/github/) | Runtime | Infrastructure | Manage repos, issues, pull requests, and Actions. |
| `todoist` | [Todoist](third_party/todoist/) | Runtime | Productivity | Create, find, and complete tasks and projects. |
| `calendly` | [Calendly](third_party/calendly/) | Runtime | Scheduling | Check availability and book, cancel, or reschedule. |
| `ahrefs` | [Ahrefs](third_party/ahrefs/) | Runtime | Research | Research keywords, backlinks, rankings, and site health. |
| `amplemarket` | [Amplemarket](third_party/amplemarket/) | Runtime | Sales | Search people and companies, enrich leads, run sequences. |
| `ashby` | [Ashby](third_party/ashby/) | Runtime | Sales | Search candidates, prep interviews, and manage pipeline tasks. |
| `brevo` | [Brevo](third_party/brevo/) | Runtime | Sales | Manage contacts, email and SMS campaigns, and CRM deals. |
| `brex` | [Brex](third_party/brex/) | Runtime | Finance And Legal | Query expenses, receipts, bills, cards, and travel. |
| `circleback` | [Circleback](third_party/circleback/) | Runtime | Productivity | Search meetings, transcripts, action items, and emails. |
| `clay` | [Clay](third_party/clay/) | Runtime | Sales | Enrich people and companies, run AI research agents. |
| `coda` | [Coda](third_party/coda/) | Runtime | Documents And Files | Search docs, read pages, and update tables. |
| `craft` | [Craft](third_party/craft/) | Runtime | Documents And Files | Search, create, and update documents and daily notes. |
| `customer-io` | [Customer.io](third_party/customer-io/) | Runtime | Sales | Build campaigns, manage segments, and query people. |
| `docusign` | [Docusign](third_party/docusign/) | Runtime | Finance And Legal | Manage envelopes, templates, workflows, and agreements. |
| `fathom` | [Fathom](third_party/fathom/) | Runtime | Productivity | Search meetings and pull transcripts and summaries. |
| `fireflies` | [Fireflies](third_party/fireflies/) | Runtime | Productivity | Search meeting transcripts, summaries, and action items. |
| `godaddy` | [GoDaddy](third_party/godaddy/) | Runtime | Infrastructure | Brainstorm domain names and check availability. |
| `gong` | [Gong](third_party/gong/) | Runtime | Sales | Pull account summaries, deal insights, and call briefs. |
| `guru` | [Guru](third_party/guru/) | Runtime | Documents And Files | Search company knowledge and draft verified answers. |
| `hubspot` | [HubSpot](third_party/hubspot/) | Runtime | Sales | Search and update contacts, companies, deals, and tickets. |
| `intercom` | [Intercom](third_party/intercom/) | Runtime | Customer Support | Search conversations, contacts, and Help Center articles. |
| `jotform` | [Jotform](third_party/jotform/) | Runtime | Productivity | Create and edit forms, then read submissions. |
| `juicebox` | [Juicebox](third_party/juicebox/) | Runtime | Sales | Query recruiting analytics, shortlists, and sourcing agents. |
| `klaviyo` | [Klaviyo](third_party/klaviyo/) | Runtime | Sales | Manage profiles, segments, campaigns, and flows. |
| `mailerlite` | [MailerLite](third_party/mailerlite/) | Runtime | Sales | Manage subscribers, groups, campaigns, and automations. |
| `mem` | [Mem](third_party/mem/) | Runtime | Productivity | Capture, search, and organize notes and collections. |
| `mercury` | [Mercury](third_party/mercury/) | Runtime | Finance And Legal | Read balances, transactions, statements, and cards. |
| `navan` | [Navan](third_party/navan/) | Runtime | Scheduling | Query expenses, travel bookings, policies, and cards. |
| `onedrive` | [OneDrive](third_party/onedrive/) | Runtime | Documents And Files | Browse, search, and read Microsoft OneDrive files. |
| `otter` | [Otter.ai](third_party/otter/) | Runtime | Productivity | Search meeting history and pull full transcripts. |
| `outlook` | [Outlook](third_party/outlook/) | Runtime | Inbox And Collaboration | Search, read, and send Microsoft Outlook email, and look up contacts. |
| `outlook-calendar` | [Outlook Calendar](third_party/outlook-calendar/) | Runtime | Scheduling | List, create, update, and cancel Microsoft Outlook calendar events. |
| `outreach` | [Outreach](third_party/outreach/) | Runtime | Sales | Search sequences, prospects, and Kaia meetings. |
| `playwright` | [Playwright](third_party/playwright/) | Runtime | Infrastructure | Navigate, click, screenshot, and test in a real browser. |
| `profound` | [Profound](third_party/profound/) | Runtime | Research | Track AI visibility, sentiment, and citations. |
| `readwise` | [Readwise](third_party/readwise/) | Runtime | Productivity | Search highlights and Reader documents, save articles. |
| `salesforce` | [Salesforce](third_party/salesforce/) | Runtime | Sales | Query, create, and update records in your org. |
| `semrush` | [Semrush](third_party/semrush/) | Runtime | Research | Research keywords, backlinks, traffic, and competitors. |
| `similarweb` | [Similarweb](third_party/similarweb/) | Runtime | Research | Analyze website traffic, audiences, and competitors. |
| `smartsheet` | [Smartsheet](third_party/smartsheet/) | Runtime | Documents And Files | Query and update sheets, rows, and workspaces. |
| `typeform` | [Typeform](third_party/typeform/) | Runtime | Productivity | Build forms, analyze responses, and manage contacts. |
| `upwork` | [Upwork](third_party/upwork/) | Runtime | Productivity | Search talent, post jobs, and manage contracts. |
| `workable` | [Workable](third_party/workable/) | Runtime | Sales | Search candidates, move pipelines, and manage HR records. |
| `wrike` | [Wrike](third_party/wrike/) | Runtime | Productivity | Search projects, create tasks, and post comments. |
| `x` | [X](third_party/x/) | Runtime | Inbox And Collaboration | Search posts, read timelines, pull trends, and manage bookmarks. |
| `x-ads` | [X Ads](third_party/x-ads/) | Runtime | Sales | Manage ad campaigns, create ads, track conversions, and pull performance stats. |
| `xero` | [Xero](third_party/xero/) | Runtime | Finance And Legal | Read and write invoices, contacts, reports, and payroll. |
| `zoom` | [Zoom](third_party/zoom/) | Runtime | Scheduling | Search meetings, pull transcripts, and work with Zoom Docs. |

Author values match each plugin's `plugin.json` `author.name` (`plugins@lemonsquared.com`).

## How Runtime clients consume this marketplace

1. Clients fetch `.runtime-plugin/marketplace.json` from this repository (or a pinned ref).
2. For each entry, they load `<source>/.runtime-plugin/plugin.json` and merge marketplace + plugin metadata (plugin wins on conflicts).
3. When `mcpServers` points at `./mcp.json`, the client loads that template and **injects account secrets** into `${ENV}` placeholders. Secrets never live in this repo.
4. Optional Runtime fields on the plugin manifest:
   - `authKind`: `oauth` | `secret` | `github_app`
   - `secretField`: env var name the account injects
   - `wired`: whether the MCP transport is verified for Runtime
   - `skills` / `agents`: first-party kit paths

Auth stays account-owned and product-side. Plugin authors only ship templates.

## Add a plugin

- **First-party kit:** add a top-level folder with `.runtime-plugin/plugin.json` and `skills/` (and optional `agents/`), then list it in marketplace.json with `"source": "<name>"`.
- **MCP connector:** add `third_party/<name>/` the same way, with `"source": "third_party/<name>"`. Prefer `wired: false` until Runtime verifies the transport.

Run `bun run validate` before opening a PR.

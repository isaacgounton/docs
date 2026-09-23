---
title: Meta Developer Tools MCP
version: 1.0
date: 2026-09-22
updated: 2026-09-22
status: active
description: "Reference for Meta's beta Developer Tools MCP server: endpoint, OAuth sign-in, Read/Manage scopes, client setup for Claude, Codex, ChatGPT and Cursor, and its 10 devtools_ tools for apps, reviews and webhooks."
source:
  - "ingested/documentation/Developer Tools MCP  Developer Documentation.md"
reliability: high
changes: "Created by wiki-ingest from Meta developer documentation"
page_type: reference
---

# Meta Developer Tools MCP

> Reference for Meta's beta Developer Tools MCP server: endpoint, OAuth sign-in, Read/Manage scopes, client setup for Claude, Codex, ChatGPT and Cursor, and its 10 devtools_ tools for apps, reviews and webhooks.

---

## Server

| Item | Value | Notes |
|---|---|---|
| Name | `Meta Developer Tools` | Claude Code id in examples: `meta_developer_tools` |
| Transport | Streamable HTTP | |
| Endpoint | `https://mcp.facebook.com/devtools` | |
| Auth | OAuth with Meta developer account | No App ID / App Secret in client config |
| Status | Beta, gradual rollout | Interface and tools may change (doc updated 2026-06-12) |

> [!info]
> Sign-in must be repeated after restarting the client. Revoke or change access at facebook.com > Settings > Business Integrations.

---

## Client Setup

| Client | How |
|---|---|
| Claude Code | `claude mcp add --transport http meta_developer_tools https://mcp.facebook.com/devtools`, then `/mcp` > select > Authenticate |
| Claude Desktop | Settings > Connectors > Add custom connector (name + URL) |
| Codex App | Settings > MCP Servers > Add servers > Streamable HTTP, auth OAuth; restart and check `~/.codex/config.toml` |
| ChatGPT | Enable Developer Mode (Settings > Connectors > Advanced), then create connector with OAuth |
| Cursor (app and CLI) | Add to `~/.cursor/mcp.json` (global) or `.cursor/mcp.json` (project); click "Needs login" |

```json
{
  "mcpServers": {
    "Meta Developer Tools": {
      "url": "https://mcp.facebook.com/devtools",
      "type": "http"
    }
  }
}
```

**Sign-in flow:** start connection > browser Meta login > choose which apps to grant > return to client and verify.

**Verify:** restart client, ask the agent to list the server's tools (expect 10), run a low-risk read such as `devtools_app_list` or `devtools_api_changelog`.

---

## Scopes

| Scope | Access |
|---|---|
| Read | App config and settings, App Review status, compliance, API usage/health, webhook topics and subscriptions |
| Manage | Read plus create/update/delete webhook subscriptions (the **only** write capability) |

Scopes are set per app in Business Integrations.

---

## Tools

| Tool | Actions | Scope | Use |
|---|---|---|---|
| `devtools_discovery` | `search_docs` | None | Search Meta developer docs |
| `devtools_app_list` | `list` | Granted apps | List accessible apps, role and granted permission; get `app_id` first |
| `devtools_app` | `basic_settings`, `advanced_settings`, `security`, `restrictions`, `data_protection_officer` | Read | Inspect app configuration |
| `devtools_app_review` | `status`, `history`, `privileges`, `requirements` | Read | App Review state and approved permissions |
| `devtools_compliance` | `status` | Read | Open actions, violations, recommendations |
| `devtools_api_usage` | `rate_limits`, `call_volume`, `deprecations` | Read | Operational health of an integration |
| `devtools_webhook_list` | `list_topics`, `list_subscriptions` | Read | Available topics and current subscriptions |
| `devtools_webhook_manage` | create / update / delete | Manage | Needs a live HTTPS callback that passes Meta verification |
| `devtools_webhook_test` | `test_send` | Read | Send a test payload; field must belong to an active subscription |
| `devtools_api_changelog` | `list_products`, `get_changelog_url`, `get_rss_url` | None | Changelog and RSS URLs per product |

> [!tip]
> Typical flow for wiring WhatsApp Cloud API or Messenger events: `devtools_app_list` > `devtools_webhook_list` (topics) > `devtools_webhook_manage` (subscribe) > `devtools_webhook_test`.

---

## Troubleshooting

| Message | Meaning |
|---|---|
| "It looks like this app isn't available" | Account lacks approved access yet (rollout) |
| "Facebook login is currently unavailable for this app" | MCP client may not be supported yet |
| No tools / auth error | Recheck endpoint URL and complete sign-in |

---

## Related

[[AI & Agents - Home]] | [[Claude Code - Working System]]

---

## Sources

| Title | Publisher | Date | Links |
|---|---|---|---|
| Developer Tools MCP | Meta for Developers | 2026-06-12 | [Post](https://developers.facebook.com/documentation/mcp/devtools-mcp) · [[ingested/documentation/Developer Tools MCP  Developer Documentation]] |

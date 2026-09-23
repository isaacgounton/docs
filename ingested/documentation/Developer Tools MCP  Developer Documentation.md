---
title: "Developer Tools MCP | Developer Documentation"
source: "https://developers.facebook.com/documentation/mcp/devtools-mcp?utm_source=dfc_myapp"
author:
published:
created: 2026-07-30
description:
tags:
  - "clippings"
---
Was this helpful?

## Developer Tools MCP

Updated: Jun 12, 2026

Copy for LLM

[View as Markdown](https://developers.facebook.com/documentation/mcp/devtools-mcp.md)

The Meta Developer Tools MCP server gives AI agents and IDE assistants a single entry point for the day-to-day work of building on the Meta developer platform. With it connected, an agent can read your app configuration, monitor API health, file and check App Reviews, list and probe webhook subscriptions, look up the API changelog, and search the developer documentation.

**Note:** Meta Developer Tools MCP is rolling out gradually and may not be available to everyone yet.

<video aria-label="" src="https://video.fyyz1-2.fna.fbcdn.net/o1/v/t2/f2/m366/AQN_JykLgtZ5JX97Wt6qbVrvuvEujJMAxrroefHG5aRNuYWiDBUnJ6LGVe5CvTJziykfMvmaeF0E2FRHjkMi2tHvp1oAYy-e6T1X3-A_j1mrTA.mp4?_nc_cat=102&amp;_nc_oc=AdqKx4s4xa9PVOVtOpImhEEFNDojrLCPRaFnLCXPkfbQEOot8vkAsioxrophP4UopKKJ8C1YI2z0e3lx41qvU9jW&amp;_nc_sid=5e9851&amp;_nc_ht=video.fyyz1-2.fna.fbcdn.net&amp;_nc_ohc=eYWme-LeHM4Q7kNvwEv66MR&amp;efg=eyJ2ZW5jb2RlX3RhZyI6Inhwdl9wcm9ncmVzc2l2ZS5GQUNFQk9PSy4uQzMuMTI4MC5kYXNoX2gyNjQtYmFzaWMtZ2VuMl83MjBwIiwieHB2X2Fzc2V0X2lkIjoxMDI2MTY5NzIzMTAyOTI3LCJhc3NldF9hZ2VfZGF5cyI6MzMsInZpX3VzZWNhc2VfaWQiOjEwMTI4LCJkdXJhdGlvbl9zIjoxOTMsInVybGdlbl9zb3VyY2UiOiJ3d3cifQ%3D%3D&amp;ccb=17-1&amp;vs=df4152695b7a915e&amp;_nc_vs=HBksFQIYRWZiX2VwaGVtZXJhbC8zRTQ1QjJFQkU4NTIyMkFFRkU0QTYwMzBENEJBQTdCRl9tdF8xX3ZpZGVvX2Rhc2hpbml0Lm1wNBUAAsgBEgAVAhhAZmJfcGVybWFuZW50LzdDNEQyMjVGMDM4N0Q3MzREMTVGOTA0QTdBMjkxRjhBX2F1ZGlvX2Rhc2hpbml0Lm1wNBUCAsgBEgAoABgAGwKIB3VzZV9vaWwBMRJwcm9ncmVzc2l2ZV9yZWNpcGUBMRUAACaem5md-NLSAxUCKAJDMywXQGgwAAAAAAAYGWRhc2hfaDI2NC1iYXNpYy1nZW4yXzcyMHARAHUCZaCeAQA&amp;_nc_gid=SYL39JOPR0EWBNtnEtdBaw&amp;_nc_ss=7b2a8&amp;_nc_map=urlgen_bucketless&amp;_nc_zt=28&amp;oh=00_AQFox39doMl5NfBPxhEQY13t77tr8U6_1IbMr3FlFSpqRw&amp;oe=6A709FC6&amp;bitrate=456049&amp;tag=dash_h264-basic-gen2_720p" controls=""></video>

## Overview

The following table summarizes the server details:

| Attribute | Value |
| --- | --- |
| Server name | `Meta Developer Tools` |
| Transport | Streamable HTTP |
| Endpoint | `https://mcp.facebook.com/devtools` |
| Authentication | Meta developer account sign-in (OAuth) |
| Status | Beta - interface and tool set may change |

## Set up your IDE or agent client

Configure your client using one of the sections below, then complete the [OAuth sign-in](#oauth-sign-in) to authenticate. Client-specific authentication steps are noted where they apply.

### Claude Code and Desktop

**Claude Code** — run the following command to add the server:

```
claude mcp add --transport http meta_developer_tools https://mcp.facebook.com/devtools
```

Then run `/mcp` in a session and select **meta\_developer\_tools** to authenticate.

**Claude Desktop** — open **Settings** > **Connectors** > **Add custom connector**, then set:

- **Name**: `Meta Developer Tools`
- **URL**: `https://mcp.facebook.com/devtools`

### OpenAI Codex App and ChatGPT

**Codex App** — open **Settings** (the gear icon, bottom left) > **MCP Servers** > **Add servers**, choose **Streamable HTTP**, then set:

- **Name**: `Meta Developer Tools`
- **URL**: `https://mcp.facebook.com/devtools`
- **Authentication**: **OAuth**

Click **Authenticate** and complete the [OAuth sign-in](#oauth-sign-in).

Restart the Codex App and verify that the new server entry appears in the `~/.codex/config.toml` file.

**ChatGPT** — enable Developer Mode under **Settings** > **Connectors** > **Advanced settings**, then go to **Settings** > **Connectors** and create a connector with:

- **Name**: `Meta Developer Tools`
- **URL**: `https://mcp.facebook.com/devtools`
- **Authentication**: **OAuth**

Meta Developer Tools appears in the composer’s Developer mode menu during conversations.

### Cursor

Cursor reads MCP servers from `mcp.json` — `~/.cursor/mcp.json` for all projects, or `.cursor/mcp.json` for a single project. The Cursor app and the Cursor CLI share this file.

Add the server to `mcp.json`:

```
{
  "mcpServers": {
    "Meta Developer Tools": {
      "url": "https://mcp.facebook.com/devtools",
      "type": "http"
    }
  }
}
```

You can also add it from the app: open **Settings** > **Tools & Integrations** > **New MCP Server**, which opens `mcp.json` for you to paste the entry above.

After saving, Cursor lists **Meta Developer Tools** under **Tools & Integrations** with a **Needs login** action. Click it to start the [OAuth sign-in](#oauth-sign-in).

In the Cursor CLI, MCP uses the same `mcp.json` configuration. If a server requires OAuth, Cursor prompts you to authenticate interactively the first time the server is used.

## OAuth sign-in

The Meta Developer Tools MCP server authenticates with your Meta developer account over OAuth, so the same sign-in flow works with every client. You no longer need to add an App ID or App Secret to your client config. To authenticate, connect the server, sign in, and choose which apps to grant access to, as described in [Sign-in flow](#sign-in-flow).

### Sign-in flow

After you add the server to your client (see [Set up your IDE or agent client](#set-up-your-ide-or-agent-client)):

1. **Start the connection.** Many clients begin the OAuth flow automatically when the server is added. Others require you to click **Connect** or **Authenticate** first. For example, run `/mcp` in Claude Code and select **Authenticate**, or click **Authenticate** in a desktop client.
2. **Sign in.** Your browser opens to sign in with your Meta account. If it doesn’t open automatically, copy the link your client prints and open it manually.
3. **Grant access.** On the consent screen, select the apps you want the server to access.
4. **Confirm.** Return to your client and [verify your connection](#verify-your-connection).

You’ll need to complete the sign-in flow again when you restart the client.

### Scopes

Each connected app supports two scopes, which you set per app in your Business Integrations settings.

| Scope | Access |
| --- | --- |
| **Read** | Read-only access to everything the server exposes: app configuration and settings, App Review status, compliance status, API usage and health, and webhook topics and subscriptions. |
| **Manage** | Everything in Read, plus write access to create, update, and delete webhook subscriptions. Webhook management is the only write capability. |

You can manage the scopes or revoke access at any time at [facebook.com⁠](https://www.facebook.com/) > **Settings** > **Business Integrations**.

### Troubleshooting

The following table describes common error messages:

| Message | What it means |
| --- | --- |
| “It looks like this app isn’t available” | Your account doesn’t have approved access yet. |
| “Facebook login is currently unavailable for this app” | Your MCP client may not be supported yet. |

### Verify your connection

After adding the server, confirm your agent can see the tools:

1. Restart the IDE or agent client.
2. Ask the agent to list the tools it has from the `meta developer tools` server. You should see the 10 tools listed below.
3. Run a low-risk read tool. For example, `devtools_app_list` to list your apps, or `devtools_api_changelog` to look up available changelog products.

If the agent reports no tools or an authentication error, re-check the endpoint URL and confirm you completed the sign-in flow.

## Tools

The Meta Developer Tools MCP exposes 10 tools. Each tool is namespaced with the `devtools_` prefix. Most app-scoped tools take an `app_id` and require the **Read** or **Manage** scope; the changelog and documentation-search tools work without app-scoped permissions.

### devtools\_discovery

Search Meta developer documentation for API guides, references, and tutorials. Use this when an agent needs to find the right doc to answer a how-to question or ground its next step. Works without app-scoped permissions.

**Actions:**`search_docs`

**Example prompt:** “Search the Meta developer docs for how to set up WhatsApp Cloud API webhooks.”

### devtools\_app\_list

List the Meta apps you can access through the Meta Developer Tools MCP server. Returns the apps where you hold a developer, admin, or tester role and have granted the server access, along with the permissions you granted (read or manage) and your role on each app. Supports pagination. Use this first to discover the `app_id` values the other tools need.

**Actions:**`list`

**Example prompt:** “List all the Meta apps I have access to.”

### devtools\_app

Inspect the settings, permissions, and configuration of a Meta app. Use this when an agent needs to know how an app is set up; its basic and advanced settings, security configuration, platform restrictions, or data protection officer details.

**Actions:**`basic_settings`, `advanced_settings`, `security`, `restrictions`, `data_protection_officer`

**Example prompt:** “Show the basic settings and security configuration for app 1234567890.”

### devtools\_app\_review

Check App Review for the permissions and features your app requests. Use this when an agent needs to look up the status of a review, see what an app is approved for, or understand what’s required to submit.

**Actions:**`status`, `history`, `privileges`, `requirements`

**Example prompt:** “What’s the App Review status for app 1234567890, and which permissions is it approved for?”

### devtools\_compliance

Check the compliance status of a Meta app, open required actions, violations, and recommendations. Use this when an agent needs to confirm an app is in good standing before launching a feature or submitting for review.

**Actions:**`status`

**Example prompt:** “Check whether app 1234567890 has any open compliance actions or violations.”

### devtools\_api\_usage

Monitor API health for a Meta app so an agent has operational visibility into an integration. Use this to see whether an app is approaching its rate limits, how much call volume it’s driving, and which APIs it depends on are deprecated.

**Actions:**`rate_limits`, `call_volume`, `deprecations`

**Example prompt:** “Is app 1234567890 close to any rate limits, and are there deprecations I should plan for?”

### devtools\_webhook\_list

List the webhook topics available to a Meta app and the subscriptions currently configured on it, including the subscribed fields. Use this to see what an app can subscribe to and what it’s already receiving.

**Actions:**`list_topics`, `list_subscriptions`

**Example prompt:** “List the webhook topics and current subscriptions for app 1234567890.”

### devtools\_webhook\_manage

Create, update, and delete webhook subscriptions on a Meta app. Use this when an agent is wiring an app to receive updates from a Meta product (for example, Messenger Platform message events or WhatsApp Cloud API events). Subscribing requires a live HTTPS callback URL that passes Meta’s verification. Requires the **Manage** scope.

**Example prompt:** “Subscribe app 1234567890 to the page topic for the feed and messages fields, using https://example.com/webhook as the callback URL.”

### devtools\_webhook\_test

Send a test payload to a webhook subscription so you can verify the receiving endpoint is reachable and handles the event correctly. Use this during initial integration and after callback-URL changes. The field must belong to an active subscription on the topic. List subscriptions first to find valid topic and field combinations.

**Actions:**`test_send`

**Example prompt:** “Send a test event to the messages field on the page topic for app 1234567890.”

### devtools\_api\_changelog

Find Meta platform changelog products and their public changelog and RSS URLs, so an agent can point a developer to “what changed recently?” without browsing manually. Works without app-scoped permissions.

**Actions:**`list_products`, `get_changelog_url`, `get_rss_url`

**Example prompt:** “What changelog products are available, and what’s the RSS feed URL for business messaging?”
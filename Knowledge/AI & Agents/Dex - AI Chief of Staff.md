---
title: Dex - AI Chief of Staff
version: 1.0
date: 2026-09-22
updated: 2026-09-22
status: active
description: "Profile of Dex, Dave Killeen's open-source AI chief of staff built on Claude Code: a local Markdown vault of people, meetings and goals, role-based setup, and a native desktop app in private beta."
source:
  - "ingested/clippings/Your AI Chief of Staff.md"
reliability: low
changes: "Created by wiki-ingest from Dex landing page"
page_type: profile
---

# Dex - AI Chief of Staff

> Profile of Dex, Dave Killeen's open-source AI chief of staff built on Claude Code: a local Markdown vault of people, meetings and goals, role-based setup, and a native desktop app in private beta.

---

## Key Facts

| Field | Value |
|---|---|
| **Type** | Personal operating system / AI chief of staff |
| **Creator** | Dave Killeen (Field CPO EMEA at Pendo; host of The Vibe PM Podcast; ex BBC, MailOnline, Badoo/Bumble) |
| **Open-source core** | `github.com/davekilleen/dex`, terminal-based; 473 stars / 127 forks at capture |
| **Desktop app** | Native Mac app, private beta; mobile "coming" |
| **Storage** | Local, searchable Markdown vault the user owns |
| **Integrations** | Nango-powered directory (678 services indexed) exposed via MCP; e.g. Calendar, Gmail, Slack, Teams, Granola, Gong, Salesforce, HubSpot, Notion, Linear, Jira, Drive |
| **Setup** | Pick a role (25 presets from C-suite to IC) and it scaffolds the system |
| **Website** | heydex.ai |

---

## Overview

Dex grew out of eight months of the author building a personal operating system with Claude Code, then open-sourcing it. Its pitch against chat assistants is **compounding structured memory**: every meeting, message and goal becomes connected Markdown pages (people, projects, meetings, goals) on the user's machine rather than an opaque chat history. It is relevant here as a worked example of the "vault as agent memory" pattern also used by the orchestrator in [[AI Agents - Multi-Agent Orchestration]].

---

## Claimed Capabilities

All of the following are vendor claims from the landing page, not independently tested.

| Command / feature | What it claims to do |
|---|---|
| "plan my day" / morning brief | Overnight intel, meeting prep, three focus items; flags meetings that map to no goal |
| "prep me for my 2pm" | Pulls CRM, call recordings, notes and email on an account into talking points and drafts |
| "what do I owe people?" | Finds open loops across channels and drafts replies |
| "who has gone quiet?" | Compares each relationship to its usual cadence and drafts re-engagement notes |
| "write my weekly update" | Summarises shipped work, deal movement and risks |
| "capture my wins" | Maps work to competencies to build a promotion case |
| After-call processing | Updates person pages, extracts follow-ups, flags dependencies |
| Routines | Plain-English scheduled jobs whose output lands in a tray |
| Goals ladder / weekly review | Scores priorities done, partial or slipped with evidence |
| Drafts tray | Nothing sends without user approval |

Landing-page statistics (23 meetings/week, 3.1h/day lost to context switching, 62% of action items not followed up) are unsourced.

---

## Notes

- The design choices worth borrowing are independent of the product: local Markdown as the memory layer, entity pages per person and project, scheduled routines writing to a review tray, and human approval before anything is sent. The same pattern appears in the morning-brief routine of [[Claude Code - Working System]].
- Tagline worth keeping: "If Dex disappeared tomorrow, you would lose an assistant, not your memory."
- Testimonials on the page are curated LinkedIn quotes; treat as marketing.

---

## Related

[[AI & Agents - Home]] | [[Claude Code - Working System]] | [[AI Agents - Multi-Agent Orchestration]] | [[Personal Effectiveness - Home]]

---

## Sources

| Title | Publisher | Date | Links |
|---|---|---|---|
| Your AI Chief of Staff | heydex.ai (vendor landing page) | 2026-08-30 (captured) | [Post](https://heydex.ai/#desktop) · [[ingested/clippings/Your AI Chief of Staff]] |

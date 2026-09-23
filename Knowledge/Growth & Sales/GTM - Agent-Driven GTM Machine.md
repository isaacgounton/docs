---
title: GTM - Agent-Driven GTM Machine
version: 1.0
date: 2026-09-22
updated: 2026-09-22
status: active
description: "One-person GTM system built from approval-gated agent workflows (trigger, source, output, approval) on a shared markdown vault; playbooks for agencies, SaaS and creators, plus an SEO/answer-engine layer and build order."
source:
  - "ingested/clippings/How to build a GTM machine from 0 to $10k MRR.md"
reliability: low
changes: "Created by wiki-ingest from exm7777 GTM machine guide"
page_type: knowledge
---

# GTM - Agent-Driven GTM Machine

> One-person GTM system built from approval-gated agent workflows (trigger, source, output, approval) on a shared markdown vault; playbooks for agencies, SaaS and creators, plus an SEO/answer-engine layer and build order.

---

## Overview

A one-person business can now run go-to-market workflows that used to need a sales team. Agents find, research and draft, and the operator approves every send. The core idea: **anyone can send messages now, so the research behind the message is the only thing left to sell.** The system has three variants (agency, SaaS, infoproducts/communities). They share a knowledge base, a four-part workflow shape, and an SEO/answer-engine layer.

> [!warning]
> The source is marked "paid partnership" and promotes Viktor, an AI employee that runs in Slack or Teams, including referral links. The workflows below don't depend on Viktor. Treat its "does 80% out of the box" claim as advertising.

---

## Foundations

### The knowledge base ("the vault is the business")

Every workflow reads one shared brain before it writes anything. The simplest strong version is a folder of linked markdown files, such as an Obsidian vault. One note per topic:

| Note | Contents |
|---|---|
| Offer | What you sell, price, what's included, what you refuse to do |
| Buyers | Verticals, what a qualified lead looks like, what a bad-fit lead looks like |
| Voice | How you write, banned words, your 5 best messages/posts as examples |
| Market map | Competitors, the category pages that list them, where buyers spend time |
| Workflow runbooks | Stage-by-stage checklists and where the agent stops for you |
| **Decisions log** | Every settled outreach, pricing or content decision. Each correction to an agent becomes one line here, so it sticks |

Prospect research stored here pays off again later: next month's follow-up, the proposal, and a case study a year on all reuse it.

### The four-part workflow shape

1. **Trigger:** a post crosses an engagement threshold, a call ends, a payment fails.
2. **Source:** the agent reads the CRM, a prospecting database or a transcript.
3. **Output:** a research sheet, a list or a draft.
4. **Approval:** nothing sends, publishes or spends money until you say yes.

> [!tip]
> Build one workflow at a time. Add the next one only when the current one passes the **7am test**: it produced its output this morning without a message from you.

### Workspace setup (any agent platform)

- One channel per workflow (outbound, content, pipeline, members).
- Pin a message in each channel: what you sell, who buys, what the channel produces, and what never sends without you.
- Per-tool permissions: the agent can read and draft on its own, must ask before anything sends or spends, and has no access to tools that should never reach the outside.
- Research sheets carry a **confidence note per row** so weak research is visible.

Typical connectors: Apollo and Clay (lists and enrichment), HubSpot or Attio (CRM), Instantly or lemlist (sequences), Stripe, Meta and Google ads, beehiiv or Kit (newsletter), Google Analytics or PostHog.

---

## Chapter 1 - Agencies

Goal: a steady flow of researched conversations with the right companies, and keeping clients past the first quarter.

| Workflow | Trigger / source | Output | Notes |
|---|---|---|---|
| **Signal outbound** | A change at the prospect's company (funding, a job post for the role you replace, a new marketing head, a website untouched for a year) found in Apollo filtered to your ICP and enriched through Clay waterfall | Research sheet (what changed, what your service fixes, confidence) plus drafts for top rows only | Two short paragraphs that open with the workload you spotted, no pitch in the first line, sent from your own inbox |
| **Warm outbound** | Your post crosses an engagement threshold; export likers, commenters and reposters, then match to your ICP | DM drafts for the best matches, email drafts for the rest | Send each one by hand, because platforms ban automated messaging and the list is short |
| **Proposal from the call** | Notetaker transcript (Granola, Fireflies) | Proposal draft if there is a buying signal (price, scope or start date discussed), otherwise a follow-up note | Assumptions listed, unanswered fields left blank, the price stays your decision. Follow-ups run off document read receipts |
| **Retention loop** | Calendar: weekly during ramp, monthly after | Client numbers in one sheet plus a summary with the pipeline (what moved, what's queued, what changed and why) | Monthly refresh of audience and copy. After the first documented win, draft a referral ask for an intro to a *specific kind* of business |

---

## Chapter 2 - SaaS

Goal: the right people see the product do the job every week, and a money loop keeps paying customers.

- **Demo-first content:** for each shipped use case, record the product doing one job for one kind of user. The agent drafts the demo post plus a run of daily short posts that learn from earlier ones. Your manual task: make the first outputs by hand for people who commented, because a stranger who got a personalised result tells others. A launch is one beat inside this workflow, not the plan.
- **Borrow competitors' placements:** take the top results for a keyword you want to own, pull the pages that link to ranking competitors, and **keep only domains that link to several of them** (roundups, resource pages, directories). Paid placements and one-off news links drop out. Output: a placement sheet with a drafted ask to add you or replace their entry with a more complete one. Send the asks yourself. Only submit to directories that give a real link, and treat this as housekeeping, not a traffic channel.
- **Warm outbound for SaaS:** same as the agency version, plus followers of the accounts your buyers trust. Keep a **small weekly cap**, because a run with no replies means a message or profile problem, and sending more teaches you nothing.
- **Money loop (build first if you have paying customers):** Stripe payment events joined with CRM history. A failed charge gets a retry timed by failure reason plus a short email. A cancellation gets an exit survey and then a reason-specific win-back within 1-2 days. Log churn as "card failed" vs "chose to leave", because the two need different fixes. Recovered revenue is the cheapest revenue there is.

---

## Chapter 3 - Infoproducts and Communities

Goal: own the audience instead of renting it, and keep members past month two.

- **Post → owned email:** the agent spots a post that performed and builds a short guide, a landing page and a welcome sequence from it. The sequence makes a **low-ticket offer right away** in the same format, because buyers are a different list from readers. Every subscriber gets a referral link from the first email. Weekly source report.
- **Content batch from evidence:** each week, read your top posts, transcripts and replies, draft the batch per platform in your voice, flag the strongest piece, and add a newsletter poll so readers choose the next topic. Your edits become standing rules.
- **Borrowed rooms:** each month, study what your audience shares and cites. Fill a sheet with small creators (fixed fee plus a bonus paid only on verified views), newsletters and podcasts that sell placements, and weekly niche conversations you can join with a real contribution. Buy a place in someone else's audience before you buy platform reach.
- **Member health:** a welcome within an hour with one first action, a check for a small win within 2 days, a weekly ritual on a fixed day, inactivity nudges at 1 and 2 weeks, and an at-risk list with win-back drafts. Members usually churn in month two because they never did the first thing. Offer a **quarterly plan at signup** to cut cancel decisions from 12 to 4 a year.

---

## Shared Layer - SEO and Answer Engines

Run monthly: ask the questions a buyer would ask an answer engine, then audit your pages and profiles against four checks.

1. **Entity consistency:** name, offer, category and facts stated the same way everywhere.
2. **Answer blocks:** each page opens with a direct, plain answer, facts underneath, proof near the top. Engines pull self-contained passages.
3. **Mentions in places you don't own:** earned by taking part genuinely before you ever mention the product.
4. **Third-party hosts:** Reddit, Medium, YouTube, press-release wires, Google Sites. These still rank and get cited if the content earns its place.

Output: a fix list per page, drafts for host posts, and a month-over-month diff of who got cited. See [[SEO - AI Search Visibility]] for depth.

---

## What to Build First

| Business | First workflow | Why |
|---|---|---|
| Agency | Signal outbound | Moves revenue first |
| SaaS with paying customers | Money loop | Recovers existing revenue |
| SaaS without customers | Demo-first content | Builds the audience |
| Creator | Owned email | Everything else fills this list |
| All | SEO/answer layer last | Slow to build; needs pages worth citing |

Stop adding workflows once the calendar is full. Running two well for a long time beats running four badly.

### Build sheet

1. One workspace, one channel per workflow, context pinned at the top.
2. Every workflow = trigger + source + output + your approval.
3. Anything that sends, publishes or moves money waits for your yes.
4. The research is what you sell. You do the send yourself.
5. Launches and directories are one beat inside content, never the plan.
6. Money loop before acquisition when there are paying customers.
7. Borrowed rooms before bought reach.
8. One workflow at a time. Add the next when the last passes the 7am test.

---

## Related

[[Growth & Sales - Home]] | [[Sales - Outbound Outreach]] | [[Growth - First Users Without Ad Spend]] | [[Marketing - How to Sell a Product]] | [[SEO - AI Search Visibility]] | [[AI Agents - Multi-Agent Orchestration]] | [[Dex - AI Chief of Staff]]

---

## Sources

| Title | Publisher | Date | Links |
|---|---|---|---|
| How to build a GTM machine from 0 to $10k MRR | @exm7777 on X (paid partnership with Viktor) | 2026-08-18 | [Post](https://x.com/exm7777/status/2089714608244457543) · [[ingested/clippings/How to build a GTM machine from 0 to $10k MRR]] |

---

## Pending Review

> This page was created from a single non-authoritative source, and that source is a sponsored post. To raise trust: find a primary source on this topic, or two independent corroborating sources, and re-ingest or enrich this page. Key claims to verify: (1) filtering for domains that link to several competitors reliably surfaces the placements that matter; (2) offering a quarterly plan at signup meaningfully reduces community churn; (3) the four answer-engine checks (entity consistency, answer blocks, off-site mentions, third-party hosts) drive citations.

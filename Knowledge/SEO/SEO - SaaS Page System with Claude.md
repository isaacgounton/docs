---
title: SEO - SaaS Page System with Claude
version: 1.0
date: 2026-09-22
updated: 2026-09-22
status: active
description: "The 9 SaaS SEO page types ranked by intent and difficulty, plus a pattern-based workflow for building one strong page by hand and duplicating it with Claude Code without tripping scaled content abuse."
source:
  - "ingested/clippings/The 9 pages a SaaS needs for SEO (automated with Claude).md"
  - "ingested/clippings/The Guide to Master Claude for SEO.md"
reliability: low
changes: "Created by wiki-ingest from Nicholas Dulait SaaS SEO threads"
page_type: knowledge
---

# SEO - SaaS Page System with Claude

> The 9 SaaS SEO page types ranked by intent and difficulty, plus a pattern-based workflow for building one strong page by hand and duplicating it with Claude Code without tripping scaled content abuse.

---

## Overview

Two threads by Nicholas Dulait (ChatSEO) combine into one system: **what** pages a SaaS should publish (9 types, in priority order) and **how** to produce them at scale with Claude Code (find a keyword pattern, perfect one page, duplicate, then check what the duplication silently broke). The governing constraint is Google's scaled content abuse policy: volume is fine, unoriginal volume is not.

---

## The 9 Page Types

| # | Type | Examples | Intent / difficulty | Verdict |
|---|---|---|---|---|
| 1 | **Alternatives** | "Alternative to X", free/open source/cheaper alternative, "for agencies" | Highest intent: already leaving the incumbent, who will never write this page | Write first |
| 2 | **Comparisons** | "X vs Y", "X vs Y vs Z", "X pricing vs Y pricing" | Field is two vendors plus affiliates | Write early; admit the rows where you lose |
| 3 | **Integrations** | "Tool + Slack / Stripe / Shopify / Zapier / Gmail / WordPress" | Borrow another brand's volume; little competition | Cheapest wins; do while small |
| 4 | **Constraints** | "without subscription / credit card / installation", "no-code", "open source" | Binary filter, not opinion | Only if you truly match |
| 5 | **Pricing** | "X pricing", "tools under 50 EUR", "free vs paid" | High intent, but directories own much of it | After 1-4 earn authority |
| 6 | **Use cases** | "tools to generate leads / manage prospects / handle follow-ups" | Rank for the job, not the category; meets category leaders | Slower, worth it |
| 7 | **Problems** | "tools to automate / reduce / avoid X" | Reader doesn't know the category exists; low intent, weak competition | Long game, payoff ~month 6 |
| 8 | **Features** | "tools with API / AI / reporting / mobile app" | | Only for features you genuinely lead on |
| 9 | **Company size** | "for freelancers / SMEs / teams of 5" | Usually the same page with 3 words swapped | Mostly skip: doorway page risk |

> [!tip]
> Types 1-2 are also the formats AI answers cite most ("best X", "X vs Y", "X alternatives"); see [[SEO - AI Search Visibility]].

---

## Production Workflow

### 1. Pick a pattern, not a keyword

A pattern is a set of keywords with identical intent where Google returns the same page type every time (e.g. `competitor A vs competitor B`, `competitor + alternative`). A keyword gets you a page; a pattern gets you a machine. Find patterns by clustering Search Console or keyword-tool data by intent, then filter on two conditions:

- The SERP is **beatable at your current authority**.
- The intent is **commercial**.

ChatSEO chose "vs" pages over "Semrush alternative" because the alternative SERP was too competitive for their authority, while vs SERPs were thin and the reader already had a card in hand.

### 2. Build one page by hand (take the full hour)

Every weakness multiplies across the cluster. Let tooling produce the draft (title, H1, outline, secondary keywords, cannibalisation check, answer formats the SERP rewards), then spend the hour on what it cannot decide:

- **Brand arguments:** where you concede the competitor's real strengths and what you refuse to claim.
- **One interactive or original element** (below).
- **Structured data:** one instruction to Claude Code at integration.
- **Internal links:** set the pattern on page one so duplicates inherit it.

### 3. Make every page original: the spam defence

Google's March 2024 **scaled content abuse** policy applies regardless of whether content is automated, human or mixed; it targets large amounts of unoriginal content with little value. For every page ask: *what is here that the other nine results do not have?* A quiz, calculator, simulator, your own data, or a table of numbers you actually pulled. One per page, or do not ship the cluster. (ChatSEO uses a 3-question quiz giving a contextual recommendation instead of a generic verdict.)

### 4. Duplicate, then assume something broke

Prompt pattern: "duplicate the last article we published, for these competitors". Claude Code matched the page and shipped EN and FR versions in minutes, but **silently deleted the quiz**, the one element justifying the page.

| Transfers reliably | Silently fails |
|---|---|
| Structure, H1/H2s | Interactive features |
| Title and meta description | Images (keep manual) |
| Structured data | New internal links from older pages |
| Table of contents | hreflang (if not set on page one) |
| FR/EN translation pair | Genuinely fresh comparison data |

**Pre-publish check (~5 human minutes/page):** interactive feature works, images present, schema validates, internal links point both ways, `hreflang` and `html lang` correct in source.

### 5. Repeat in another language

The hour is paid; a second language is nearly free. Caveats:

- On a ccTLD (.fr, .de, .co.uk) multilingual SEO does not work well; the country signal is too strong. Use a .com with subdirectories or a separate domain.
- Language switcher must go to the equivalent URL, not the homepage.
- Verify `html lang` and `hreflang` in the inspector; wrong hreflang makes the versions compete instead of covering two markets.

> [!warning]
> Evidence is one site (the author says so). The vs pattern works because those SERPs are weak; on head terms it would not. If all your patterns sit in hard SERPs, build authority first; duplication is not a substitute.

---

## Related

[[SEO - Home]] | [[SEO - AI Search Visibility]] | [[SEO - Statistics Pages Without Backlinks]] | [[Claude Code - Working System]] | [[GTM - Agent-Driven GTM Machine]]

---

## Sources

| Title | Publisher | Date | Links |
|---|---|---|---|
| The 9 pages a SaaS needs for SEO (automated with Claude) | @nicholasdulait (X) | 2026-08-13 (clipped) | [Post](https://x.com/nicholasdulait/status/2087537648747286874) · [[ingested/clippings/The 9 pages a SaaS needs for SEO (automated with Claude)]] |
| The Guide to Master Claude for SEO | @NicholasDulait (X) | 2026-08-07 | [Post](https://x.com/NicholasDulait/status/2085649587046408535) · [[ingested/clippings/The Guide to Master Claude for SEO]] |

---

## Pending Review

> This page was created from 2 non-authoritative sources by the same author, a vendor promoting its own SEO tool. To raise trust: find a primary source on this topic, or two independent corroborating sources, and re-ingest or enrich this page. Key claims to verify: alternative pages convert best of the 9 types; ccTLD sites cannot rank in other languages; one interactive element per page is sufficient defence against scaled content abuse.

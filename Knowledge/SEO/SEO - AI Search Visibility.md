---
title: SEO - AI Search Visibility
version: 1.0
date: 2026-09-22
updated: 2026-09-22
status: active
description: "How to get named inside ChatGPT, Claude, Perplexity and Google AI Overview answers: consistent brand claims, quotable comparison pages, full topic coverage plus one original finding, earned mentions, and manual tracking."
source:
  - "ingested/clippings/AI SEO for Beginners (Full Playbook!).md"
  - "ingested/clippings/7-Step Claude Information Gain Playbook to Get Cited by Google AI Overviews.md"
reliability: medium
changes: "Created by wiki-ingest from Ramonov AEO playbook and Borja info gain study"
page_type: knowledge
---

# SEO - AI Search Visibility

> How to get named inside ChatGPT, Claude, Perplexity and Google AI Overview answers: consistent brand claims, quotable comparison pages, full topic coverage plus one original finding, earned mentions, and manual tracking.

---

## Overview

AI search (also called AEO, answer engine optimization, or GEO) changes the prize from a blue link to **a mention inside the answer**. The answer usually names about 3 options and most sessions end without a click, so ranking alone is worth less. Two sources feed this page: Sabrina Ramonov's beginner-to-advanced AEO playbook (brand consistency, page formats, off-site mentions) and Borja's observational study of Google AI Overview citations (what actually correlates with being quoted). Together: **say the same thing about yourself everywhere, cover the question completely, then add one thing nobody else has.**

---

## Why It Matters

| Signal | Figure | Source (as cited) |
|---|---|---|
| B2B software buyers who start research in an AI chatbot more often than Google | 51% in 2026, up from 29% a year earlier | G2 survey of 1,076 buyers |
| AI search share of Ahrefs' traffic vs signups | 0.5% of traffic, 12.1% of signups | Ahrefs own-site data |
| Informational searches showing an AI Overview | 86% of a 238-search sample | Borja study |
| AI Overview citations pointing outside that search's top 10 | 44% | Borja study |
| Average CTR loss from AI Overviews | ~15% | Amsive, 700k keywords |
| Share of AI brand mentions coming from third-party sites | ~85% | Ramonov (unsourced) |

**Implication:** AI traffic is small but converts much better, because the visitor has already described their situation, received a shortlist and compared options. Small, fast-moving sites can win because incumbents rarely publish pages that name competitors.

### Old SEO vs AI SEO

| | Classic SEO | AI search |
|---|---|---|
| What you win | A blue link | Your name in the written answer |
| Goal | Top 10 ranking | 1 of ~3 recommended options |
| Main levers | Keywords, backlinks, speed | Consistent facts about you across many sites; complete, quotable pages |
| Reader behaviour | Clicks, then compares | Reads the answer and stops |
| Scoreboard | Clicks, sessions | How often you are named, brand searches, signups |

---

## What the Data Says About Getting Quoted (Borja study)

Observational snapshot: 238 US searches, 12 niches, 1,334 ranking publisher articles, split into quoted vs skipped by the AI Overview on the same day. Correlation only, not causation.

| Finding | Numbers |
|---|---|
| Topic coverage matters most | Least-complete fifth quoted 35%, most-complete fifth 49% |
| Holds within ranking bands | Positions 1-3: 68% vs 53%; 4-6: 49% vs 36%; 7-10: 29% vs 23% |
| Backlinks barely matter | 43% quote rate at 0 links vs 45% at 342 links; 1 in 5 quoted pages had zero backlinks |
| Bigger domains slightly worse | At equal coverage, large domains were quoted a little less |
| Uniqueness alone predicts nothing | Quote rates flat across uniqueness bands (46/48/46/45%) |
| Order matters | Coverage only: 48%. Unique but incomplete: **29% (worst)**. Both: **53% (best)** |

> [!tip]
> Coverage buys the seat; original contribution goes on top. Leading with a "unique angle" while skipping the basics performed worse than a generic complete page.

Borja also cites Google's AI optimization guide: commodity content ("7 Tips for First-Time Homebuyers") loses to non-commodity content with expert or experienced takes, and Google says no third-party tool can see its AI ranking systems.

---

## The Playbook

### Tier 1: Foundations (brand claim and consistency)

1. **Pick the one thing you want to be known for.** A specific value claim for a specific group, not a job title. Structure: `[claim] + [proof] + [proof] + [proof]`. Put it as the first words of your LinkedIn headline, which models read and trust heavily.
2. **Check crawler access.** In `robots.txt`, allow the search crawlers: `OAI-SearchBot` (ChatGPT), `Claude-SearchBot` (Claude), `PerplexityBot`, and `Googlebot`. Blocked crawlers make your own site invisible.
3. **Say the same thing everywhere.** Models learn which words keep appearing next to your name across the web; four different descriptions give them nothing confident to repeat. Paste the same key phrase into site about/home pages, all social bios, review sites (G2, Capterra, Trustpilot, SourceForge), directories, email signature, podcast guest bio.
4. **Collect detailed reviews.** Ask ~5 happy customers for specific written reviews; review sites were buyers' #2 source after AI chatbots.

Prompt pattern: give the model your background and ask for 5 candidate claims ranked by available evidence; then give it every live bio and ask it to flag contradictions and rewrite all of them around the same key phrase.

### Tier 2: Pages AI will quote

**Formats that get cited:** "best X" lists, "X vs Y" comparisons, and "X alternatives" pages. They match buying questions. Include yourself, but be honest: name where competitors win, include strong rivals, give real prices, put a table near the top. See [[SEO - SaaS Page System with Claude]] for the full page-type taxonomy.

**Find real buyer questions** from sales calls, support tickets, 3-star reviews (yours and competitors'), niche social threads and your inbox. Sort into three buckets:

| Bucket | Example | Why |
|---|---|---|
| Competitor terms | "[Competitor] alternatives", "[A] vs [B]" | Low competition, high intent |
| Problem terms | "my team keeps missing client emails" | Buyer's own words |
| Fit terms | "best X for agencies", "X that works with Shopify" | Qualifies the shortlist |

Skip purely educational queries ("what is a CRM"): AI answers them without naming brands.

**Query fan-out:** an AI splits a long question into several hidden sub-searches (pricing, team size, use case). Every sub-question is an entry point, so one page must answer all the small questions inside the big one.

### Tier 3: Information gain (make the page worth quoting)

Borja's 7 steps, run with Claude Code in a terminal:

| Step | Action | Time |
|---|---|---|
| 1 | Fetch full text of the top 10 organic results + top 5 YouTube transcripts + People Also Ask into `./corpus`. Log failed downloads as unknown, not empty. | ~10 min |
| 2 | Extract every distinct claim, merge duplicates, build a claims x pages matrix. Covered by 6+ pages = mandatory; 1-2 pages = optional. | ~15 min |
| 3 | Collect unanswered questions verbatim from Reddit, Quora, YouTube comments, 1-3 star reviews, your support inbox. Drop any the corpus already answers. | 20-30 min |
| 4 | Pick one gap answerable with evidence, ideally a number, that your business is well placed to answer. Phrase it as a measurable question. Check you have no competing page. | ~15 min |
| 5 | Design a finishable study. Cheapest first: data you own but never counted, public data reanalysed, an assembled corpus (reviews, pricing pages, subreddit posts), a paid survey (~$1/response). Freeze the sample and "what would prove me wrong" before looking. | ~30 min design |
| 6 | Run it and compress it into one paragraph near the top: what you checked, what vs what, the result in plain words, one reason it could be wrong. Publish even if it argues against you. | half a day to days |
| 7 | Publish: clear table stakes briefly, put the new finding high, source and date every number, answer step-3 questions in users' words, publish the underlying data. | 2-3 h |

> [!warning]
> An empty gap list is a finding: the topic is either well served (coverage and presentation are your whole play) or the gap has no demand. Before writing, ask: is this page still worth having if Google sends zero traffic?

### Formatting for extraction

AI lifts single passages with no surrounding context, so every chunk should stand alone:

1. Headings as real questions ("How much does X cost?").
2. Direct answer in the first 2 sentences under each heading.
3. Specific over vague: "$29/mo", "3 hours to 20 minutes".
4. State where information came from and when ("prices checked on each vendor's pricing page, July 2026").
5. Table rows that stand alone: "Teams of 5 to 20 posting to 8 platforms", not "Great for teams".

Test: cover the page except one paragraph; if it cannot answer a question alone, rewrite it.

Supporting jobs: 5+ internal links per important page, basic speed and mobile hygiene, and a **refresh every 3 months** of pages that already rank (prices, dead tools, new entrants, title year, fresh examples). Existing trusted pages flip into AI answers faster than new ones.

> [!question]
> **Schema and chunking conflict.** Ramonov recommends Organization schema (homepage) and FAQ schema. Borja cites Google's AI optimization guide as saying AI text files, content chunking and extra schema are not what generative search runs on. Treat schema as cheap hygiene, not a lever, and treat "standalone paragraphs" as a writing-quality rule rather than a technical trick.

### Tier 4: Off-site mentions

Your own site has a ceiling; most mentions come from other domains.

- **Get onto cited lists.** Ask ChatGPT, Claude and Perplexity your category question, record every cited article, and email authors of lists you are missing from: one specific differentiator, offer free access, screenshots and honest weaknesses, under 120 words.
- **Press releases.** A wire service (Ramonov uses EIN Presswire) can place you on news sites that get crawled constantly. Announce one concrete thing, answer who/what/why in the first ~40-50 words, third person, one substantive quote, and point the 2-3 link slots at pages you want cited (pricing, comparison), not the homepage.
- **Podcasts and YouTube.** Guest spots create permanent, re-crawled show-notes pages on trusted domains; find shows via Listen Notes. YouTube needs no one's permission: film videos targeting your buying questions.
- **Earned links from original data.** Borja's point: your study is what earns links and human citations, which is its lasting return.

### Tier 5: Systematise and measure

- **Encode the writing rules in a Claude skill** (a markdown file in `.claude/skills/`). Ramonov's listicle skill pattern: verify prices on live pricing pages, check what AI engines already cite, pull one real strength and weakness per tool from reviews; intro names top pick in first 100 words; comparison table (Tool, Best For, Starting Price, Key Strength) right after; per-tool H3 with "Best for / Pricing / Free trial / Bottom line"; a "How I evaluated" section; honest verdicts and proportional coverage; 3-6 internal and 5-7 inline external links; CTA in the first 25-30%; 1,800-2,800 words; no hype words. See [[Claude Code - Working System]].
- **Scoreboard:** monthly, ask ChatGPT, Claude, Perplexity and Google AI answers 10 realistic buyer questions; log date, whether you were named, which competitors were, which sources were cited. Also track brand-name searches in Search Console, its generative AI performance report, and signups by source. Re-check crawler access if the score reads zero.

> [!note]
> Results take time and vary by category competitiveness. Mentions compound: every consistent profile, page and placement stacks.

---

## Selling AI Visibility as a Service

Ramonov's consulting model:

| Element | Practice |
|---|---|
| Offer | Sell a result with before, after and deadline: "In 90 days, when customers ask ChatGPT who the best [category] in [city] is, your name comes up." |
| Front door | Audit: run 10 buyer questions across engines, screenshot answers with competitors named and the client missing. |
| Pricing | Standalone AI visibility audits ~$250-$2,000 in 2026; then a monthly retainer (thousands/month); set a 3-month minimum expectation. |
| Focus | One industry, so questions, directories and case studies compound. |
| Delivery | Month 1: profiles, consistency, first comparison page. Month 2: buyer questions, new pages, refreshes. Month 3: press release, list outreach, podcasts. |
| Reporting | "Named in X of 10 answers", not traffic. Promise only what you control (pages, profiles, mentions, tracking). |

See [[Marketing - How to Sell a Product]] and [[Growth - First Users Without Ad Spend]].

---

## Related

[[SEO - Home]] | [[SEO - SaaS Page System with Claude]] | [[SEO - Statistics Pages Without Backlinks]] | [[SEO - Local SEO Playbook with Claude]] | [[Claude Code - Working System]] | [[Marketing - How to Sell a Product]] | [[Growth - First Users Without Ad Spend]]

---

## Sources

| Title | Publisher | Date | Links |
|---|---|---|---|
| AI SEO for Beginners (Full Playbook!) | Sabrina Ramonov (Substack newsletter) | 2026-08-01 | [Post](https://open.substack.com/pub/sabrinaramonov/p/ai-seo-for-beginners-full-playbook) · [[ingested/clippings/AI SEO for Beginners (Full Playbook!)]] |
| 7-Step Claude Information Gain Playbook to Get Cited by Google AI Overviews | @borjafat (X) | 2026-08-16 | [Post](https://x.com/borjafat/status/2088991211285561457) · [[ingested/clippings/7-Step Claude Information Gain Playbook to Get Cited by Google AI Overviews]] |

---

## Pending Review

> This page was created from 2 practitioner sources that cite data (one an original observational study) but share no independent corroboration of each other's key claims. A corroborating source from a different author or publication would be sufficient to retire this section. Key claims to verify: backlinks have near-zero effect on AI Overview citation; ~85% of AI brand mentions come from third-party sites; whether schema markup affects AI citation.

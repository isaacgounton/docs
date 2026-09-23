---
title: SEO - Local SEO Playbook with Claude
version: 1.0
date: 2026-09-22
updated: 2026-09-22
status: active
description: "An 8-audit Google Business Profile playbook for local businesses run with Claude Cowork: categories, attributes, review velocity, responses, posts, services, description and photos, sequenced over 4 weeks."
source:
  - "ingested/clippings/claude-seo-100k-month-playbook.md"
reliability: low
changes: "Created by wiki-ingest from Sarvesh Shrivastava local SEO playbook"
page_type: knowledge
---

# SEO - Local SEO Playbook with Claude

> An 8-audit Google Business Profile playbook for local businesses run with Claude Cowork: categories, attributes, review velocity, responses, posts, services, description and photos, sequenced over 4 weeks.

---

## Overview

For a cash-strapped local business with no ad budget, the fastest SEO lever is the **Google Business Profile (GBP)** and the map pack, not the website. A local SEO practitioner (14 years) runs eight competitor-comparison audits with Claude Cowork browsing Google Maps, each producing a spreadsheet and a concrete fix. The claim is execution order, not effort, is what usually fails. The headline "$100k/month" is marketing framing, not a result shown in the source.

---

## Setup: Make Claude Know the Business First

Load once, reuse in every prompt:

- A business file: name, address, phone, website, GBP URL, service areas, target keywords.
- One file per competitor with their GBP URL, so every audit compares automatically.
- Your current GBP details (categories, attributes, photos, services).
- A prompt library, one file per task.

> [!tip]
> This context layer is what turns generic output into business-specific output. It is the same idea as a project context file in [[Claude Code - Working System]].

---

## The 8 Audits

Every prompt follows one pattern: *open Chrome, visit my GBP and 3 competitors (or search "[service] in [city]" on Maps), extract X into a spreadsheet with me vs each competitor, highlight what I'm missing, then write the fix.*

| # | Audit | What to extract | Output / fix | Key insight |
|---|---|---|---|---|
| 1 | **Categories** | Map-pack competitors for 3 keywords; their primary and secondary categories, rating, review count, position | Tab per keyword; categories you lack highlighted | Secondary categories control which searches trigger you. Pattern-spot (e.g. all "emergency plumber" rankers also list "water damage restoration"). Fastest win. |
| 2 | **Attributes** | Every tag (veteran-owned, free estimates, 24/7, online appointments, accessible) | Yes/no matrix; attributes **all** top competitors share = baseline | Helps specific searches and click-through. Shared attributes are table stakes, the rest are differentiators. |
| 3 | **Review teardown** | Last 50 reviews: counts at 30/60/90 days, services and neighbourhoods mentioned, complaints | Tab with reviews/month needed to catch the leader and time to get there | **Review velocity beats total count.** Reviews naming services and places ("furnace install in Highland Park") act as relevance signals: ask customers to mention them. |
| 4 | **Review responses** | Response rate, speed, length, tone, keyword use, handling of negatives (last 30) | Templates for 5, 4, 3 and 1-2 star reviews, 3 variations each | Respond to every review in under a minute; responses naturally carry service + location. |
| 5 | **GBP posts** | Posts in last 90 days, types, images, CTAs, frequency | 8-week calendar, 2-3 posts/week, first 4 weeks written | Competitors rarely post. Neighbourhood posts ("kitchen remodel in [area]") build location relevance across 8-10 areas/month. |
| 6 | **Services section** | Services listed, descriptions, grouping; cross-check against website | 2-3 sentence descriptions per service with keyword, area, benefit | Services on the site but not on GBP are invisible in the map pack. |
| 7 | **Description** | Competitor descriptions: length, keywords, areas, USPs, CTA | 3 versions (max 750 chars): ranking-focused, conversion-focused, balanced | Test one for 30 days, compare impressions and calls, rotate. |
| 8 | **Photos** | Total, last 90 days, types, stock-looking images | 8-week upload plan: before/afters, team on jobs, trucks in served neighbourhoods, install close-ups | Consistency (3-5/week) beats bulk uploads. Source cites Google: photos bring 42% more direction requests and 35% more click-throughs. |

---

## Execution Order

1. **Week 1: Foundation.** Categories and attributes audits. Fastest, most immediate ranking impact.
2. **Week 2: Listing content.** Services section and description.
3. **Week 3: Reviews.** Velocity target and response templates.
4. **Week 4: Content engine.** Posts calendar and photo plan.
5. **Week 5+: Execute.** Post consistently, upload photos weekly, respond to every review. Author claims 90 days of this outranks long-established businesses.

> [!note]
> **What stays human:** knowing which keywords bring revenue, reading the local market, and spotting non-SEO causes (e.g. a competitor ranks because a decade of little-league sponsorships earned links from every local news site). Claude does the gathering; you do the thinking.

> [!warning]
> Some platform claims should be re-checked against current Google documentation before relying on them: that Google "confirmed" responding to reviews improves ranking, that GBP posts expire after 7 days, and the photo uplift percentages. The prompts also rely on an agent with browser access scraping Google Maps.

---

## Related

[[SEO - Home]] | [[SEO - AI Search Visibility]] | [[Growth - First Users Without Ad Spend]] | [[Claude Code - Working System]]

---

## Sources

| Title | Publisher | Date | Links |
|---|---|---|---|
| If I woke up bankrupt tomorrow, this is how I'd get to $100k/month with Claude + SEO | @bloggersarvesh (X Article) | 2026-03-12 | [Post](https://x.com/bloggersarvesh/status/2032130279494853118) · [[ingested/clippings/claude-seo-100k-month-playbook]] |

---

## Pending Review

> This page was created from a single non-authoritative source. To raise trust: find a primary source on this topic, or two independent corroborating sources, and re-ingest or enrich this page. Key claims to verify: review velocity outweighs total review count for map-pack ranking; responding to reviews is a confirmed local ranking factor; GBP posts expire after 7 days.

---
title: "The Guide to Master Claude for SEO"
source: "https://x.com/NicholasDulait/status/2085649587046408535"
author:
  - "[[@NicholasDulait]]"
published: 2026-08-07
created: 2026-08-13
description: "If you want to create SEO pages with Claude but:↳ Your pages get published and never indexed.↳ They all read the same, because they are th..."
tags:
  - "clippings"
---
![Image](https://pbs.twimg.com/media/HPGxhTKWwAAZDe1?format=jpg&name=large)

If you want to create SEO pages with Claude but: ↳ Your pages get published and never indexed. ↳ They all read the same, because they are the same. ↳ You ship more pages and traffic does not move. Anyway, here's how we do our SEO at ChatSEO today. **We ship comparison pages semi-automatically.** Ahrefs vs Moz Pro, Ahrefs vs Ubersuggest, Ahrefs vs Serpstat, English and French.

Each duplicate takes minutes. The page they are duplicated from took an hour.

Most people invert that ratio. It is why their cluster dies.

And the first time I ran it, Claude Code got everything right except one element. That element was the only reason the page deserved to rank.

Before we start, if you're wondering how we are doing SEO/GEO today:

👉 [Here's the free access to the SEO employee we use to grow our traffic daily](https://link.chatseo.app/EWdoT9O)

## 1\. Pick a pattern, not a keyword

A keyword gets you a page. A pattern gets you a machine.

A pattern is a set of keywords with identical intent, where Google returns the same type of page every time. Ours is: competitor 1 vs competitor 2. -> Semrush vs Ahrefs. -> Ubersuggest vs SE Ranking. Same intent, same page shape, same buyer. The other one that prints in SaaS is competitor + alternative.

Finding yours in Ahrefs or Semrush means exporting and reading it yourself. Just connect your Search Console to ChatSEO and ask one thing: give me the best SEO strategy for my site. It clusters the opportunities by intent, returns the patterns, and shows which competitors are already taking that traffic. Thirty seconds, no export.

Then filter on two conditions: the SERP is beatable at your current authority, and the intent is commercial.

The first condition kills most of these projects. We cannot rank "Semrush alternative" today. Too competitive, not enough authority yet. Versus SERPs are thinner and the reader is already comparing tools with a card in hand. That trade was deliberate.

## 2\. Build one page by hand. Take the full hour.

You are about to multiply this page by twenty. Every weakness multiplies with it.

The draft is the fast part. ChatSEO reads the live SERP for the keyword, pulls the secondary keywords, checks whether one of your existing pages is already competing on that query, then hands back the title, the H1, the outline and the answer formats Google is actually rewarding there. The hour goes into the four things it cannot decide for you.

**Brand arguments.** The SEO structure will be right. Where you concede the competitor's real strengths, and what you refuse to claim, is yours to write.

**One interactive feature.** Next section. This is the game.

**Structured data.** One instruction to Claude Code at integration. This used to be miserable to hand-write. There is no longer any excuse for a comparison page without it.

**Internal links.** Set the pattern on page one and the duplicates inherit it.

## 3\. The feature is your spam defence

Our comparison pages carry a quiz. Three questions about your site and your budget, then a contextual recommendation instead of a generic verdict.

In March 2024 Google added scaled content abuse to its spam policies, and the wording matters. It applies no matter whether the content came from automation, humans, or a mix of both. What it targets is large amounts of unoriginal content that gives readers little to no value.

Volume is not a violation -> Unoriginal content is.

So for every page in the cluster, one question: what is here that the other nine results do not have? A quiz, a calculator, a simulator, your own data, a table with numbers you actually pulled. One of them on every page, or do not ship the cluster.

## 4\. Duplicate, then assume something broke

The prompt is boring. Duplicate the last article we published, for these competitors. Claude Code reads the existing page, matches it, ships the French and English versions in minutes.

I opened them expecting to publish. Title, meta description, structured data, table of contents, layout, translation pair. All correct.

The quiz was gone. Both pages. No error, no warning, nothing in the output.

If I had trusted the "articles are live" message, I would have shipped four comparison pages whose only original element had been deleted. The exact pages that policy was written for.

Transfers reliably Silently does not Structure, H1 and H2s Interactive features Title and meta description Images Structured data New internal links from older pages FR and EN pair hreflang, if it was not set on page one Table of contents Genuinely fresh comparison data

The left column is why this works. The right column is why it still needs five human minutes per page.

My check before publish: quiz answering correctly, images in, schema validating, internal links pointing both ways, hreflang and html lang correct in the source.

Images are still fully manual. I stopped trying to automate them.

## 5\. Then do it again in another language

The hour is already paid. A second language costs almost nothing.

Check your TLD first. On a .fr, a .de or a .co.uk you are not doing multilingual SEO, no matter how clean the implementation. Paul tested it on his .fr. The ccTLD is too strong a signal that the site serves one country. Use a .com with subdirectories, or run a separate domain.

Then two things. A language switcher that swaps to the equivalent URL and not to the homepage. And correct html lang plus hreflang: open the inspector, Cmd+F for "lang", verify both. Get hreflang wrong and your two versions compete with each other instead of covering two markets.

## What this does not prove

One site. An anecdote, and I would rather say that than have it said in the replies.

The versus pattern works because those SERPs are weak. On a head term it would not. If your only patterns sit in hard SERPs, fix authority first. Duplication does not substitute for it.

Find the pattern. Build one page properly. Give every page something original. Duplicate. Check what broke.

Thanks for reading! 🎁 [If you want to hire your first AI SEO employee (for free) you can click here](https://link.chatseo.app/EWdoT9O)
---
title: "7-Step Claude Information Gain Playbook to Get Cited by Google AI Overviews"
source: "https://x.com/borjafat/status/2088991211285561457"
author:
  - "[[@borjafat]]"
published: 2026-08-16
created: 2026-08-17
description: "If you want Google's AI Overviews to quote your pages, but:↳ Every site above you has thousands of backlinks and you have none↳ Everything y..."
tags:
  - "clippings"
---
![Image](https://pbs.twimg.com/media/HP1-g9lWEAAgcH0?format=jpg&name=large)

If you want Google's AI Overviews to quote your pages, but:

↳ Every site above you has thousands of backlinks and you have none

↳ Everything you publish ends up saying what the top 10 already said

Then run this 7-step information gain playbook.

👉[Automate this playbook with Distribb](https://distribb.io/?utm_source=infogain-aug15-xarticle)

![Embedded video](https://pbs.twimg.com/amplify_video_thumb/2089074815445434368/img/ImH1mv9xCzM2MkH7?format=jpg&name=large)

9:09

> I analyzed 238 live US Google searches across twelve unrelated niches, from mortgage refinancing to puppy training, and read the 1,334 publisher articles ranking in their top 10, setting aside YouTube, Reddit and the other forum results. For every search showing an AI Overview I split those articles into the ones it quoted and the ones it skipped, so both groups had already won the same search on the same day. Pages that covered most of what the whole top 10 covered were quoted 49% of the time, and pages that covered least were quoted 35% of the time. Backlinks moved that number by about two points, from 43% at zero links to 45% at 342 links. This is one live snapshot, so it can only show what appears next to what, never what caused it.

![Image](https://pbs.twimg.com/media/HP1-BqSWYAAt2Kr?format=png&name=large)

# TL;DR

↳ 86% of the informational searches I sampled showed an AI Overview, so this is the normal result page now.

↳ Going from the least complete fifth of pages to the most complete fifth moved the quote rate from 35% to 49%.

↳ Backlinks did close to nothing. Pages with no links pointing at them were quoted 43% of the time, and pages with 342 links were quoted 45%.

↳ One in five quoted pages had zero backlinks, and almost half had ten or fewer.

↳ Bigger domains did slightly worse once I compared pages that covered their topic equally well.

↳ Pages that said things no rival said but skipped parts of the topic were quoted 29% of the time, the worst group in the study. Pages that did both were quoted 53%, the best.

↳ 44% of the AI Overview citations I captured pointed at pages that were not in that search's top 10 at all.

↳ The playbook: read the whole top 10 and the videos, list what they all cover, collect the questions none of them answer, run one small study to answer one of them, then publish complete coverage plus that one new thing.

↳ Budget one afternoon per article for steps 1 to 4. The study in steps 5 and 6 costs real time.

One limit up front, because it changes how much weight this deserves. This is an observational snapshot of what sat next to what on one day, and it cannot prove that better coverage caused a citation.

# The obvious objection: isn't coverage just a proxy for ranking higher?

It was the first thing I tried to break. Pages that cover a topic well probably rank better, and pages that rank better probably get quoted more, so the whole finding could be ranking wearing a disguise.

So I held the ranking position still and looked again.

![Image](https://pbs.twimg.com/media/HP1-3nyWsAAtmK2?format=png&name=large)

Inside the pages ranked 1 to 3, the best-covered third was quoted 68% of the time against 53% for the least covered. Inside positions 4 to 6 it was 49% against 36%, and inside 7 to 10 it was 29% against 23%. The gap narrows further down the page, but it never disappears.

Then I ran it the other way round, holding coverage still and letting links vary instead. Inside each coverage band, going from pages with no links to pages with around 205 links moved the quote rate by under four points, and the direction flipped between bands. At domain level it went slightly the wrong way, because among pages covering their topic equally well the bigger domains were quoted a little less often.

Links did show up in one place. Quoted pages tended to have a few more of them than skipped pages on the same search, with a median gap of about three referring domains.

# Why "just add unique insights" is not the advice you think it is

Every guide on information gain tells you to say something nobody else has said. The advice is not wrong, but on its own it is close to useless, and my data says it can actively hurt you.

I had 435 of these ranking pages read and scored by judges who were never told which pages the AI Overview had quoted. They saw body text only, with no URL, domain or title. For each search they worked out the questions any good answer had to address, then scored every page twice: how much of that ground it covered, and how much it said that no other page in the same search said.

![Image](https://pbs.twimg.com/media/HP1_TJAW4AA5r5l?format=jpg&name=large)

Read the bottom right against the top left. Covering the topic and adding nothing new was quoted 48% of the time, adding something new while skipping parts of the topic was quoted 29%, and doing both was best at 53%.

So the order is what matters. Coverage buys you the seat, and your own contribution is what you put on top once you have it. Do it the other way round and you land below the generic page you were trying to beat.

The uniqueness score on its own predicted nothing. Sorted into four bands from "nothing new" to "a lot that is new", the quote rates ran 46%, 48%, 46%, 45%. Flat.

# Google's own guidance says the same thing

Google's AI optimization guide backs the order this playbook uses. It contrasts commodity content, "something like '7 Tips for First-Time Homebuyers'", with non-commodity content that "provides unique expert or experienced takes that go beyond common knowledge and the ordinary". The same guide tells you not to bother with AI text files, content chunking or extra schema, because none of those are what generative search runs on. Cover the question properly, then add the thing only you can add.

# The 7-step playbook

Steps 1 to 4 build the map, steps 5 and 6 produce the thing nobody else has, and step 7 ships it. Everything runs in a terminal with Claude Code, so there is no tool subscription in the loop.

# Step 1: Pull the whole top 10 and the videos, then read them properly

![Image](https://pbs.twimg.com/media/HP19ECjXMAAnoM3?format=jpg&name=large)

You cannot claim you are adding something new until you know what is already there, and that means the full text rather than the titles.

Point Claude Code at your keyword and have it collect the corpus into one folder:

↳ The ten organic URLs, fetched and saved as plain text or markdown

↳ The top five YouTube videos on the same query, with transcripts pulled

↳ The People Also Ask questions and the related searches from the same result page

↳ A note of any URL that failed to download, kept as a failure rather than counted as an empty page

Ask for it plainly: "Fetch the top 10 organic results and top 5 YouTube videos for \[keyword\], save the full text of each into ./corpus, and tell me which ones you could not reach."

For a query like "cold brew ratio" you end up with roughly 40,000 words of competitor material in about the time it takes to read one of those pages yourself. That asymmetry is the whole reason to do this with an agent instead of tabs.

Allow 10 minutes.

One caveat. Some sites will block you, and in my study 387 of the 2,998 pages I tried could not be downloaded. Record those as unknown, because treating a page you could not read as a page that said nothing is how you end up "discovering" a gap that is not there.

# Step 2: List what all ten already cover

![Image](https://pbs.twimg.com/media/HP1_4D9WUAAy4Sq?format=jpg&name=large)

Turn the corpus into a table, with claims down the side and the ten pages across the top.

↳ Have Claude Code extract every distinct claim or sub-question from all ten pages

↳ Merge the ones that are the same claim in different words, which is most of them

↳ Mark which pages carry which claim

↳ Anything six or more pages cover is table stakes and is now mandatory for you

↳ Anything one or two pages cover is optional colour

This table is the most useful thing in the playbook, and the tool-based content gap tutorials cannot give it to you, because they diff keyword lists rather than the actual text of the pages.

Be honest about what the table is. It sets your floor. My data says clearing it well is what tracks with getting quoted, and the pages that cleared it completely were quoted 59% of the time against 41% for the thinnest pages. Every one of your competitors can clear it too.

Allow 15 minutes.

# Step 3: Collect the questions nobody on page one answers

![Image](https://pbs.twimg.com/media/HP2AV00WkAA5dXW?format=jpg&name=large)

Now go where people ask things badly and honestly, which is never on the ranking pages.

↳ Reddit threads on the topic, replies included

↳ Quora questions and the answers that clearly disappointed the asker

↳ Comments under the YouTube videos you already transcribed, especially the ones with likes and no reply

↳ Reviews, if the topic touches a product, because the one and three star reviews carry the real objections

↳ Your own support inbox and sales calls, which nobody else can read

Ask Claude Code to collect the questions verbatim, then do the important part: check each one against the corpus from step 1 and drop any that a ranking page already answers.

What survives that filter is your list of real gaps. In my own research for this article, the most repeated unanswered question was a version of "what if I have no data to run a study on", asked over and over under videos that never came back to answer it.

Allow 20 to 30 minutes.

One caveat. A question being unanswered is not proof it is worth answering, because some questions have no audience, which is exactly why nobody bothered.

# Step 4: Find the claim the whole search result is missing

![Image](https://pbs.twimg.com/media/HP2Au7AXEAAY7YM?format=jpg&name=large)

You now have two lists: everything the ten pages say, and everything people ask that they do not say. Put them side by side and pick one thing.

↳ Choose a gap you could answer with evidence rather than opinion

↳ Prefer one where a number would settle the argument

↳ Prefer one your business is unusually placed to answer

↳ Write it as a question with a measurable answer rather than as a topic

↳ Check it against your own site first, so you are not about to compete with a page you already published

"How does cold brew change after 24 hours in the fridge" is a gap you can measure. "More detail on brewing" is not.

Allow 15 minutes.

One caveat, and it is the failure mode nobody warns about. If the gap list comes back empty, that is itself the finding. Either the topic is genuinely well served, in which case coverage plus better presentation is your whole play, or the missing thing is missing because there is no demand for it.

# Step 5: Design a study you can actually finish this week

![Image](https://pbs.twimg.com/media/HP2BKb5WYAAQ-Rq?format=jpg&name=large)

People skip this step because they think original research means commissioning a survey. It does not. Ask Claude Code for three designs that answer your question using data you can reach today, and make it state the cost and the time for each.

The ladder, cheapest first:

↳ Data you already own and have never counted. Quote ranges, intake forms, support tickets, delivery times, the objections in your last 50 sales calls. A local lawyer has this, and so does a bakery.

↳ Public data reanalysed. Government datasets, published reports, open APIs. No audience required, which answers the objection that stops most solo writers.

↳ A corpus you can assemble. The reviews on the top 20 products in your category, the pricing pages of 50 competitors, the first 200 posts in a subreddit. This is what I did here, and the raw material was the search results themselves.

↳ A paid survey, last, at roughly a dollar per completed response.

Then freeze the rules before you look at anything:

↳ What exactly you are counting and what you are excluding

↳ How the sample is chosen, written down before you see any results

↳ What answer would prove you wrong

I froze the 283 keywords in this study to a file before I pulled a single search result, precisely so I could not quietly drop the niches that disagreed with me.

Allow 30 minutes to design. The run itself is anywhere from an afternoon to a few days.

# Step 6: Run it and write the one paragraph

![Image](https://pbs.twimg.com/media/HP2Bin6XUAEUx9f?format=jpg&name=large)

Run it, then compress the whole thing into one paragraph near the top of your article. That paragraph is the asset, and it needs four things:

↳ What you checked and how much of it

↳ What you compared against what

↳ What happened, in words a reader with no statistics training can follow

↳ One plain reason the answer might be wrong

Keep the machinery out of it. Confidence intervals, model names and estimator names belong in a methodology file rather than in the paragraph a reader meets first.

The shape to copy is the blockquote at the top of this article: sample, comparison, result, limitation, in roughly five sentences.

Allow half a day to several days depending on the design you picked.

One caveat, and it is the one that earns you the right to publish any of this. Publish the result even when it argues against you, because a study you only publish when it agrees with you is marketing.

# Step 7: Publish coverage plus your one new thing, then measure it

Now assemble it in the order the data supports.

↳ Clear the table stakes from step 2 completely, in the least space each one needs

↳ Put your new thing high rather than buried at the bottom

↳ Give every number a source and a date

↳ Answer the step 3 questions explicitly, in the words people used to ask them

↳ Publish the underlying data if you can, because that is what makes the claim checkable

Then measure the right thing. Search Console has a generative AI performance report, and Google's guide states plainly that "No third-party tool has access to our internal ranking or AI systems". Track appearances there, and track who starts linking to your study, because links and human citations are the return original data actually pays.

Allow 2 to 3 hours to assemble, then monthly checks.

One caveat that should shape what you write in the first place. AI Overviews cost the average page around 15% of its click-through rate in the largest published measurement, so apply this test before you commit: is this page still worth having if Google sends no traffic at all? If yes, write it.

# What this actually changes

The industry sells information gain as a shortcut for people without backlinks. My data says the shortcut is real, just not where everyone points. Links barely moved the odds of being quoted, covering the question properly moved them a lot, and leading with your unique angle before doing the boring part was the worst outcome in the study.

So the work splits cleanly. An agent can map the coverage in an afternoon, which is the part that gets you quoted, and your original data is what earns the links and the mentions that keep paying after the algorithm changes.

# Run the 7 steps in order

↳ Pull the whole top 10 and the videos, then read them properly.

↳ List what all ten already cover, and treat that list as mandatory.

↳ Collect the questions nobody on page one answers.

↳ Find the one claim the whole search result is missing.

↳ Design a study you can actually finish this week.

↳ Run it and compress it into one paragraph.

↳ Publish coverage plus your one new thing, then measure it.

The order is the point. Coverage first, your own contribution second.

👉[Use Distribb to run this playbook on every article you publish](https://abs.twimg.com/emoji/v2/svg/1f449.svghttps://distribb.io/?utm_source=infogain-aug15-xarticle)

[Th](https://abs.twimg.com/emoji/v2/svg/1f449.svghttps://distribb.io/?utm_source=infogain-aug15-xarticle)anks for reading.

Borja

# Sources

↳ Google Search: Optimizing your website for generative AI features: [https://developers.google.com/search/docs/fundamentals/ai-optimization-guide](https://developers.google.com/search/docs/fundamentals/ai-optimization-guide)

↳ Google Search: Creating helpful, reliable, people-first content: [https://developers.google.com/search/docs/fundamentals/creating-helpful-content](https://developers.google.com/search/docs/fundamentals/creating-helpful-content)

↳ Ahrefs: how many AI Overview citations come from the top 10: [https://ahrefs.com/blog/ai-overview-citations-top-10/](https://ahrefs.com/blog/ai-overview-citations-top-10/)

↳ Ahrefs: adding schema and AI citations: [https://ahrefs.com/blog/schema-ai-citations/](https://ahrefs.com/blog/schema-ai-citations/)

↳ Amsive: AI Overviews and click-through rate, 700,000 keywords: [https://searchengineland.com/guide/how-to-optimize-for-ai-overviews](https://searchengineland.com/guide/how-to-optimize-for-ai-overviews)
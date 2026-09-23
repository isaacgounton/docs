---
title: "how to actually sell a product (full guide)"
source: "https://x.com/everestchris6/status/2086835132695265586?s=46&t=12Nfhh8OAxVshqoN9SnZfQ"
author:
  - "[[@everestchris6]]"
published: 2026-08-10
created: 2026-08-21
description: "in the current age of ai, anyone can build a product, but almost nobody knows the proper way to market it. so here's the whole process:by ..."
tags:
  - "clippings"
---
![Image](https://pbs.twimg.com/media/HPXpNMjbIAA_T9f?format=jpg&name=large)

in the current age of ai, anyone can build a product, but almost nobody knows the proper way to market it. so here's the whole process: by the end of this you'll know how to work out exactly who your product is for, how to find where those people already are, and how to create something they'll actually stop for.

every prompt i use is written out in full, and at the end i've put the parts that can run on their own so you can set the whole thing up as you read

(fyi, i have never run a paid ad for anything i've sold. so everything here is the organic version)

this is the whole process i run before i make a single piece of content, and what i do once it's out.

![Image](https://pbs.twimg.com/media/HPWztx9a4AAYdQx?format=jpg&name=large)

the whole process

start with one person, not a market:

before anything else you decide who this is for. and it can't be "gamers" or "small business owners", because that's a category and nobody can picture a category.

you want one person. what they do all day, what annoys them, what they've already tried, what they'd scroll straight past. you keep narrowing until you can see them.

this feels like the boring part and it decides everything after it. the platform you post on comes out of it, and so do the words you use, and quite often the product itself changes once you've done it properly. if you get this wrong, you can make good content for six months and have it land on nobody.

the mistake here is picking the widest possible audience because it feels safer. it's the opposite. a wide audience means vague content, and vague content gets ignored by everyone including the people who would have bought.

get obsessed with them

i mean it. i personally write down everything.

demographics first, because they're easy. age, where they live, what they do for money, roughly what they earn etc.,

then psychographics, what they want and what they're scared of, how they see themselves and who they'd hate being mistaken for, and the thing about this problem they'd never admit out loud.

then i write out their day. what time they get up, what they're doing the first time they open their phone, what else is on the screen when my thing shows up, what mood they're in at that moment. writing a full day for a person who doesn't exist sounds stupid i know but it isn't. you make completely different content once you can picture who your target audience is

there's a difference between knowing facts about someone and knowing someone. the first one gets you generic content and the second is what makes a stranger feel like you're talking to them specifically.

go and look at their faces, here's something nobody really does.

open instagram, search the key term for your product, and find an account whose audience is the people you want. then go through the follower list and actually open them, so you're looking at their profile pictures and reading what they post. do 10-20 of those and you'll know these people better

![Image](https://pbs.twimg.com/media/HPWrdM2aIAAw41n?format=jpg&name=large)

instagram follower list

you'll notice things you'd never have guessed. how old they actually are versus how old you assumed, what other things they follow and things like that

i usually keep all of it in notion, one page per audience, and i go back and add to it whenever i learn something new.

here's a prompt that speeds this up

paste this into claude:

"i'm selling \[product\]. it costs \[price\]. build me a profile of the single person most likely to buy it.

give me:

demographics. age range, location, job, rough income, what device they're on most.

psychographics. what they want, what they're afraid of, how they see themselves, what they'd be embarrassed to admit about this problem.

a day in their life, hour by hour, from waking up to going to sleep. mark the moments where they'd be on their phone and what frame of mind they'd be in at each one.

what they've already tried for this problem and why it didn't work for them.

the words they'd use to describe the problem themselves. not marketing language, the actual phrasing a person would type.

three things that would make them immediately distrust someone selling this to them.

then tell me which parts of this you're confident about and which parts you're guessing, so i know what to go and verify."

then check the guesses against real people

go and read the subreddit for that problem. read the comments under the biggest videos in that space. go back through those instagram followers. you're looking for the places where the profile was wrong, and there usually will be some.

steal their words

this is the highest leverage thing in this entire process.

go and collect the actual sentences these people write about their problem from reddit threads, from youtube comments, from reviews of competing products. exactly as written, typos and all.

connect the apify MCP to claude, it's at [mcp.apify.com](https://mcp.apify.com/),

![Image](https://pbs.twimg.com/media/HPW207Ka0AAuO2p?format=jpg&name=large)

apify mcp connector on claude desktop

then ask for what you want in plain english. something like: using the apify MCP, find me a reddit scraper and pull every post and comment from r/whatever for the last three months. it finds the right scraper, runs it, and hands you back the data.

then you write using those words instead of yours. people describe their own problems in specific ways and it's almost never how a marketer would put it.

this is also how you find out what the product should be, because the complaint that keeps repeating is the thing to build.

the prompt:

"here is everything people posted about this problem in r/\[subreddit\] over the last three months. \[attach the file\]

pull out: the exact phrases that come up more than once, quoted as written. what they say they've already tried, and why it failed. the specific words they use for the emotion. not your summary of it, their words. what they're asking for that nobody seems to be giving them.

then tell me what a product would have to do to make these specific people happy, and what would make them ask for a refund."

![Image](https://pbs.twimg.com/media/HPWwemuaUAAjqbI?format=jpg&name=large)

language file

what to actually sell them

if you already have a product, this is where you find out whether it's the right one, and sometimes it isn't.

if you don't have one yet, the ideas are sitting in the file you just made.

keep the first product small. a guide, a template pack, a short course or a simple tool. the goal of the first product isn't to be impressive, it's to prove that you read those people correctly.

where they actually are

once you know the person, the platform picks itself. this is the bit most people get backwards, choosing the platform they like and then hunting for an audience there.

for example, if they're young you're on tiktok and instagram, and if they're older facebook still works while very little else does. gamers are on youtube and twitch, professionals are on linkedin and in a few specific subreddits, and people who are mid-problem and looking for a fix right now are on reddit and in google searches.

the prompt:

"my audience is \[paste the profile\].

tell me every platform and specific community where these people already gather. name the subreddits, the instagram and tiktok accounts they follow, the forums, the discord servers, the youtube channels, the facebook groups.

for each one, tell me roughly how many of them are in there, how people in that community talk, and what kind of post gets removed or downvoted.

then rank them by how easy it is to reach these people for free, and tell me which ones i should ignore and why."

![Image](https://pbs.twimg.com/media/HPWwnHHbAAA0Zcg?format=jpg&name=large)

ranked platform list

the "which to ignore" instruction is the useful half. anyone can list platforms. knowing which one to skip is what saves you a lot of time.

pick two and do them properly. spreading across six is how people end up doing all of them badly.

the rules that hold everywhere

these are the same on every platform, and once you understand them most of the tactical advice you read makes sense by itself.

packaging is what people actually buy. on youtube that means the title and the thumbnail, on tiktok it's the first frame and the first line you say out loud, and on reddit it's the post title on its own. that's the product as far as the viewer is concerned, and the thing you actually made is what gets delivered afterwards.

so decide the packaging first and build the thing to satisfy it. if you can't write a title and picture an image that you would personally stop for, the idea is weak, and it doesn't matter how good the content would have been.

the click and the hold are one number. people try to raise them separately and it backfires. a hook that overpromises gets the click and loses the person immediately, and every platform reads that pair as a bad experience and stops showing it. what you're actually working on is whether the click got rewarded fast.

you make things specifically for a person. the platform builds a picture of who your audience is and then goes looking for more of them. scattered output makes that picture incoherent and your reach falls even when the individual posts are good. keeping the format consistent matters more than posting on a schedule.

the first 2 seconds

on youtube the thumbnail only sits there for about two seconds now before the video starts playing on its own. so you get two seconds on the image and then the first five seconds of the video.

tiktok is harsher. the first frame and like the first three words, and if either one is soft they're gone.

what the image has to do is make someone ask a question they need the answer to.

the example i use is a thumbnail from valorant. a character is standing on top of a wall that shouldn't exist, and underneath her there are four people who have no idea she's there. you don't need to know the game. you look at it and you want to know how she got up there and what happens next. that video did 1.6 million views, and the same idea done a second time did 1.5 million.

![Image](https://pbs.twimg.com/media/HPWrtolbEAAvAWr?format=jpg&name=large)

thumbnail example

so before you design anything, write down the question you want the viewer to ask.

titles and hooks

two different jobs here, and they need opposite titles.

if it's going to be found in a feed, the title finishes the thought the image started without giving away the answer. what it must not do is repeat the image in words. that's a wasted slot and it's the most common mistake i see.

if it's going to be found in search, forget that. someone typed a specific thing and is scanning for the match, so you say plainly what it is using the words they typed. decide which one you're making before you write anything.

for a written post, the first sentence is doing both jobs at once. for a short video, it's the first line you say out loud.

the prompt i use:

"the content is about \[topic\]. my audience is \[paste profile\]. here's what the person will get out of it: \[payoff\].

give me 15 hooks. mix these types: a specific number, a mistake being named, a contradiction of something they already believe, a result stated plainly, a question they can't answer.

use the words my audience actually uses. no marketing language.

then for each one, tell me what it promises, and whether my content can actually deliver that. mark any hook that overpromises.

then rank the ones that are left and tell me why the top three are top."

a hook you can't pay off is worse than a weak hook, because it burns the person and the platform notices.

you open with the hook and that hook is a promise. then you tell it as a story, and the story is what carries the emotion, which is the actual point since nobody stays to the end of something they don't feel anything about. then you pay off the promise you made at the start.

test two of everything

i don't decide which version is better. i put both out and let it tell me.

two thumbnails per youtube video. two different hooks per tiktok/instagram. on reddit it's the same post under two different titles in two subreddits. same content underneath, different packaging on top.

then keep the three formats that are working and keep running new ones underneath them.

read the drop-off

the drop-off curve is the only honest feedback you get, and it's specific if you look at the shape.

a cliff in the first few seconds means the hook promised something the opening didn't deliver. fix the opening, not the hook. a slow steady slide means it's fine but too slow, so cut. a bump means people went back and watched something again, and whatever that was, do more of it. if there's no retention graph, you're reading the same thing off two numbers. on reddit it's views against comments, on x it's impressions against replies, in an email it's opens against clicks. the first number tells you about your packaging and the second tells you whether the thing delivered.

![Image](https://pbs.twimg.com/media/HPWr1ePbUAAodSU?format=jpg&name=large)

retention graph

one idea, every platform

once something works, it doesn't get copied and pasted everywhere. it gets repackaged.

the underlying idea stays the same while the packaging changes completely, because a title that works on youtube reads as clickbait on reddit and gets you removed.

so you keep the idea and the payoff, and you rebuild the hook and the format for each place using what you know about how that community talks. the audience profile does most of this work for you if you actually wrote it down.

![Image](https://pbs.twimg.com/media/HPWrjvzacAAlR93?format=jpg&name=large)

two things shifted recently that are worth knowing before you start.

thumbnails got cleaner and text on them does less than it used to. same on any platform with an image attached.

short form followers sometimes don't watch your long videos. people build a channel on short form, watch the subscriber count climb, and then find out that audience won't follow them across.

then you sell

this part is easy if everything before it was done properly.

you give real value in the open. you package it so people actually see it. you say what you're selling at the end, once the thing has already been useful on its own.

the reason it works is that you know exactly who you're talking to, so what you built is something they genuinely wanted. selling something people want to people you understand is not hard.

what you can leave running

do all of this by hand first until you know what a good one looks like. then you'll notice which parts you keep repeating, and those are the parts to put on an agent.

"pull new comments and threads from those communities every week and add anything new to the language file. the way people talk about a problem drifts, and new complaints appear that weren't there a month ago. this is the most useful thing to automate because it's pure collection and it never stops being useful."

"watch what's performing in the niche. top posts in those subreddits, videos gaining traction, formats starting to appear. you want to catch a format while it's still working rather than three months after everyone copied it."

"produce the packaging batch. two hook options and a couple of thumbnail concepts for whatever you're making next, written against the audience profile so it's already in the right language when you read it."

"refresh the audience profile once a month against the new comments, and have it tell you what changed rather than handing you a rewritten document."

then it pings you when there's something to look at, and you read it, fix what sounds wrong, and post it yourself.

what stays with you is judging whether something is any good, and answering anyone who replies. most people who can't sell anything have just never worked out who it was for.
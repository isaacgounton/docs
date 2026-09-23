---
title: Vibe Coding - MVP Rules
version: 1.0
date: 2026-09-22
updated: 2026-09-22
status: active
description: "Harshil Tomar's 18 do's and 18 don'ts for shipping MVPs fast: buy auth, payments, uploads, search and realtime; default Next.js stack; observability from day one; plus how the rules become AI-assistant instructions."
source:
  - "ingested/clippings/vibe-coding-2.0-18-rules.md"
  - "ingested/notes/vibe-coding-ai-instructions.md"
reliability: low
changes: "Created by wiki-ingest from Harshil Tomar Vibe Coding 2.0 post and prompt"
page_type: knowledge
---

# Vibe Coding - MVP Rules

> Harshil Tomar's 18 do's and 18 don'ts for shipping MVPs fast: buy auth, payments, uploads, search and realtime; default Next.js stack; observability from day one; plus how the rules become AI-assistant instructions.

---

## Overview

From someone claiming 50+ client MVPs: projects that should take 3 weeks take 3 months not because of bad code but because of bad **decisions before the code**, mainly rebuilding commodity pieces. The single principle: know what NOT to build. Spend your hours on the thing that makes the product unique, and hand everything else to mature services.

---

## The Default Stack

| Layer | Default | Replaces |
|---|---|---|
| Auth | Clerk or Supabase Auth | Hand-rolled sessions, OAuth |
| UI | Tailwind + shadcn/ui (Radix primitives) | Raw CSS, custom components |
| State | Zustand (client) + Server Components / React Query (server) | Redux, deep Context |
| API | tRPC + Next.js Server Actions | Custom REST |
| Data | Prisma + managed Postgres (Supabase, Neon, Railway) | Raw SQL, self-hosted DB |
| Forms | React Hook Form + Zod | Manual validation |
| Payments | Stripe (~45 min integration) | Anything custom (PCI) |
| Files | UploadThing or Cloudinary | DIY storage/CDN |
| Search | Algolia, Typesense, Meilisearch | Home-built search |
| Realtime | Supabase Realtime, Pusher, PartyKit | Hand-rolled websockets |
| Deploy | Vercel push-to-deploy + preview URL per PR | Manual deploys |
| Errors / logs | Sentry (also LogRocket, Axiom) | Finding out from users |
| Analytics | PostHog or Plausible | Guessing |
| Secrets | `.env` in `.gitignore`; Doppler or Vercel env in prod | Hardcoded keys |

---

## The Rules

### Buy, don't build

Auth, payments, file uploads, search and realtime are each months of edge cases (security, PCI, CDN, typo tolerance, conflict resolution). Use the service; migrate later only when real data says why.

### Keep it simple

- No Redux or custom REST for a product with 12 users: "don't build for 10 million users before you have 10".
- Use an ORM; raw SQL is harder to refactor and easier to get wrong on security.
- Tailwind covers ~99% of styling; Figma to working UI in 2-3 hours with shadcn.

### Ship safely

- Feature branches plus preview deployments, even solo; never push straight to main.
- Push-to-deploy only.
- Never commit secrets: GitHub scans public repos and providers like AWS revoke leaked keys.

### Observe from day one

Sentry and analytics before launch so data exists when you need it. Lighthouse audit before launch; under 70 is a red flag (usual culprits: unoptimised images, big JS bundles, render-blocking resources).

### Help users, and future you

- Onboarding, first-run tooltips and empty states: confused users leave.
- README from day 1 (run steps, env vars, core decisions): ~20 minutes that saves ~4 hours.
- Modular folders (components, hooks, utils, types).
- Record decisions and tradeoffs; don't rely on memory.
- Refactor after every 2-3 features.
- Don't chase perfect: the MVP's job is to learn.

> [!tip]
> Before building any component, ask: is there an existing service that does this, and do we need it to ship this week?

---

## Rules as AI-Assistant Instructions

A companion prompt (derived from the article, not by the original author) turns the rules into a system prompt for any AI coding assistant. Its structure:

| Section | What it tells the assistant |
|---|---|
| Core philosophy | Ship fast; build only what's unique; ship imperfect |
| Default stack | Next.js App Router plus the table above |
| Always / never rules | The 18 rules restated as hard constraints |
| Push-back scripts | If asked to build auth, CSS framework, Redux, REST, manual deploy, raw SQL or payments, question it with a one-line alternative |
| Project structure | `app/`, `components/ui` + `components/features`, `lib/` (db, auth, utils), `hooks/`, `types/`, `prisma/`, `README.md` |
| Done checklist | Lighthouse 70+, no console errors, optimised images, no huge bundles, analytics + Sentry, secrets in `.env`, README |
| Reminders | "Are we building for 10 million users or 10?", "Can we ship this week without this?" |

The useful idea is the **push-back clause**: the assistant is told to challenge scope creep rather than comply. In Claude Code this belongs in `CLAUDE.md` (see [[Claude Code - Working System]]) rather than being pasted per chat.

> [!note]
> The derived prompt hardens some nuance: "don't write raw CSS for everything" becomes "never write raw CSS", and "don't build custom APIs too early" becomes "never build custom REST APIs". It also fixes Next.js as the framework, which the article only implies.

---

## Related

[[AI & Agents - Home]] | [[Claude Code - Working System]] | [[Growth - First Users Without Ad Spend]]

---

## Sources

| Title | Publisher | Date | Links |
|---|---|---|---|
| Vibe Coding 2.0: 18 Rules to be the Top 1% Builder | Harshil Tomar, @Hartdrawss (X article) | 2026-02 | [Post](https://x.com/hartdrawss/article/2026198305362083910) · [[ingested/clippings/vibe-coding-2.0-18-rules]] |
| Vibe Coding AI Instructions (derived prompt) | Local note, derived from the above | 2026-02-25 | [[ingested/notes/vibe-coding-ai-instructions]] |

## Pending Review

> This page was created from a single non-authoritative source (the second file is derived from the first, so it does not corroborate). To raise trust: find two independent corroborating sources, and re-ingest or enrich this page. Key claims to verify: (1) Stripe integration takes ~45 minutes for an MVP; (2) Lighthouse <70 is the right pre-launch threshold; (3) the default stack covers "95%" of MVP needs.

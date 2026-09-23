---
title: Claude Code - Working System
version: 1.0
date: 2026-09-22
updated: 2026-09-22
status: active
description: "How to run Claude Code like an employee: repo workspace, CLAUDE.md/roadmap/review memory files, plan mode, tickets, visual QA, layered review, routines, parallel sessions, permissions, plus reusable sub-agent files."
source:
  - "ingested/clippings/Use Claude Code Better Than 99% of People (Full System).md"
  - "ingested/clippings/7-claude-sub-agents-that-replace-a-200k-team.md"
reliability: low
changes: "Created by wiki-ingest from Startup Ideas Pod and Nav Toor posts"
page_type: knowledge
---

# Claude Code - Working System

> How to run Claude Code like an employee: repo workspace, CLAUDE.md/roadmap/review memory files, plan mode, tickets, visual QA, layered review, routines, parallel sessions, permissions, plus reusable sub-agent files.

---

## Overview

The core claim across both sources: Claude performs best when treated as a delegate with a defined workspace, written context, a clear assignment and boundaries, not as a chat box. The first source (Startup Ideas Pod) lays out a nine-part operating system for a single product repo, demoed on a "missed-lead responder for med spas". The second (Nav Toor) packages recurring roles as sub-agent markdown files that each run in their own context window. Together they describe two layers: the **repo brain** that tells Claude how to work, and **specialist agents** that Claude can delegate to.

---

## The Nine-Part System

| # | Piece | What it is | Key practice |
|---|---|---|---|
| 1 | Workspace | A repo with purpose-named folders | Project explains itself |
| 2 | Memory files | `CLAUDE.md`, `roadmap.md`, `review.md` | Include an explicit out-of-scope list |
| 3 | Brief | Plan mode before edits | Force it to read the context files first |
| 4 | Ticket | One small task with a visible finish line | One task, one finish line, one reviewable change |
| 5 | Eyes | Claude runs the app and inspects it | Judge from the buyer's first 5 seconds |
| 6 | Review | Three layers: diff, review.md, /review | Must fix / should fix / okay to ship |
| 7 | Schedule | Routines for recurring work | Start with read-only operator tasks |
| 8 | Parallel agents | Separate sessions with worktree isolation | Each session = one assignment |
| 9 | Permissions | Safe / ask first / human owned | Start conservative, widen with trust |

### 1. Workspace layout

```text
repo/
├── CLAUDE.md        # how Claude works (style, business context, quality bar)
├── roadmap.md       # what matters this week + out of scope
├── review.md        # quality standards phrased as questions
├── app/             # the product
├── context/         # business brain (morning-brief.md, weekly-ops.md land here)
├── customers/       # sales calls, support notes, objections, customer language
├── specs/
├── demos/           # demo flows, loom scripts, screenshots
└── routines/        # recurring prompts
```

The setup prompt gives product, buyer, pain, promise and goal, then ends with "ask me for any missing context that would materially change the setup and keep the first version simple". That closing instruction makes Claude surface high-leverage questions before defaulting the rest.

### 2. Memory files

- **CLAUDE.md**: working style (small reviewable changes; explain the plan before behaviour-changing edits; follow existing code style; run relevant checks; summarise what changed, what was tested, what needs human review), plus business context and a quality bar (e.g. landing page clear in 5 seconds, works on mobile, uses customer language).
- **roadmap.md**: this week only, and an **out-of-scope** list (payments, CRM integration, admin dashboards, multi-user permissions). Scope limits keep the MVP focused.
- **review.md**: standards as questions. Matches roadmap? Small enough to review? Main flow still works? Mobile issues? Form errors handled? Auth/payment/production-data risk? Complexity we can cut? Is the offer clear in 5 seconds and the CTA visible?

### 3-4. Brief and ticket

Plan mode prompt pattern: inspect app + the three memory files, then return files to change, smallest clean implementation, UX, risks, verification plan, and what is intentionally left out; wait for approval. You then react (e.g. trim fields, connect to Supabase, leave auth alone).

| Good ticket | Bad ticket |
|---|---|
| Waitlist form collecting name, email, company, with success message | "Make the app better" |
| Pricing page using the existing design system | "Make this more viral" |
| Fix onboarding redirect after email verification | "Add AI" |
| Turn five customer objections into a landing section | "Build the whole thing" |

> [!tip]
> Vague prompts make Claude guess, and once it guesses you stop managing the work and start cleaning it up.

### 5. Eyes (self-verification)

Ask Claude to start the app, walk the flow as a first-time buyer, verify implementation (empty-form state, success state, backend record, console and network errors), report what is confusing or low-trust, then make **one** focused fix for the highest-impact issue. In the demo it found the page asked for an email before earning trust and added expectation-setting microcopy at the CTA.

### 6. Review in three layers

1. **Your own diff read**: does it match ticket and plan? Surprising changes (a waitlist ticket touching auth, routing, DB) are where risk lives.
2. **Claude against review.md**: classify issues as must fix / should fix / okay to ship; flag out-of-scope file changes and roadmap violations.
3. **`/review`** for normal work, a deeper "ultra" review before auth, payments or big features.

### 7. Routines

| Routine | Trigger | Output | Guardrail |
|---|---|---|---|
| Morning brief | Weekdays 7am | `/context/morning-brief.md`: top customer pain, one product risk, one build task, one customer question | No code changes, no PRs, <500 words |
| Weekly ops review | Fridays 3pm | `/context/weekly-ops.md`: grouped/duplicate issues, one highest-leverage fix | Leave code alone |
| PR review | PR opened | Comments only on bugs, broken flows, security, confusion; readiness summary | Uses review.md |

### 8. Parallel sessions

Separate Claude Desktop code sessions, each with its own context and worktree. Example morning: a bug session (returns root cause, files changed, checks run), a hero-copy session (before/after plus customer language used) and a demo-script session (script plus objection handled). Aim for small packets you can accept, revise or reject.

### 9. Permission buckets

| Safe | Ask first | Human owned |
|---|---|---|
| Read files, inspect code, plan, run local tests, edit a feature branch, update docs, open draft PR | Install deps, DB migrations, auth, payment logic, deleting files | Production deploys, customer-data decisions, billing, security-sensitive changes |

> [!warning]
> The source explicitly warns that YOLO / skip-permissions mode carries real risk. Contrast with [[AI Agents - Multi-Agent Orchestration]], which runs agents with permission bypass inside isolated worktrees.

### Skills, connectors, hooks

- **Skill**: any prompt typed twice. Suggested: landing-page teardown, customer-notes extraction (exact words, objections, buying triggers; the most valuable because it grounds copy in customer language), demo script (pain, product moment, payoff).
- **Connector**: richer context (GitHub, Linear, Google Drive, Slack).
- **Hook**: guardrails (format after edits, tests before PR summary).

### 7-day rollout

| Day | Action |
|---|---|
| 1 | Create repo brain: memory files, `/context`, `/customers`, definition of done |
| 2 | Plan mode on one small task |
| 3 | Build one visible improvement |
| 4 | Preview loop: Claude clicks through, checks mobile |
| 5 | Review diff against review.md |
| 6 | Send to 10 people; put replies in `/customers` |
| 7 | First routine (morning brief) |

---

## Sub-Agents as Specialist Roles

A sub-agent is a markdown file with YAML frontmatter (`name`, `description`) and a system prompt. In Claude Code it lives in `.claude/agents/<name>.md`; Claude can pick one automatically from its `description` or you invoke it. Each runs in its own context window, so it does not pollute the main thread. (The source also claims a Settings > Sub-Agents screen in Claude.ai, Desktop and Cowork; not verified.)

```markdown
---
name: researcher
description: Use when the user needs deep research ... flags contradictions.
---
You are a research analyst. You go deep, not wide.
When invoked: 1. ... 5. Return Findings / Contradictions / Open Questions.
Rules: never invent a citation ...
End every brief with: "Confidence: High / Medium / Low" ...
```

All seven share one design pattern: **role line, numbered "when invoked" steps, hard rules, and a forced closing sentence** that makes the agent commit to a verdict.

| Agent | Output shape | Notable rule | Forced closer |
|---|---|---|---|
| Researcher | 3 findings, 3 contradictions, 3 open questions + confidence | Primary sources only; never invent citations | "Confidence: H/M/L" |
| Editor | Draft ~30% shorter + "what I cut and why" | Stops if there is no thesis; banned buzzwords; no dashes | "The strongest line is ___" |
| Project Manager | One-page plan: milestones, owners, critical path, top 3 risks | Milestones must be falsifiable; say if deadline is unrealistic | "The project dies if ___ slips" |
| Analyst | Headline, 3 reasons, action, suggested chart | Never return raw tables | "If you do nothing else, do ___" |
| Recruiter | 5 specific channels, 5-line outreach, rubric, rejection email | No generic job boards; honest rejections | "The first call should answer ___" |
| Ops Lead | Process map tagged AUTOMATE / KILL / KEEP / DOCUMENT + SOP | Never automate a broken process; name the sacred human step | "Must never be automated: ___" |
| CFO | Runway, burn, bleeding line, ranked cut list | No "it depends" without a default; bold warning if runway <6 months | "You run out of money on ___" |

Suggested starter sets: solo founder (CFO, PM, Recruiter); freelancer (Researcher, Editor, PM); engineer (Researcher, Analyst, Ops Lead); creator (Researcher, Editor, Analyst). Install three, use daily for two weeks, add a fourth only when you catch yourself repeating a job.

> [!note]
> The "$780K of payroll replaced" framing (sum of seven salaries) and the title's "$200K" are marketing, not measured outcomes. Treat the agent files as prompt templates, not staff replacements.

---

## Related

[[AI & Agents - Home]] | [[AI Agents - Multi-Agent Orchestration]] | [[Vibe Coding - MVP Rules]] | [[AI Video - Faceless Videos with Claude Skills]] | [[GTM - Agent-Driven GTM Machine]]

---

## Sources

| Title | Publisher | Date | Links |
|---|---|---|---|
| Use Claude Code Better Than 99% of People (Full System) | @startupideaspod (X) | 2026-08-17 | [Post](https://x.com/startupideaspod/status/2089426109540729315) · [[ingested/clippings/Use Claude Code Better Than 99% of People (Full System)]] |
| The 7 Claude Sub-Agents That Replace a $200K Team | Nav Toor, @heynavtoor (X) | 2026-05-10 | [Post](https://x.com/heynavtoor/status/2053422550567502046) · [[ingested/clippings/7-claude-sub-agents-that-replace-a-200k-team]] |

## Pending Review

> This page was created from two practitioner posts on X, neither authoritative. To raise trust: check claims against Anthropic's Claude Code documentation, or find two independent corroborating sources, and re-ingest or enrich this page. Key claims to verify: (1) sub-agents can be added via a Settings > Sub-Agents screen in Claude.ai, Desktop and Cowork; (2) Claude Desktop's code tab runs parallel sessions with worktree isolation and an "ultra review" mode; (3) scheduled routines can run unattended on a cron-like schedule.

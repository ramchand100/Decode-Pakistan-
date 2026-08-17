---
name: decode-pakistan-content
description: Pre-production content workflow for the "Decode Pakistan" YouTube channel — a Think School-style explainer channel covering Pakistani business case studies, economics, geopolitics, and policy/history. Use this skill whenever the user asks to find video topics/ideas, brainstorm hooks or openings, write or outline a video script, research a Pakistani business/economic/political story for content, or update the channel's topic tracker — even if they don't say "Decode Pakistan" or "skill" explicitly, e.g. "give me some video ideas," "write me a hook for the sugar mafia story," or "draft the script for the PIA episode." Covers topics, hooks, and scripts only — not voiceover generation or video editing/assembly, which are handled separately once those tools are connected.
---

# Decode Pakistan — Content Workflow

Decode Pakistan is a research-driven explainer channel in the mold of Think School:
dense, well-sourced videos that make a Pakistani business, economic, or political story
feel like a story — with a hook, rising stakes, and a payoff insight — rather than a lecture.
This skill covers the three pre-production stages: finding topics, writing hooks, and
writing full scripts. It does not cover voiceover or video assembly (Remotion) — those are
separate, later stages the user will wire up once they provide voice/Remotion access.

Everything this skill produces should be usable by someone with zero context on the specific
episode — a topic idea should be pitchable in one line, a hook should work read cold, a script
should be recordable as-is.

## Where things live

- `content/topics.csv` — the running topic tracker. Every topic idea generated gets a row here
  so ideas persist across sessions instead of living only in chat history.
- `content/scripts/` — finished/in-progress scripts, one file per episode, named
  `YYYY-MM-DD-slug.md` (e.g. `2026-08-17-pia-privatization.md`).
- `references/pillars.md` — the four content pillars with what makes a story fit each one,
  plus worked examples. Read this before generating topics.
- `references/hook-patterns.md` — the four hook types with formulas and Pakistan-specific
  examples. Read this before writing hooks.
- `references/script-template.md` — the full script structure with a worked example. Read
  this before writing a script.

## Stage 1 — Finding topics

Read `references/pillars.md` first. The four pillars are: business case studies, economic
explainers, geopolitics, and policy/history. A good episode usually sits mainly in one pillar
but touches at least one other (a business case study about a textile mill collapse is also an
economic story about currency devaluation, for instance) — that overlap is often what makes a
topic strong rather than generic.

When asked for topic ideas:
1. Research current, real, verifiable stories — don't invent company names, statistics, or
   events. If you're not confident a detail is accurate, say so rather than presenting it as fact.
2. For each idea, write: the topic (one line), the pillar, and a one-line "why this works"
   angle — the specific tension, surprise, or stakes that makes it worth 12 minutes of someone's
   time. "Why this works" is not a summary of the topic; it's the reason a viewer who's never
   heard of this story would stay for the hook.
3. Favor specificity over breadth. "How Pakistan's textile industry lost its edge" is weaker
   than "How one Faisalabad mill's 2008 bet on cotton futures wiped out three family
   conglomerates" — specific stories have real hooks; category surveys don't.
4. Append new ideas as rows in `content/topics.csv` (create it from the template below if it
   doesn't exist yet) rather than only listing them in chat, so the tracker stays the source of
   truth. Don't duplicate a topic that's already in the tracker with status other than `idea`.

`content/topics.csv` columns: `id,date_added,pillar,topic,why_it_works,hook_angle,status,sources,notes`
— `status` is one of `idea`, `hooked`, `scripted`, `recorded`, `published`, `dropped`.
Leave `hook_angle` blank until Stage 2 fills it in, and `sources` blank until you have real
citations to put there.

## Stage 2 — Writing hooks

Read `references/hook-patterns.md` first. For a given topic, generate one hook per pattern
(question, shocking-stat, contrarian-claim, story-cold-open) — four total, not four variations
of the same one — so the user is actually choosing between different angles, not different
wordings. Each hook should be 1-3 sentences, exactly as it would be spoken on camera or in
voiceover, not a description of a hook.

After the user picks or the ideas are solid, record the winning hook_angle back into
`content/topics.csv` for that topic and update its status to `hooked`.

## Stage 3 — Writing scripts

Read `references/script-template.md` first. A script follows: hook → context → escalating
narrative → payoff/insight → CTA. The two things that separate this genre from generic
explainer content:

- **Escalation, not a list.** Each beat should raise the stakes or answer a question the last
  beat raised, not just add another fact. If a section could be reordered without changing
  anything, it's a list — restructure it so order matters.
- **Citations hold up to scrutiny.** Pakistani business/economics/politics content gets
  fact-checked hard in comments. Every non-obvious claim (a number, a date, a quote, an
  attribution of blame) needs an inline source note like `[Dawn, 2023]` or `[SBP annual report
  2022]` so the user can verify before recording. Never invent a citation — if you can't find
  or verify a source for a claim, flag it inline as `[NEEDS SOURCE]` rather than dropping the
  claim or making one up.

Save the finished script to `content/scripts/YYYY-MM-DD-slug.md` and update the topic's row in
`content/topics.csv` to status `scripted`.

## A note on judgment

Pakistani political and economic topics are often genuinely contested — don't flatten a story
to make it cleaner than it is. Where a topic has real disagreement about causes or blame (e.g.
who's responsible for a economic crisis), the strongest version of the video usually names the
competing explanations rather than picking one and presenting it as settled, unless the
evidence clearly favors one side.

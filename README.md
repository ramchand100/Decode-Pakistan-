# Decode Pakistan

Content project for a Think School-style YouTube channel covering Pakistani business case
studies, economics, geopolitics, and policy/history.

## Structure

- `.claude/skills/decode-pakistan-content/` — the Claude Code skill that handles the
  pre-production workflow: finding topics, writing hooks, and writing scripts. See its
  `SKILL.md` for details.
- `content/topics.csv` — running tracker of every topic idea, its pillar, hook angle, sources,
  and production status (`idea` → `hooked` → `scripted` → `recorded` → `published`).
- `content/scripts/` — finished and in-progress episode scripts.

## Roadmap

Voiceover generation (via a cloned voice) and automated video assembly (via Remotion) are
planned as later stages, once the relevant API/project access is connected. For now this repo
covers pre-production only: topics, hooks, and scripts.

# cstack

Chris Handy's agent-dotfiles: **skills**, rules, and evals for operating Chris OS and related agent workflows.

This repo is the source of truth for *procedures* (how agents should behave). Notion remains the source of truth for *wiki content* (commitments, projects, tasks, knowledge). Google Calendar is time. Chat is intake, not memory.

## Cursor plugin

cstack is a **personal local Cursor plugin** (same shape as [pstack](https://github.com/cursor/plugins/tree/main/pstack), tiny). It is not a marketplace listing.

- Manifest: [`.cursor-plugin/plugin.json`](.cursor-plugin/plugin.json)
- Skills path: `"skills": "./skills/"` — Cursor loads skills from that folder when the plugin is opened/installed
- Do **not** duplicate skills under `.cursor/skills/` or `.agents/skills/`

Open or install this repo as a Cursor plugin so `chris-os` (and future skills under `skills/`) load from the canonical path.

## Layout

```
.cursor-plugin/  # plugin.json (name, skills path, metadata)
skills/          # Canonical agent skills (one folder per skill, each with SKILL.md)
evals/           # Lightweight fixture prompts + expected behaviors (no heavy harness)
README.md        # This file
```

One true path for skills: **`skills/<name>/SKILL.md`**.

## Skills

| Skill | When |
| --- | --- |
| [`chris-os`](skills/chris-os/SKILL.md) | Operate Chris OS: inbox filing, ingest, wiki query, lint, board, weekday digest, routing to eggbot |

Add new skills as `skills/<name>/SKILL.md` with YAML frontmatter (`name`, pushy `description` that states what it does **and** when to use it). Keep bodies as checkable procedures that point at Notion URLs; do not paste the whole Operating Model into a skill.

## Grok Bot install

Grok Bot's skill library is a **copy** of skills from this repo, installed only when Chris says to copy. Agents must not self-install into Grok Bot. Live bots are only Chief of Staff and dr eggbot until eggbot mints specialists.

## Notion (Chris OS)

Canonical OS pages live in Notion. Start from Home and the Operating Model:

- [Chris OS — Home](https://app.notion.com/p/3bf204d753d581f6a395d32018e28295)
- [Operating Model](https://app.notion.com/p/3cb204d753d5812dbb92f61c598f27d2)
- [System](https://app.notion.com/p/3bf204d753d58111a9f3e82aedd49523)

## Evals

`evals/<skill>/` holds small prose fixtures (prompts + expected behaviors) for smoke-testing skill adherence. No runner required yet — read the fixtures and judge by hand or with a future pipeline.

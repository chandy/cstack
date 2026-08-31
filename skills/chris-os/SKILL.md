---
name: chris-os
description: >
  Operate Chris OS: route work between Notion (wiki/board), Google Calendar (time),
  and chat (intake only); file Knowledge and Task Inboxes; ingest meetings/clips;
  answer from the wiki with citations; lint the OS; run the weekday 7am ET digest;
  brief eggbot only for missing recurring specialist kinds. Use whenever operating
  Chris OS, deciding Notion vs skill vs eggbot, filing inbox items, compiling
  Granola/clips into Knowledge, querying commitments/projects/tasks, health-checking
  the wiki, keeping the board honest, or producing the morning digest. Do not skip
  this skill for Chris OS bookkeeping — chat is not memory.
---

# Chris OS

Operator playbook for Chris Handy's personal OS. Notion is the wiki (system of record for commitments, projects, tasks, knowledge). Google Calendar is time. Chat is intake, not memory.

Live Grok Bots are only **Chief of Staff** and **dr eggbot**. Specialists do not exist until eggbot mints them. Do not invent Writer, Researcher, Designer, Coder, Forge, Projects Manager, or any other standing bot.

Procedures and recurring corrections live in this skill (and siblings in this repo). Facts that change — today's tasks, this week's meetings, current Knowledge rows — live in Notion. Fetch the Operating Model before changing how the OS works.

## Canonical Notion

| Role | URL |
| --- | --- |
| Home | https://app.notion.com/p/3bf204d753d581f6a395d32018e28295 |
| System (catalog) | https://app.notion.com/p/3bf204d753d58111a9f3e82aedd49523 |
| Operating Model (schema) | https://app.notion.com/p/3cb204d753d5812dbb92f61c598f27d2 |
| Knowledge evergreen pointer | https://app.notion.com/p/3cd204d753d581c59d75dc2eed1ed358 |
| Library (browse-only) | https://app.notion.com/p/3bf204d753d581b3bcd8fcaa6987f617 |
| Tasks DB | https://app.notion.com/p/82c397de853448d5986abe67b296c679 |
| Knowledge DB | collection://207df5ce-542c-4ad5-b222-35577b8a1964 (id `9892d4fdce1a4af7a9f44db7fce62cb8`) |
| Projects DB | https://app.notion.com/p/5dcaafb9064541c5a5decc5638be1e80 |

Do not invent sibling schema pages. How the OS works → Operating Model. Where DBs live → System. Library is browse, not a parent for new OS docs.

## Systems of record

| Is SoR | Is not SoR |
| --- | --- |
| Notion — commitments, projects, tasks, knowledge | Apple Reminders |
| Google Calendar — personal, work, CK household, imported Outlook “Calendar” | Obsidian |
| | Local Mac assistant repo |
| | Slack / Teams threads |
| | Grok Bot chat transcripts |

Chat captures. Notion remembers. Calendar schedules.

## Authority

- Default: inspect, summarize, suggest.
- Reversible wiki/board edits may proceed (file Knowledge, update task status, draft on a page).
- Never email, publish, delete, pay, force-push, or deploy without Chris's explicit say-so.
- Do not silently overwrite wiki claims. Flag contradictions with both sources.

## Roster and routing

| Who | Does | Does not |
| --- | --- | --- |
| Chief of Staff | Operate Chris OS: ingest, query, lint, file both Inboxes, morning digest, keep the board honest, brief eggbot when a standing job is missing | Mint specialist bots; send email / publish / delete without Chris |
| dr eggbot | Design and create Grok Bots (one job, one voice, explicit anti-jobs) | Run the OS or do the specialist work it designed |

Routing rules:

1. Time, mail, inbox, wiki, board, “what today” → CoS (this skill).
2. Missing *kind* of recurring job (needs its own voice and anti-jobs) → brief eggbot. Do not CreateAgent for specialists yourself.
3. One-off → Task. Do not mint a bot for a one-off.
4. No Projects Manager bot. No standing Writer / Researcher / Designer / Coder / Forge.
5. Until a specialist is minted, CoS handles OS bookkeeping and does not fake a specialist role.

## Where things go (cstack vs Notion)

| Content | Home |
| --- | --- |
| Procedures, recurring corrections, checkable operator steps | Skills in this repo (`skills/`) |
| Wiki content: concepts, decisions, how-tos, commitments, board state | Notion |
| Schema / how the OS works | Operating Model (Notion) |
| Grok Bot skill library | A **copy** of skills from this repo, installed only when Chris says to copy. Never self-install into Grok Bot. |

If a rule matters twice, encode it here (or in the Operating Model), not as another chat reminder.

---

## Procedure: Ingest

Use when new material arrives (Granola, clip, bookmark, email, chat dump, Drive file).

1. Land it in **Knowledge Inbox** (do not leave load-bearing facts only in chat).
2. Set **Source** to one of: `Granola` | `Bookmark` | `Clip` | `Chat` | `Email` | `Manual`.
3. Compile into existing Knowledge pages when they exist; create a page when the concept is new.
4. Set **Area**, **Project**, and **Status** to `Processed` or `Evergreen` (Evergreen only if it will be reused).
5. Open a **Task** only when there is a clear next action.
6. If new data contradicts an existing page: flag both claims and sources. Do not silently overwrite.
7. Leave a row in Inbox when Chris must decide emphasis, or when the source is load-bearing.
8. Granola is a raw meeting source, not a second brain. Do not treat Granola as the archive.

One source may touch several pages. Routine Granola tagging can batch.

## Procedure: Query

Use when answering from the wiki (“what did we decide…”, “what's on the board…”, commitments/projects/knowledge).

1. Fetch the **Operating Model** if the question touches how the OS works.
2. Index first: Knowledge views / evergreen pointer, Tasks, Projects — then only the relevant pages.
3. Answer with citations (page titles + URLs).
4. File a useful answer back as Knowledge with `Source = Chat` so explorations compound.
5. Do not invent facts from chat memory when the wiki should have them.

## Procedure: Lint

Use when health-checking the wiki or when Chris asks to tidy the OS.

Check for: contradictions, stale claims, orphans, concepts with no page, missing Area/Project, Inbox leftovers.

1. Report findings with citations.
2. Turn real work into a **Task**.
3. Do not silently rewrite history.

## Procedure: Board

Use when keeping next actions honest.

1. Every Now project should have a clear next action on Tasks.
2. Progress belongs on the project/task page, not only in chat.
3. CoS owns board honesty. There is no Projects Manager bot.

## Procedure: Daily digest (weekdays 7am ET)

Produce **one** digest in Chief of Staff chat:

1. Shape of the day (from Calendar + board).
2. Overnight mail that needs a person — if it is a real next action, create a Task.
3. File Knowledge Inbox and Task Inbox (or report what remains and why).
4. Mention Notion in the digest only when something was filed or today depends on it.

## Procedure: Brief eggbot

Use only when a *kind* of job keeps showing up and needs a standing specialist.

Brief eggbot with: job, anti-jobs, board claimant yes/no, pstack yes/no (coding bots). Reuse and tighten before minting a duplicate. One-offs stay Tasks.

---

## Quick checks

Before acting, confirm:

- [ ] Am I treating chat as intake and Notion as memory?
- [ ] Am I pointing at canonical pages instead of inventing schema?
- [ ] Is this reversible, or does it need Chris's say-so?
- [ ] One-off → Task; recurring missing kind → eggbot brief; OS bookkeeping → CoS?
- [ ] Did I avoid inventing specialist bots?

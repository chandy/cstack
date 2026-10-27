---
name: chris-os
description: >-
  Use whenever operating Chris OS: filing inboxes, ingesting Granola/clips,
  querying the wiki, linting, keeping the board honest, running the weekday
  digest handoff to Digest, or deciding Notion vs skill vs eggbot. Chat is not
  memory. Fetch Chris (working context) when who he is or how to operate with
  him matters.
---
# Chris OS

Operator playbook for Chris Handy's personal OS. Notion is the wiki (system of record for commitments, projects, tasks, knowledge). Google Calendar is time. Chat is intake, not memory.

Standing specialists come from **dr eggbot** only. Do not invent Writer, Researcher, Designer, Coder, Forge, Projects Manager, or any other standing bot.

Procedures and recurring corrections live in this skill (and siblings in cstack). Facts that change — today's tasks, this week's meetings, current Knowledge rows — live in Notion. Fetch the Operating Model before changing how the OS works. Fetch **Chris (working context)** before planning his day, drafting as him, or making tradeoffs that touch health, family, or career.

## Canonical Notion

| Role | URL |
| --- | --- |
| Home | https://app.notion.com/p/3bf204d753d581f6a395d32018e28295 |
| System (catalog) | https://app.notion.com/p/3bf204d753d58111a9f3e82aedd49523 |
| Operating Model (schema) | https://app.notion.com/p/3cb204d753d5812dbb92f61c598f27d2 |
| Chris (working context) | https://app.notion.com/p/3cd204d753d581fc862fef82597599c2 |
| Knowledge evergreen pointer | https://app.notion.com/p/3cd204d753d581c59d75dc2eed1ed358 |
| Library (browse-only) | https://app.notion.com/p/3bf204d753d581b3bcd8fcaa6987f617 |
| Tasks DB | https://app.notion.com/p/82c397de853448d5986abe67b296c679 |
| Knowledge DB | collection://207df5ce-542c-4ad5-b222-35577b8a1964 (id `9892d4fdce1a4af7a9f44db7fce62cb8`) |
| Projects DB | https://app.notion.com/p/5dcaafb9064541c5a5decc5638be1e80 |
| Adopt Chris OS (source migration) | https://app.notion.com/p/3bf204d753d581c2a089c78f07284e8b |

Do not invent sibling schema pages. How the OS works → Operating Model. Who Chris is / how to work with him → Chris (working context). Where DBs live → System. Library is browse, not a parent for new OS docs. Life snapshots (history, family, ADHD, money/home) are supporting depth, not the front door.

## Systems of record

| Is SoR | Is not SoR |
| --- | --- |
| Notion — commitments, projects, tasks, knowledge | Apple Reminders |
| Google Calendar — personal, work, CK household, imported Outlook “Calendar” | Obsidian |
| | Local Mac assistant repo (`asst`) |
| | Slack / Teams threads |
| | Grok Bot chat transcripts |

Chat captures. Notion remembers. Calendar schedules. Competing sources get compiled into the wiki, then left as archive on disk. Do not delete Mac files without Chris's say-so.

**CK** is Chris and Katrina's shared household calendar. Not every event on it is Chris's. Do not treat Katrina's medical or other personal appointments as his. Only treat a CK event as his (agenda or conflict) when he is clearly the attendee, or it is a household event he is going to (school, family outing). If ownership is ambiguous, list it as household context, not as his meeting.

## Authority

- Default: inspect, summarize, suggest.
- Reversible wiki/board edits may proceed (file Knowledge, update task status, draft on a page).
- Never email, publish, delete, pay, force-push, or deploy without Chris's explicit say-so.
- Do not silently overwrite wiki claims. Flag contradictions with both sources.
- Do not recap compensation dollars in chat.
- Do not manage medical care from wiki pages.

## Roster and routing

| Who | Does | Does not |
| --- | --- |
| Grok Bot | Operate Chris OS: ingest, query, lint, file both Inboxes, keep the board honest, brief eggbot when a standing job is missing | Mint specialist bots; send email / publish / delete without Chris; run the weekday morning digest timer |
| Digest | Weekday 6:30 ET morning digest in its own short chat (calendars, actionable overnight mail, Inbox filing for the digest, one prep item) | Rest of Chris OS; mint bots |
| dr eggbot | Design and create Grok Bots (one job, one voice, explicit anti-jobs) | Run the OS or do the specialist work it designed |
| Trace | TypeScript / mepo / evals teaching | Chris OS; Bridgewater coaching |
| Harness | Agent-harness product+tech watch (Pi + OpenCode primary; Muse / Cursor / Grok secondary); Notion Knowledge notes; weekday 9:00 ET light check | Chris OS; Tasks board; coding shipping |

Routing rules:

1. Time, mail, inbox, wiki, board, “what today” (ad-hoc) → Grok Bot.
2. Weekday morning digest delivery → Digest chat (not Grok Bot).
3. Agent harness product/tech intel (Pi, OpenCode, Muse, Cursor, Grok) → Harness.
4. Missing *kind* of recurring job (needs its own voice and anti-jobs) → brief eggbot. Do not CreateAgent for specialists yourself.
5. One-off → Task. Do not mint a bot for a one-off.
6. No Projects Manager bot. No standing Writer / Researcher / Designer / Coder / Forge.
7. Until a specialist is minted, Grok Bot handles OS bookkeeping and does not fake a specialist role.

## Where things go (cstack vs Notion)

| Content | Home |
| --- | --- |
| Procedures, recurring corrections, checkable operator steps | Skills in cstack (`skills/`) |
| Wiki content: concepts, decisions, how-tos, commitments, board state | Notion |
| Schema / how the OS works | Operating Model (Notion) |
| Who Chris is / how to operate given those facts | Chris (working context) |
| Grok Bot skill library | A **copy** of skills from cstack, installed only when Chris says to copy. Never self-install into Grok Bot. |

If a rule matters twice, encode it in cstack (or in the Operating Model), not as another chat reminder.

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
9. If the source changes who Chris is or how to work with him, update **Chris (working context)** and keep supporting pages as depth.

One source may touch several pages. Routine Granola tagging can batch.

## Procedure: Query

Use when answering from the wiki (“what did we decide…”, “what's on the board…”, commitments/projects/knowledge).

1. Fetch the **Operating Model** if the question touches how the OS works.
2. Fetch **Chris (working context)** if the question touches who he is, priorities, constraints, or how to plan/talk with him.
3. Index first: Knowledge views / evergreen pointer, Tasks, Projects — then only the relevant pages.
4. Answer with citations (page titles + URLs).
5. File a useful answer back as Knowledge with `Source = Chat` so explorations compound.
6. Do not invent facts from chat memory when the wiki should have them.

## Procedure: Lint

Use when health-checking the wiki or when Chris asks to tidy the OS.

Check for: contradictions, stale claims, orphans, concepts with no page, missing Area/Project, Inbox leftovers, working-context drift vs later facts (e.g. employment).

1. Report findings with citations.
2. Turn real work into a **Task**.
3. Do not silently rewrite history.

## Procedure: Board

Use when keeping next actions honest.

1. Every Now project should have a clear next action on Tasks.
2. Progress belongs on the project/task page, not only in chat.
3. Grok Bot owns board honesty. There is no Projects Manager bot.
4. **Queue** is when: Inbox, This week, Next, Waiting, Someday. **Priority** is what to do first in that window: High / Medium / Low. High is today's first work. Leave Priority empty unless it actually matters. Do not backfill Medium on every row.
5. When filing a task that is the day's focus, set Queue = This week and Priority = High.

## Procedure: Daily digest (weekdays 6:30am ET)

Owned by **Digest** bot — deliver in Digest chat, not Grok Bot.

Produce **one** digest:

1. Shape of the day (from Calendar + board), bounded by working-context constraints (family load, small surface, one next action). Name **High** tasks first.
2. Overnight mail that needs a person — if it is a real next action, create a Task.
3. File Knowledge Inbox and Task Inbox (or report what remains and why).
4. Mention Notion in the digest only when something was filed or today depends on it.
5. **CK calendar:** Chris and Katrina share it. Do not treat every CK event as Chris's. Katrina medical stays hers. Only flag conflicts for events he is attending.

Grok Bot must not keep a competing morning-digest timer.

## Procedure: Brief eggbot

Use only when a *kind* of job keeps showing up and needs a standing specialist.

Brief eggbot with: job, anti-jobs, board claimant yes/no, pstack yes/no (coding bots). Reuse and tighten before minting a duplicate. One-offs stay Tasks.

---

## Quick checks

Before acting, confirm:

- [ ] Am I treating chat as intake and Notion as memory?
- [ ] Am I pointing at canonical pages instead of inventing schema?
- [ ] Did I fetch working context when who/how matters?
- [ ] Is this reversible, or does it need Chris's say-so?
- [ ] One-off → Task; recurring missing kind → eggbot brief; OS bookkeeping → Grok Bot?
- [ ] Did I avoid inventing specialist bots?
- [ ] Is weekday digest on Digest, not Grok Bot?

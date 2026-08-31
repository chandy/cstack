# chris-os evals

Tiny fixtures for smoke-testing the `chris-os` skill. Expected behaviors are prose, not a harness.

## Fixture: file this Granola note

**Prompt:** A Granola transcript from today's 1:1 landed. File it.

**Expect:**

- Treat Granola as a raw source (`Source = Granola`), not a second brain.
- Land / compile into Knowledge Inbox → existing pages if they exist, else a new Knowledge page.
- Set Area, Project, Status = Processed or Evergreen.
- Open a Task only if there is a clear next action.
- Flag contradictions instead of silently overwriting.
- Do not invent specialist bots; CoS does the filing.

## Fixture: where does this belong

**Prompt:** Should this recurring “weekly research brief” job become a Notion Task, a skill in cstack, or a new Grok Bot?

**Expect:**

- Procedures / recurring corrections → skill in this repo (if Chris wants it encoded).
- Wiki content and one-off next actions → Notion (Task for a one-off).
- Missing *kind* of recurring specialist work that needs its own voice → brief eggbot; do not CreateAgent yourself.
- Do not self-install into Grok Bot's skill library unless Chris asks to copy.
- Live bots remain only Chief of Staff and dr eggbot until eggbot mints someone.

# Deutsch bewegt! — Project Guide

## What this project is

Website for the **"Deutsch bewegt!"** event (Goethe-Institut): an external
bilingual site (German / Greek) that hosts info, program, workshop sign-ups,
certificates, evaluation, a partners-only area, and an archive of previous
years.

Full offer and functional spec: [Specs/Goethe offer Deutsch bewegt website.md](Specs/Goethe%20offer%20Deutsch%20bewegt%20website.md)

## Who works in this repo

Two collaborators with different modes:

- **Panagiotis — developer.** All code, infrastructure, implementation.
- **Konstantina — research & project management.** No coding tasks.
  Her workspace is [pm/](pm/) — follow [pm/CLAUDE.md](pm/CLAUDE.md) when
  working there.

## Persona inference — don't ask, infer

Do **not** start sessions with "who am I talking to?". Infer from context:

1. **Working directory.** If CWD is inside `/pm`, assume PM persona
   (Konstantina) and apply [pm/CLAUDE.md](pm/CLAUDE.md). Otherwise, assume
   developer (Panagiotis).
2. **First-message signals** sharpen the inference:
   - Greek + research / meeting / stakeholder / email / decision-log /
     timeline tasks → PM.
   - English + code / infra / deploy / refactor / tech-decision tasks → dev.
3. **Confirm only when signals conflict** — e.g. a clearly PM task at repo
   root, or a clearly dev task while in `/pm`. A one-line check is enough:
   *"Quick check — is this PM work or dev work? (sets how I proceed.)"*

Default behavior rules:

- Inside [pm/](pm/), `pm/CLAUDE.md` extends and overrides this file.
- Everywhere else, full developer mode.
- Never modify files in `/pm` during dev tasks without explicit request —
  that's the PM workspace.

## Response style

**Short by default, expand when needed.**

- Default: brief and direct. Answer, state results, move on. No preamble ("great question!"), no rehash of what the user just said, no over-summarizing.
- Expand when: the question is genuinely complex, meaningful tradeoffs are worth surfacing, or a decision depends on information the user doesn't have yet.
- Headings, tables, and bullet lists earn their place when information is parallel or complex. For simple answers, one paragraph — or one line — beats a structured list.
- One-line updates during tool use (*"reading the spec", "creating the task"*) are fine; silence isn't.

## Task management

Tasks live in **ClickUp**; the repo owns scope and durable context. They reference each other — they don't mirror.

- **ClickUp list:** **Goethe** (`901510874240`) — path `Workspace > Team Space > Clients > Goethe`. MCP server: `clickup-pnk`.
- **ClickUp** for anything with lifecycle state: work items, assignees, due dates, dependencies.
- **Repo markdown** for scope ([deliverables.md](deliverables.md)), decisions, research, stakeholders, meeting notes.

### For Claude

- "Create a task / what's open / due this week?" → use the ClickUp MCP (`clickup-pnk`) against the **Goethe** list (`901510874240`).
- "What was promised / note this decision / summarize the meeting?" → repo markdown.
- **Crossover:** action items captured in meeting notes get created as ClickUp tasks, with the task IDs/URLs pasted back into the note for traceability.
- **Scope vs work:** [deliverables.md](deliverables.md) checkboxes reflect *organizer sign-off* — a scope state. A ClickUp task can be "done" for weeks before the corresponding checkbox is ticked.

### Light ClickUp convention (to seed before the list grows)

- **Custom field `spec_ref`** (text) — e.g. `A8#4`, `A6.8` — cross-reference to the offer spec.
- **Tags** — `phase-1` / `phase-2` / `phase-3` for lifecycle; `pm` / `dev` / `organizer` for who's acting.

## Tech stack

_TBD — to be decided before implementation. Document here once set._

## Product constraints worth remembering (from the spec)

- **Bilingual parity.** Every page must exist in DE and EL, with clear language
  toggle.
- **Hosted outside `goethe.de`.** Linked from the Goethe-Institut site, not
  under its domain.
- **Certificates** go only to users who registered online **and** have
  `status = "attended"`.
- **GDPR** on every form (signup, evaluation, marketing consent).
- **Admin panel** must be usable by non-technical organizers (exports to CSV/Excel,
  manual resend, manual certificate issuance).
- **Email deliverability** matters — a third-party sending service will be used;
  bounce/failure handling via resend.
- **QR check-in is optional** (+€480); fallback is an uploaded "attended" list.

## Cost & timeline baseline (from offer)

- Development: **€4.200 + VAT** (lump sum on delivery).
- Yearly hosting, support, content refresh: **€700 / year + VAT**.
- Optional QR check-in: **€480 + VAT**.
- Timeline: **10–12 weeks** from kickoff and receipt of material.

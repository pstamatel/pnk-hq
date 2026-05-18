# PnK Software Solutions — HQ

Operational hub for **PnK Software Solutions**: client engagements, internal admin, and project management. This repo holds **scope, context, and coordination** — application code for individual projects lives elsewhere (separate repos per project, or as decided per engagement).

## Structure

```
pk-hq/
├── CLAUDE.md                       ← this file (PnK-wide rules)
├── .mcp.json                       ← ClickUp MCP wiring (PnK-wide)
├── clients/<client>/<project>/     ← per-project workspace, with its own CLAUDE.md
└── pnk/                            ← (future) internal PnK matters: capacity, invoicing, admin
```

Currently active engagements:

- [clients/goethe/deutsch-bewegt/](clients/goethe/deutsch-bewegt/) — bilingual event website for Goethe-Institut.

## Who works in this repo

Two collaborators / co-founders:

- **Panagiotis** — all code, infrastructure, technical decisions. Comfortable with both Greek and English.
- **Konstantina** — digital marketing, research, project management. Non-technical. Her workspace inside any project is `*/pm/`, governed by that project's `pm/CLAUDE.md`.

Persona labels in this repo are **always the names** (`panagiotis`, `konstantina`) — never role-based aliases like `dev` or `pm`. A name carries both identity (who is at the keyboard) and typical mode (the kind of work they usually do), but it does not lock the mode: Panagiotis sometimes does PM work; Konstantina is doing more business-side work over time. The current task signals which mode to operate in.

## Persona resolution — don't ask, resolve

Do **not** start sessions with "who am I talking to?". Resolve in this order:

1. **Explicit in-session instruction wins.** *"I'm Konstantina right now"* → use that and stop.
2. **`CLAUDE.local.md` at repo root** (gitignored, per-machine). If it contains `persona: panagiotis` or `persona: konstantina`, treat it as the default persona for this session.
3. **Fallback: infer from context** (language is *not* a signal — both write in both languages):
   - **Working directory.**
     - CWD inside any `*/pm/` subdir → assume Konstantina; apply the nearest `pm/CLAUDE.md`.
     - CWD inside `clients/<client>/<project>/` (not under `pm/`) → assume Panagiotis, project-scoped.
     - CWD at repo root or `pnk/` → assume Panagiotis, PnK-wide / cross-client work.
   - **Task type sharpens the inference.**
     - Research / meeting notes / stakeholder / email drafts / decision log / timeline / client-facing artifacts → leans Konstantina.
     - Code / infra / deploy / refactor / tech decisions / repo structure → leans Panagiotis.
4. **Confirm only when signals conflict with the active persona** — e.g. `persona: konstantina` is set but the request is *"deploy this to prod"*, or a clearly Konstantina-shaped task at repo root with no `CLAUDE.local.md`. One-line check: *"Quick check — is this Panagiotis or Konstantina work? (sets how I proceed.)"*

### When Panagiotis does PM-style work (or vice versa)

The active persona stays the same (the person hasn't changed), but adapt the *mode* to the task:

- Apply the PM workspace conventions ([`pm/CLAUDE.md`](clients/goethe/deutsch-bewegt/pm/CLAUDE.md)) for templates and file conventions, regardless of who's doing it.
- Keep response language matching what the user wrote.
- Don't impose Konstantina-specific constraints (e.g. "no dev commands") on Panagiotis just because he's doing PM-style work.

### Default behavior rules

- Inside `*/pm/`, the project's `pm/CLAUDE.md` extends and overrides this file.
- Inside `clients/<client>/<project>/`, that project's `CLAUDE.md` extends and overrides this file.
- Never modify files in another client's directory while working on a given client, unless explicitly asked.
- Never modify files under any `pm/` during code/infra tasks without explicit request — that's the PM workspace.

## Cross-client confidentiality

Multiple clients live in this repo.

- **Never reference one client's information in artifacts produced for another client.** Treat each `clients/<X>/` as a sealed context for outbound work.
- When asked cross-client questions internally ("which clients have overdue invoices?", "where am I overcommitted?"), it is fine to read across — but only for internal answers to Panagiotis, never in client-facing output.
- If a client's contract requires hard data isolation, that client gets its own separate repo — flag the conflict rather than working around it here.

## Response style

**Short by default, expand when needed.**

- Default: brief and direct. Answer, state results, move on. No preamble ("great question!"), no rehash of what the user just said, no over-summarizing.
- Expand when: the question is genuinely complex, meaningful tradeoffs are worth surfacing, or a decision depends on information the user doesn't have yet.
- Headings, tables, and bullet lists earn their place when information is parallel or complex. For simple answers, one paragraph — or one line — beats a structured list.
- One-line updates during tool use (*"reading the spec", "creating the task"*) are fine; silence isn't.

## Task management

Tasks live in **ClickUp**; the repo owns scope and durable context. They reference each other — they don't mirror.

- **ClickUp** for anything with lifecycle state: work items, assignees, due dates, dependencies. MCP server: `clickup-pnk`.
- **Repo markdown** for scope, decisions, research, stakeholders, meeting notes.
- **Each project's CLAUDE.md** names that project's ClickUp list ID and any project-specific conventions.

### For Claude

- "Create a task / what's open / due this week?" → use the ClickUp MCP (`clickup-pnk`) against the **active project's list** (named in that project's CLAUDE.md).
- "What was promised / note this decision / summarize the meeting?" → repo markdown, inside the relevant project directory.
- **Crossover:** action items captured in meeting notes get created as ClickUp tasks, with the task IDs/URLs pasted back into the note for traceability.
- **Scope vs work:** project `deliverables.md` checkboxes reflect *client sign-off* — a scope state. A ClickUp task can be "done" for weeks before the corresponding checkbox is ticked.

### Shared ClickUp conventions

- **Custom field `spec_ref`** (text) — cross-reference into the project's spec (e.g. `A8#4`, `A6.8`).
- **Tags** — `phase-1` / `phase-2` / `phase-3` for lifecycle; `panagiotis` / `konstantina` / `client` for who's acting.

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

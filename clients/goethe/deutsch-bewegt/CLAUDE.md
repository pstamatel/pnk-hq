# Goethe-Institut — Deutsch bewegt! website

Project-specific context. Extends the PnK-wide [root CLAUDE.md](../../../CLAUDE.md).

## What this project is

Website for the **"Deutsch bewegt!"** event (Goethe-Institut): an external bilingual site (German / Greek) that hosts info, program, workshop sign-ups, certificates, evaluation, a partners-only area, and an archive of previous years.

Full offer and functional spec: [Specs/Goethe offer Deutsch bewegt website.md](Specs/Goethe%20offer%20Deutsch%20bewegt%20website.md)
Contract summary: [Specs/Goethe offer Deutsch bewegt website - contract summary.md](Specs/Goethe%20offer%20Deutsch%20bewegt%20website%20-%20contract%20summary.md)
Deliverables tracker: [deliverables.md](deliverables.md)

## ClickUp

- **List:** **Goethe** (`901510874240`) — path `Workspace > Team Space > Clients > Goethe`.
- All Deutsch bewegt! tasks live in this list. Use the `clickup-pnk` MCP server.

## Tech stack

_TBD — to be decided before implementation. Document here once set. Implementation likely lives in a separate repo (decision pending)._

## Product constraints worth remembering (from the spec)

- **Bilingual parity.** Every page must exist in DE and EL, with clear language toggle.
- **Hosted outside `goethe.de`.** Linked from the Goethe-Institut site, not under its domain.
- **Certificates** go only to users who registered online **and** have `status = "attended"`.
- **GDPR** on every form (signup, evaluation, marketing consent).
- **Admin panel** must be usable by non-technical organizers (exports to CSV/Excel, manual resend, manual certificate issuance).
- **Email deliverability** matters — a third-party sending service will be used; bounce/failure handling via resend.
- **QR check-in is optional** (+€480); fallback is an uploaded "attended" list.

## Cost & timeline baseline (from offer)

- Development: **€4.200 + VAT** (lump sum on delivery).
- Yearly hosting, support, content refresh: **€700 / year + VAT**.
- Optional QR check-in: **€480 + VAT**.
- Timeline: **10–12 weeks** from kickoff and receipt of material.

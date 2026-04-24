# Deliverables & Commitments Tracker

_Every commitment from the offer ([Specs/Goethe offer Deutsch bewegt website.md](Specs/Goethe%20offer%20Deutsch%20bewegt%20website.md)). Organized around the 13 contractual deliverables in §A8, plus the add-on in scope (QR check-in), commercial terms, phase gates, and responsibilities. Check each item as it is delivered and accepted by the organizer._

**Status legend:** `[ ]` not started · `[~]` in progress · `[x]` delivered & accepted

**Section codes** refer to the offer spec (A1–A9, B1–B3).

---

## Cross-cutting constraints

Apply across every deliverable:

- [ ] **Hosted outside `goethe.de`** — A1, A8#1
- [ ] **Full DE/EL content and navigation parity**, with clear language toggle — A4, A8#1
- [ ] **Responsive design** (mobile + desktop) — A3
- [ ] **Modern aesthetic** that fits the project identity — A2
- [ ] **Inbound link from goethe-institut.de** to the site — A1 _(organizer-side action)_

---

## A8 Deliverables

### 1. External bilingual website (DE/EL), outside `goethe.de`
- [ ] Full parity of content and navigation across both languages — A8#1, A4
- [ ] Freely accessible on the public internet — A1

### 2. Final site structure & core pages
Final site map and content hierarchy agreed with organizers at kickoff (A3). Indicative pages:
- [ ] Home / Info — A3, A8#2
- [ ] Program — A3, A8#2
- [ ] Workshops — A3, A8#2
- [ ] Registration — A3, A8#2
- [ ] Evaluation — A3, A8#2
- [ ] Archive of previous years — A3, A8#2
- [ ] Partners-only area — A3, A8#2
- [ ] Contact — A3, A8#2
- [ ] Policies (GDPR / Cookies) — A3, A8#2, A8#12

### 3. Per-year program & past-year archive
- [ ] Workshops / sessions and speakers organized per year — A6.1, A8#3
- [ ] Past-year programs viewable via menu with clear per-year navigation — A6.7, A8#3
- [ ] **Selected past-year photo material** hosted in the archive — A2
- [ ] _Optional:_ host additional past-year material (digital flyers, posters, etc.) if material is provided and access policy is agreed — A6.7

### 4. Workshop sign-up system
- [ ] Each workshop displayed with title, time, description, speakers/εισηγητές — A6.2
- [ ] User selects which workshops to attend — A6.2
- [ ] Registration form — **required fields: email, name, organization (φορέας)** _(decided scope)_ — A6.2, A8#4
- [ ] Secure storage of registration data — A6.2, A8#4
- [ ] Table view of registrations in admin panel — A6.2, A8#4
- [ ] Export registrations to CSV / Excel — A6.2, A8#4

### 5. Admin panel (for non-technical organizers)
- [ ] Manage registrations — A7, A8#5
- [ ] Basic email sends — A7, A8#5
- [ ] Manage certificates — A7, A8#5
- [ ] Manage evaluation results — A7, A8#5
- [ ] Mark / correct participant attendance status (manual correction path) — A7, A6.4, A6.8

### 6. Automated emails
- [ ] Registration confirmation email — A6.3, A8#6
- [ ] Instructions / info emails (access, hours, useful info) — A6.3, A8#6
- [ ] Custom email template aligned with site aesthetic — A6.3, A8#6
- [ ] Email-sending service license & setup procured by PnK — A6.3
- [ ] Consent-at-registration option for future-event updates — A6.3
- [ ] Separate newsletter signup form — A6.3

### 7. Failure notification & resend
- [ ] Failure notification to organizers (emails or certificates) — A6.3, A6.4, A8#7
- [ ] Manual resend from admin panel — A6.3, A6.4, A8#7

### 8. Certificates of attendance
- [ ] PDF template — aesthetics and content agreed with organizer — A6.4, A8#8
- [ ] Automatic generation with participant name — A6.4, A8#8
- [ ] Automatic sending by email only to registered + status `"attended"` — A6.4, A8#8
- [ ] Attendance source — **primary: QR check-in**; **fallback: organizer-fed "attended" list / manual correction** — A6.4, A6.8
- [ ] Manual certificate issuance — name (+ optional email), downloadable and optionally emailed — A6.4, A8#8

### 9. Evaluation form
- [ ] Evaluation form embedded in the site (project + event) — A6.5, A8#9
- [ ] Store responses — A8#9
- [ ] Export results to CSV / Excel via admin — A6.5, A8#9
- [ ] Automatic thank-you email after submission — A6.5, A8#9
- [ ] _Optional:_ match evaluation email against registration email (stats only) — A6.5

### 10. Partners-only area
- [ ] Password-protected section — A6.6, A8#10
- [ ] Promo material uploaded & organized (downloadable files) — A6.6, A8#10
- [ ] PnK uploads material within reasonable time after receipt from organizer — A6.6

### 11. SEO, social preview, accessibility basics
- [ ] Clean URLs — A5
- [ ] Proper titles and meta descriptions — A5
- [ ] Proper content structure — A5
- [ ] sitemap.xml — A5, A8#11
- [ ] robots.txt — A5, A8#11
- [ ] Open Graph / social preview tags — A5, A8#11
- [ ] EL / DE version recognition (hreflang) — A5
- [ ] Good loading speed — A5, A8#11
- [ ] Basic accessibility — A5, A8#11

### 12. Policy pages & GDPR basics
- [ ] Privacy / cookies policy pages published — A8#12
- [ ] GDPR compliance on registration form — A8#12
- [ ] GDPR compliance on evaluation form — A8#12
- [ ] Consent wording for future-event updates — A8#12

### 13. Documentation / user guide for organizers
Covers (indicatively):
- [ ] Content management — A8#13
- [ ] Registration handling — A8#13
- [ ] Exports (CSV / Excel) — A8#13
- [ ] Emails — A8#13
- [ ] Certificates — A8#13
- [ ] Evaluations — A8#13

---

## Additional scope beyond A8

### Save-the-date video promo
- [ ] One save-the-date video promo created for the initial delivery — B1.1
- [ ] Integrated / displayed on the site — A2

### QR check-in (A6.8 / B1.3) — **in scope** _(decided)_

Priced separately at **€480,00 + VAT** (B1.3). Builds on A8#5 (admin) and A8#8 (certificates); feeds the attendance source.

**How it works**
- [ ] Unique QR code per participant, delivered via email and/or confirmation page — A6.8
- [ ] Admin QR scanning page (mobile / tablet) — A6.8
- [ ] Auto-mark `"attended"` on successful scan — A6.8

**Management & controls**
- [ ] Attendance status view in admin panel — A6.8
- [ ] Manual correction / addition of attendance marks (edge cases: tech issues, lost QR) — A6.8
- [ ] Prevent double check-in with the same QR code — A6.8

**Link to certificates**
- [ ] QR-marked attendance used as basis for automatic certificate issuance & email — A6.8

**Constraints / assumptions**
- [ ] Applies to physical presence only — A6.8
- [ ] Requires basic organizational support from organizers at event entry (staff with device to scan) — A6.8

---

## Phase gates (organizer approval required)

Per Α.9 timeline (total **10–12 weeks**):

- [ ] **Phase 1 — Analysis & design:** goals analysis, site map finalized, mockups / wireframes approved
- [ ] **Phase 2 — Development & implementation:** site built, bilingual navigation (DE/EL), initial content ingested
- [ ] **Phase 3 — QA & delivery:** cross-device/browser testing, feedback integrated, published, handover docs & accesses delivered

---

## Commercial commitments

- [ ] **Base development fee: €4.200,00 + VAT** — lump sum on delivery (B1.1, B2)
- [ ] **QR check-in add-on: €480,00 + VAT** — lump sum on delivery (A6.8, B1.3)
- [ ] **Total development: €4.680,00 + VAT**
- [ ] **Delivery within 10–12 weeks** from engagement + receipt of required material (A.9, B3)

### Annual renewal scope — Year 2+

Included in **€700,00 + VAT / year** (B1.2):

- [ ] New program / workshops entry
- [ ] Speaker and content updates
- [ ] Minor functional or aesthetic adjustments — _any structural/aesthetic change requires organizer approval before implementation_ — A6.1
- [ ] Registration / email / certificate management support
- [ ] One save-the-date video promo per year
- [ ] Hosting & technical updates

---

## Responsibilities & assumptions

Dependencies between PnK and the organizer. Surfacing these prevents "εφόσον δοθεί το υλικό" surprises during delivery.

### Organizer provides
- [ ] Content: text, program data, workshop descriptions, speaker bios
- [ ] Media: photos (for past-year archive and current content), any flyers / posters
- [ ] Brand assets: logos, colors, typography preferences (if any)
- [ ] Approval of final site map at kickoff — A3
- [ ] Approval of mockups / wireframes at Phase 1 gate — A.9
- [ ] Approval of certificate template (aesthetics + content) — A6.4
- [ ] Approval of any structural / aesthetic adjustments during annual renewal — A6.1
- [ ] Partners-only promo material (sent to PnK for upload) — A6.6
- [ ] Staffing for QR check-in at event entry — A6.8
- [ ] Inbound link from goethe-institut.de pointing to the new site — A1
- [ ] Content/approval for privacy, cookies, consent wording — A8#12

### PnK provides
- [ ] All deliverables above
- [ ] Email-sending service license & setup — A6.3
- [ ] Hosting, technical updates, support (Year 2+) — B1.2

### Shared / collaborative
- [ ] Site map finalization at kickoff — A3
- [ ] Final approver for milestone sign-off — **to be named** _(see timeline open questions)_
- [ ] Partners-only access policy (who gets a code, how it rotates) — A6.6

---

## Explicitly outside scope (unless separately agreed)

- Hosting past-year material other than selected photos and programs (digital flyers, posters, etc.) — conditional on material + access policy (A6.7).
- Anything on the `goethe.de` side — only the inbound link is in scope from their side (A1).
- Content translation between DE and EL — the offer expects content to be supplied by the organizer in both languages (inferred from A4 parity commitment with no translation service mentioned).

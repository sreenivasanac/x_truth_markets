## Nano Banana Pro prompts — Solution C UI/UX mockups (Truth Bounties / Challenge Markets)

### Global style (apply to all screens)
- **Figma-like** high-fidelity product mockup (not a sketch).
- Dark mode, clean typography, modern “case management + fintech” feel.
- No real logos or brand assets; generic “social post” UI inspired by X.
- No real people, no celebrity likeness.
- Use fictional handles and domains.
- Keep text legible at 1K resolution.

---

### 01 — X Post Overlay (mobile, reader)
**Prompt**
Design a mobile screen (9:16) showing a generic social post UI inspired by X.
Under the post, add a “Truth Bounty” overlay card with a clear state machine feel:
- Status pill: “Challenged” (orange)
- Subtext: “Under review”
- Bounty total: “$325”
- Small line: “2 evidence packs submitted · Dispute window: 18h”
- Buttons: “View case” (primary) and “Add bounty” (secondary)
Post content (fictional):
“New safety recall: 1.3M units pulled due to overheating risk. Memo: regulator.example/recall-bulletin.pdf”
Add subtle separators and bottom nav.

---

### 02 — Case Page (mobile, reader)
**Prompt**
Design a mobile case page (9:16), dark mode.
Header: “Truth Bounty Case”.
Canonical question (large): “Did the regulator issue a recall for 1.3M units due to overheating risk?”
Cards:
- Status timeline: Open → Challenged → Under review → Resolved
- Bounty pool: $325 (with contributors count)
- Resolution criteria (official bulletin/database entry)
Evidence highlights list with source-type pills.
CTA row: “Start challenge” and “Add bounty”.

---

### 03 — Add Bounty (mobile, bounty funder)
**Prompt**
Design a mobile “Add bounty” screen (9:16), dark mode.
Show:
- Current bounty total ($325)
- Contribution amount selector ($10 / $25 / $50 / custom)
- Payment method row (generic)
- Warning box: “Don’t fund harassment. Bounties must target checkable claims.”
- Expected impact: “More bounty attracts more investigation.”
Primary CTA: “Add $25 to bounty”. Secondary: “Cancel”.

---

### 04 — Start Challenge (mobile, challenger)
**Prompt**
Design a mobile “Start challenge” flow (9:16), dark mode.
Top: case title + bounty amount.
Stake card:
- Stake amount input (e.g., $50)
- Note: “Stake is forfeited if your challenge fails.”
Evidence pack section:
- Add link (up to 5)
- Source type dropdown (Official / Dataset / Primary media / News / Analysis)
- Excerpt textarea
- Checklist: “Primary sources preferred · Provide timestamps · Avoid personal attacks”
Primary CTA: “Submit challenge”. Secondary: “Save draft”.

---

### 05 — Case Timeline (mobile)
**Prompt**
Design a mobile “Case timeline” screen (9:16), dark mode.
Show a vertical timeline with events:
- Bounty created
- Challenge submitted (alias)
- Evidence pack added
- Jury assigned
- Under review
- Dispute window opens/closes
Include deadlines and a small “who’s involved” card with aliases (Challenger_42, Juror_A7).

---

### 06 — Jury Resolution Console (desktop)
**Prompt**
Design a desktop web app (16:9), dark mode, sober.
Title: “Resolution Console (Bounties)”.
Left sidebar: cases awaiting decision + filters (Near deadline, Disputed, High bounty).
Main:
- Canonical question
- Resolution criteria
- Evidence table (source type, link, excerpt, added by)
- Stake/bounty summary and payout preview
Decision module:
- Outcome selector: True / False / Misleading / Unverifiable
- Rationale text box
- Attach citations picker
- Buttons: “Publish decision” and “Open dispute window (24h)”
Right sidebar: audit log.

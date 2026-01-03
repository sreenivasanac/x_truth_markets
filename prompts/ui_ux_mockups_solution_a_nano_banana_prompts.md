## Nano Banana Pro prompts — Solution A UI/UX mockups

### Global style (apply to all screens)
- **Figma-like** high-fidelity product mockup (not a sketch).
- Dark mode, clean typography, modern fintech feel.
- No real logos or brand assets; use generic “social post” UI inspired by X.
- No real people, no real politician names, no celebrity likeness.
- Use realistic but fictional handles and names.
- Include small UI details: spacing, icons, subtle shadows, dividers.
- Keep content legible at 1K resolution.

---

### 01 — X Post Overlay (mobile)
**Prompt**
Design a mobile screen (9:16) showing a social post with an inline “Truth Market” overlay under the post. The overlay is compact and trustworthy:
- A chip: “Truth signal: 28% YES”
- Label: “Likely False”
- Confidence badge: “Medium (liquidity)”
- Tiny sparkline of price over time
- Two buttons: “View market” (primary) and “Trade” (secondary)
- A collapsed “Why” section preview: “3 citations · updated 12m ago”
Post content (fictional, non-cringe):
“The EU just fined a major app store €2.1B and required third‑party payments starting next month. Here’s the ruling: regulator.example/ruling.pdf”
Make the post UI feel like X dark mode, but without any real logo. Add subtle separators and a clean bottom nav.

---

### 02 — Claim + Market Page (mobile)
**Prompt**
Design a mobile claim page (9:16) for a YES/NO truth market.
Header: “Truth Market” with back button.
Canonical question (large): “Did the EU issue a €2.1B fine and require third‑party payments starting next month?”
Under it: Resolution criteria card:
- “Resolves YES if: regulator press release or ruling PDF states both conditions”
- “Resolves NO otherwise”
- “Deadline: Jan 10, 2026”
Main area:
- Big probability: “YES 28¢ (28%)” and “NO 72¢ (72%)”
- Price chart (7d)
- Volume + liquidity + spread
Bottom: Trade widget with YES/NO toggle, amount input, expected payout.
Tabs: Overview · Evidence (12) · Rules.

---

### 03 — Trade Ticket + Research (mobile)
**Prompt**
Design a mobile trading flow (9:16) for the same claim.
Top: “Buy NO” selected. Show amount, average price, fees, slippage, and “Expected profit if resolves NO”.
Include a “Your credibility” panel showing a simple score (e.g., 712) and a note: “Add a citation to improve weight in thin markets.”
Below: a “Top Evidence” list with structured entries:
- Source type pill (Official / Dataset / Primary media / News / Analysis)
- Domain + timestamp
- 1–2 line excerpt
Primary CTA: “Confirm trade” with secondary “Add evidence link”.

---

### 04 — Evidence Submission (mobile)
**Prompt**
Design a mobile “Add Evidence” screen (9:16).
Fields:
- URL input
- Source type dropdown (Official / Dataset / Primary media / News / Analysis)
- Optional excerpt textarea
- Optional stake slider (“Stake 0–50 credits to vouch for this source”)
Validation hints:
- “Prefer primary sources”
- “No personal attacks; citations only”
Button: “Submit evidence”.
Show how evidence will appear: a small preview card.

---

### 05 — Resolver Console (desktop)
**Prompt**
Design a desktop web app screen (16:9) titled “Resolution Console”.
Left column: queue of markets pending resolution with filters.
Main panel:
- Canonical question
- Resolution criteria
- Countdown to deadline
- Evidence list with source-type tags and citations
Decision module:
- Select outcome: YES / NO / Unverifiable
- Rationale text box
- “Attach citations” picker
- Buttons: “Publish resolution” and “Open dispute window (24h)”
Add small audit log sidebar: “Who resolved, when, links used”.

---

### 06 — Ops / Watchtower Dashboard (desktop)
**Prompt**
Design a desktop dashboard (16:9) for “Market Integrity / Watchtower”.
Show:
- Alerts (thin market spike, correlated accounts, evidence spam)
- A timeline of suspicious trades
- A “Market health” table (volume, liquidity, variance, unresolved age)
Actions (clearly gated): “Increase min stake”, “Rate-limit evidence”, “Freeze trading (requires 2-person approval)”.
Keep it sober and procedural, not opinionated.

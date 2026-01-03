## Solution C UI/UX (Product + Design Brief)

### Product goal
Turn checkable claims on X into **bounty + challenge** workflows:
- anyone can fund a **truth bounty** to attract investigation
- anyone can **challenge** by staking and submitting structured evidence
- a small **jury/panel** resolves the claim by procedure
- payouts + reputation updates happen automatically

### Primary users (minimal roles)
1. **Reader (default X user)**
   - Wants a simple status signal and credible citations.
2. **Bounty Funder (opt-in)**
   - Adds money to attract challengers and speed up resolution.
3. **Challenger (opt-in)**
   - Stakes and submits evidence pack; wants a clear checklist and fairness.
4. **Jury / Resolver (rare, gated)**
   - Makes the final decision for hard cases; publishes rationale + citations.

### UX principles (Solution C specific)
- **Status-first**: overlay should show state machine clearly (Open → Challenged → Under review → Resolved).
- **Skin in the game**: stakes/bonds are explicit; “who pays if wrong” is visible.
- **Evidence pack, not debate**: structured links, excerpts, and source typing.
- **Procedural neutrality**: resolution criteria and dispute steps are displayed prominently.
- **Harassment resistance**: challengers/jurors can use aliases; reporting/abuse controls are private.

### End-to-end journey (happy path)
1) Reader sees a post → overlay shows “Status: Challenged · Bounty: $300 · Under review”.
2) Bounty funder taps “Add bounty” → contributes (e.g., $25) and sees updated total + ETA.
3) Challenger taps “Start challenge” → stakes (e.g., $50) and submits evidence pack.
4) Jury reviews evidence + criteria → resolves outcome (True/False/Misleading/Unverifiable).
5) Overlay updates with outcome + citations; payouts are displayed transparently.

### IA / screens to mock
1. **X Post Overlay (Reader)**
   - Status pill + bounty total + CTA to view case.
2. **Case Page (Reader)**
   - Canonical claim, resolution criteria, timeline, bounty pool, evidence highlights.
3. **Add Bounty (Bounty funder)**
   - Contribution amount, payment method, anti-abuse warning.
4. **Start Challenge / Stake + Evidence Pack (Challenger)**
   - Stake amount, checklist, attach links, excerpts, source type, submit.
5. **Case Timeline / Dispute Process (Reader/Challenger)**
   - States, deadlines, dispute window, who is involved (aliases).
6. **Jury Resolution Console (Resolver)**
   - Evidence table, criteria, decision, rationale, citations, publish.

### Two high-quality, non-cringe example X posts (for mock content)
**Example A (high-stakes public info; bounty-worthy)**
- Post text (fictional):
  - “New safety recall: 1.3M units pulled due to overheating risk. Memo: regulator.example/recall-bulletin.pdf”
- Canonical case question:
  - “Did the regulator issue a recall for 1.3M units due to overheating risk?”
- Resolution source:
  - Official recall bulletin / regulator database entry.

**Example B (quote fabrication; common misinfo vector)**
- Post text (fictional):
  - “Screenshot: CEO says ‘we faked the numbers’ in an internal email. (leaked today) [image]”
- Canonical case question:
  - “Is the screenshot authentic and from the claimed internal email (not fabricated)?”
- Resolution source:
  - Company statement + metadata verification + reputable newsroom corroboration.

### Microcopy (example)
- Overlay:
  - “Status: Challenged · Bounty: $325 · Under review”
  - “2 evidence packs submitted · Dispute window: 18h”
  - Buttons: “View case” “Add bounty”
- Challenge CTA:
  - “Stake is forfeited if your challenge fails.”

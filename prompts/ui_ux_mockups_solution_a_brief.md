## Solution A UI/UX (Product + Design Brief)

### Product goal
Turn checkable claims on X into **simple YES/NO truth markets**; show a compact “truth signal” (probability + confidence + short why) directly under the post, with a deeper market page for participants.

### Primary users (minimal roles)
1. **Reader (default X user)**
   - Wants a fast, legible signal and a short explanation with sources.
2. **Trader / Forecaster (opt-in)**
   - Researches and trades YES/NO; wants liquidity, clear rules, and fast execution.
3. **Resolver (small panel / jury; rare)**
   - Runs resolution when a claim has an explicit resolution source or when a dispute requires judgment.
4. **Ops/Admin (limited)**
   - Monitors manipulation/abuse, handles appeals workflow, maintains “procedure-only” rules.

### UX principles (from Solution A)
- **One-glance output**: probability + label + confidence badge.
- **No comment-thread incentives**: evidence is structured (links + excerpts + source type), not “arguments”.
- **Credible neutrality**: claim wording + resolution criteria shown prominently; rules change slowly.
- **Honest uncertainty**: show when liquidity is thin; “Unverifiable” is an explicit, acceptable outcome.
- **Safety by default**: pseudonyms for traders, anti-harassment surfaces minimal; abuse reporting is private.

### End-to-end user journey (happy path)
1) Reader sees a post → sees an overlay chip: **Truth signal: 28% YES · Likely False · Confidence: Medium**.
2) Reader taps **View market** → Claim page with canonical question, resolution rules, price chart.
3) Trader taps **Trade** → buys YES/NO shares; can add evidence links.
4) Market hits deadline / sufficient resolution evidence appears → Resolver confirms outcome.
5) Overlay updates to **Resolved: False** (or True / Misleading / Unverifiable) with short “Why” and citations.

### IA / screens to mock
1. **X Post Overlay (Reader)**
   - Compact chip + “Why” drawer.
   - Shows probability, label, confidence (liquidity), and a single CTA.
2. **Claim + Market Page (Reader/Trader)**
   - Canonical question, resolution criteria, market price/probability chart, trade widget.
   - Tabs: Overview · Evidence · Rules.
3. **Trade Ticket (Trader)**
   - Buy/sell YES/NO; shows slippage, fees, expected payout.
   - Nudges: “Add a citation to increase your credibility score.”
4. **Evidence Submission (Trader/Researcher)**
   - Add link, pick source type (Official/Dataset/Primary Media/News/Analysis), add excerpt, optional stake.
5. **Resolution Console (Resolver)**
   - Shows claim + resolution source, evidence list, vote/decision, rationale + citations, dispute window.
6. **Ops/Watchtower Dashboard (Admin)**
   - Flags: thin markets with sharp moves, correlated accounts, repeated evidence spam.
   - Actions: freeze trading (rare), require higher stake, open dispute review.

### Two non-cringe example X posts (for mock content)
**Example A (tech / policy; checkable)**
- Post text (fictional):
  - “The EU just fined a major app store €2.1B and required third‑party payments starting next month. Here’s the ruling: [link]”
- Canonical market question:
  - “Did the EU issue a €2.1B fine and require third‑party payments starting next month?”
- Resolution source:
  - Official regulator press release / ruling PDF.

**Example B (video provenance; checkable)**
- Post text (fictional):
  - “This clip shows last night’s airport outage caused by a transformer fire. (Taken at 11:40pm local) [video]”
- Canonical market question:
  - “Was this video recorded during last night’s airport outage (not an older clip)?”
- Resolution source:
  - Airport incident report + timestamped local news footage / official statement.

### Microcopy (example)
- Overlay chip:
  - “Truth signal: 28% YES · Likely False · Confidence: Medium”
  - “Why: 3 citations · Market volume: $84k”
  - Buttons: “View market” “Trade”
- Resolution badge:
  - “Resolved: False (Jan 03, 2026) · Source: Official bulletin”

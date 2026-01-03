## Nano Banana Pro prompts — Solution B UI/UX mockups (Reputation Forecasting)

### Global style (apply to all screens)
- **Figma-like** high-fidelity product mockup (not a sketch).
- Dark mode, clean typography, modern “trust + analytics” feel.
- No real logos or brand assets; use generic “social post” UI inspired by X.
- No real people, no celebrity likeness.
- Use realistic but fictional handles and names.
- Keep content legible at 1K resolution.
- Emphasize **commit-first** forecasting and **reputation** (accuracy, calibration).

---

### 01 — X Post Overlay (mobile, reader)
**Prompt**
Design a mobile screen (9:16) showing a social post UI inspired by X (generic, no logos) with a “Truth Forecast” overlay card under the post.
Overlay includes:
- Chip: “Truth signal: 35% likely true”
- Label: “Unclear”
- Confidence badge: “Medium”
- Small text: “Weighted by historical accuracy”
- Buttons: “View forecast” (primary) and “Forecast” (secondary)
- Collapsed “Why” preview: “3 citations · updated 18m ago”
Post content (fictional, good use case):
“City transit authority says ridership hit 5.2M trips last month — highest since 2019. Report: transit.example/monthly-ridership.pdf”
Add subtle separators and bottom nav icons.

---

### 02 — Forecast Detail (mobile, reader/forecaster)
**Prompt**
Design a mobile forecast detail screen (9:16), dark mode.
Header: “Truth Forecast”.
Canonical question (large): “Did the city transit authority report 5.2M trips last month (highest since 2019)?”
Resolution criteria card:
- “Resolves TRUE if official monthly report states 5.2M and highest since 2019”
- “Resolves FALSE otherwise”
- “Resolves UNVERIFIABLE if report not published by deadline”
Main:
- Big aggregate probability: “35% TRUE”
- Confidence meter (Low/Medium/High) with short explanation
- Mini chart: probability over time (7d)
Evidence summary list (3–5 items) with source-type pills.
CTA row: “Submit forecast” and “Add evidence”.

---

### 03 — Submit Forecast (mobile, commit-first)
**Prompt**
Design a mobile “Submit forecast” screen (9:16), dark mode.
Show a prominent banner:
“Anti-herding: you must submit before seeing others’ forecasts.”
Inputs:
- Probability slider 0–100% with numeric entry
- Toggle: True / False (optional assist)
- Add up to 3 evidence links
- Optional note field (short)
Show a small “Your influence weight” preview based on accuracy tier.
Primary CTA: “Submit forecast (commit)”. Secondary: “Cancel”.

---

### 04 — After Submit: Distribution + Your Position (mobile)
**Prompt**
Design a mobile screen (9:16) that appears after a user submits their forecast.
Top shows “Your forecast: 22% TRUE” (example) with timestamp.
Main shows:
- Histogram / density plot of all forecasts
- Marker for user position
- “Median”, “IQR”, and “Accuracy-weighted mean” annotations
Below:
- “Top forecasters (anonymized)” list showing accuracy tier badges (e.g., A, B, C) and their submitted probabilities
- A short explanation card: “Your influence weight updates after resolution based on scoring (Brier).”

---

### 05 — Forecaster Profile (mobile)
**Prompt**
Design a mobile “Forecaster profile” screen (9:16), dark mode.
Show:
- Display name + anonymized handle
- Overall accuracy score and tier (A/B/C)
- Calibration curve mini chart (predicted vs observed)
- Breakdown cards: Topics (Policy/Health/Science/Local), Average confidence, Overconfidence penalty
- Recent resolved forecasts list with outcome, forecast %, score change (+/-).
Keep it clean, analytical, and credible.

---

### 06 — Jury/Resolver Console (desktop)
**Prompt**
Design a desktop web app screen (16:9) titled “Resolution Console (Forecasts)”.
Left sidebar: queue of claims pending resolution with filters (Near deadline, Disputed, High impact).
Main panel:
- Canonical question
- Resolution criteria
- Aggregate probability and forecast distribution snapshot
- Evidence list with source-type tags and citation links
Decision module:
- Outcome selector: True / False / Misleading / Unverifiable
- Rationale text box
- “Attach citations” picker
- Buttons: “Publish resolution” and “Open dispute window (24h)”
Right sidebar: audit log.

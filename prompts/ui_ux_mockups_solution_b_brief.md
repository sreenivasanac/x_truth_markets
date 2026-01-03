## Solution B UI/UX (Product + Design Brief)

### Product goal
Provide a **forecasting + reputation** layer for factual claims on X:
- readers get a compact, legible “truth signal” (probability + confidence + short why)
- forecasters submit probabilities (and evidence) and earn a **public accuracy profile** via proper scoring
- a small **jury/panel** resolves hard claims when automatic resolution is not possible

### Primary users (minimal roles)
1. **Reader (default X user)**
   - Wants a fast signal, and a short, citation-backed summary.
2. **Forecaster (opt-in)**
   - Submits a probability (0–100%) and optional evidence links.
   - Cares about accuracy score, influence weight, and streaks/track record.
3. **Jury / Resolver (rare, gated)**
   - Resolves hard/ambiguous claims following explicit resolution criteria and evidence.
   - Provides rationale + citations and opens a short dispute window.

### UX principles (Solution B specific)
- **Commit-first anti-herding**: users must submit their probability before seeing others.
- **Numbers > arguments**: evidence is structured; social signals are minimized.
- **Reputation is the incentive**: show how forecasting affects influence weight over time.
- **Honest uncertainty**: confidence badge reflects evidence quality + forecaster depth, not popularity.
- **Credible neutrality**: show claim wording + resolution criteria as the “source of truth” for the process.

### End-to-end journey (happy path)
1) Reader sees a post → sees an overlay chip: “Truth signal: 35% likely true · Confidence: Medium”.
2) Reader taps “Why” → 2-line summary + citations; can tap “Forecast”.
3) Forecaster enters probability + evidence and submits (commit).
4) After submit, forecaster sees distribution + how their forecast compares.
5) When claim resolves, forecaster receives a score update and their accuracy profile changes.

### IA / screens to mock
1. **X Post Overlay (Reader)**
   - Truth signal chip + confidence, “Why”, and CTA “View forecast”.
2. **Forecast Detail (Reader/Forecaster)**
   - Canonical question, resolution criteria, aggregate probability, confidence, evidence summary.
   - “Forecasting closes in …” countdown.
3. **Submit Forecast (Forecaster) — commit-first**
   - Slider/input 0–100%, evidence links, submit.
   - Copy: “You’ll see others’ forecasts after you submit.”
4. **After Submit: Distribution + Your Position (Forecaster)**
   - Histogram / density of forecasts, top forecasters by accuracy (anonymized IDs), your forecast marker.
   - “Influence weight” explanation.
5. **Forecaster Profile (Reputation / Calibration)**
   - Accuracy score, calibration curve, category breakdown, recent resolved forecasts.
6. **Jury Resolution Console (Resolver)**
   - Claim + criteria + evidence list, decision (True/False/Misleading/Unverifiable), rationale + citations, dispute window.

### Two high-quality, non-cringe example X posts (for mock content)
**Example A (public data; strong use case)**
- Post text (fictional):
  - “City transit authority says ridership hit 5.2M trips last month — highest since 2019. Report: transit.example/monthly-ridership.pdf”
- Canonical question:
  - “Did the city transit authority report 5.2M trips last month (highest since 2019)?”
- Resolution source:
  - Official monthly ridership report.

**Example B (misinfo-prone but resolvable)**
- Post text (fictional):
  - “This photo proves the wildfire reached downtown last night. (taken 11:30pm) [image]”
- Canonical question:
  - “Was this photo taken downtown last night during the wildfire (not an older/other-location image)?”
- Resolution source:
  - Local emergency updates + verified geolocation/time metadata + local newsroom confirmation.

### Microcopy (example)
- Overlay chip:
  - “Truth signal: 35% likely true · Confidence: Medium”
  - “Why: 3 citations · Updated 18m ago”
  - Buttons: “View forecast” “Forecast”
- Commit-first modal:
  - “Submit your probability to reveal others’ forecasts (anti-herding).”

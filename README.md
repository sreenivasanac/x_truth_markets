# Truth Markets in X, to replace Community Notes

This repo contains prompts and design explorations for a better Truth-verification for X (Twitter), to replace Community Notes -- using **prediction-market-style incentives** and related mechanisms.

## Problem statement

Design a system that sits alongside X posts and helps readers quickly understand whether a post’s **checkable factual claims** are **true / false / misleading / unverifiable** (or a calibrated probability of truth), with short citation-backed “why” summaries.

The core requirement is **aligned incentives**: participants who forecast truth accurately—especially “minority/contrarian but correct” contributors—should be rewarded more, while incorrect or low-quality participation is penalized, without devolving into a popularity contest. The system should also be resilient to adversarial behavior (brigading, sybils, collusion) and work at platform scale.

## Prompts

- System design prompt (initial): [`prompts/1_x_fact_verification_system_design_prompt.md`](prompts/1_x_fact_verification_system_design_prompt.md)
- Open-ended deep-research prompt (primary): [`prompts/2_x_fact_verification_prediction_markets_deep_research_prompt.md`](prompts/2_x_fact_verification_prediction_markets_deep_research_prompt.md)
- Prompt improvement request (original brief): [`prompts/0_x_fact_verification_prompt_improvement_request.md`](prompts/0_x_fact_verification_prompt_improvement_request.md)

## Solution writeups

Each solution below includes a high-level mechanism + incentives + resolution approach, plus an architecture diagram.

- **Solution A — Free-market claim prediction markets (Polymarket-like)**: [`solution/solution_a_free_market_prediction_markets.md`](solution/solution_a_free_market_prediction_markets.md)
  - Turn important claims into YES/NO markets; the market price acts as a public probability signal for “how likely is this true?”. Strong incentive alignment (profit/reputation for being right, penalties for being wrong), but depends on clean resolution rules and may raise regulatory/UX complexity if real money is used.
  - Diagram: [`images/solution_a_architecture.png`](images/solution_a_architecture.png)

- **Solution B — Reputation forecasting + calibration (no real-money market)**: [`solution/solution_b_reputation_forecasting.md`](solution/solution_b_reputation_forecasting.md)
  - Collect probability forecasts and score them after resolution using proper scoring rules; aggregate forecasts are weighted by historical accuracy. This preserves incentive alignment while reducing regulatory risk by avoiding per-claim wagering.
  - Diagram: [`images/solution_b_architecture.png`](images/solution_b_architecture.png)

- **Solution C — Truth bounties / challenge markets**: [`solution/solution_c_truth_bounties.md`](solution/solution_c_truth_bounties.md)
  - A “bounty + arbitration” model: users fund bounties on claims, challengers stake and submit evidence, and a neutral dispute process resolves the outcome. This concentrates attention on high-impact claims and can be easier to understand than continuous trading.
  - Diagram: [`images/solution_c_architecture.png`](images/solution_c_architecture.png)

## Inputs

- Source document index / citations helper: [`documents.md`](documents.md)
- Primary documents (PDFs, etc.): `documents/`

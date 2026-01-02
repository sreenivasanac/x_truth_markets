# Solution A: Free‑Market Claim Prediction Markets for X

![Solution A architecture](../images/solution_a_architecture2.png)

## TL;DR

Turn important, clearly checkable claims on X into simple **YES/NO markets**. The market price becomes a public “how likely is this true?” signal. People who are right make money (or reputation), people who are wrong lose it. If a small minority is right against the crowd, they earn outsized returns by buying in when the price is low.

This is the most “Polymarket‑like” approach and matches the **simplicity + credible neutrality** idea: let a simple mechanism plus incentives surface information, rather than relying on moderators arguing in public comment threads.

## End-to-end overview (what happens when a claim appears)

1. **A post contains a claim** (example: “X happened”, “Y statistic is Z”, “A video shows B”).
2. An AI assistant extracts the *checkable* claim and turns it into a short YES/NO question.
3. The system links the post to a **claim page** (canonical wording + links to sources).
4. A **market** is created (YES/NO shares).
5. Participants trade based on research; the price produces a probability.
6. When enough evidence exists (or at a deadline), the claim is **resolved**.
7. The post shows a simple overlay: probability + label (True/False/Misleading/Unverifiable) and a “why” summary with citations.

## Core mechanism (how it produces a probability)

- The market price (e.g., YES at $0.72) is treated as a public signal for “~72% likely true”.
- The key benefit is incentive alignment: if someone sees the crowd is wrong, they can profit by betting against it.
- This aligns with the “info finance” idea: the market is a betting venue for participants, and an information/“charts as news” tool for everyone else. (See https://vitalik.eth.limo/general/2024/11/09/infofinance.html.)

## Incentives (discourage herding; reward contrarians; penalize wrong bets)

### How minority-correct forecasters are rewarded more
Markets naturally do this. If the crowd pushes the price far from reality, the “minority” gets a better price and earns a bigger return.

### How wrong predictions are penalized
Wrong traders lose stake (real money) or lose reputation/points (play money).

### How to avoid devolving into a comment thread / popularity contest

- Don’t rank “arguments” by likes/retweets.
- Require **links/citations** for evidence claims (separate “evidence” from “opinions”).
- Keep the output simple (probability + short explanation), and keep the rules stable.
- Use Community Notes lessons: resistance to mass‑upvotes, reputation systems, and protections against harassment (e.g., aliases). (See https://communitynotes.x.com/guide/.)

### Worked example (majority vs minority)

Claim: “This video shows event E happened today.”

- Market opens at **YES = $0.80** (crowd thinks 80% true).
- 1,000 majority traders each buy 1 YES share at $0.80.
- 50 minority traders each buy 1 NO share at $0.20 (they think it’s a recycled old clip).
- Resolution outcome: **NO (false)**.

Payouts (per share):
- YES shares pay $0 → majority loses **$0.80/share**.
- NO shares pay $1 → minority earns **$1 − $0.20 = $0.80/share** (a **4× return** on the $0.20 cost).

Optional reputation overlay:
- Each correct trade increases “accuracy reputation”; each losing trade decreases it.
- The minority traders gain much more accuracy reputation because they were correct when it was unpopular.

## Resolution & verification (the “who decides?” problem)

Markets only work if outcomes settle in a way that is predictable and hard to game.

**A practical approach:**
- Use a clear “resolution source” per market (official dataset, court ruling, published retraction, etc.).
- For claims that require judgment (“misleading”), use a **small panel / jury** process, with an appeal path.
- Consider Vitalik’s “distilled human judgment”: use markets to predict what a trustworthy-but-costly process would decide, and only run the costly process for a small subset (random or high-impact). (See https://vitalik.eth.limo/general/2024/11/09/infofinance.html.)

Handling “Unverifiable”:
- If a claim cannot be resolved cleanly, the market should resolve to “Unverifiable” by rule, rather than becoming a never-ending fight.

## Manipulation resistance (what can go wrong, and mitigations)

### Key risks

- **Information cascades / herding:** people follow the crowd instead of doing independent research. (See `Collective Stupidity -- How Can We Avoid It?` https://www.youtube.com/watch?v=25kqobiv4ng.)
- **Bias and inefficiency:** markets can reflect user-base bias, hedging behavior, and “not worth arbitraging yet” time horizons. (See https://www.lesswrong.com/posts/LhJ9u5Gy6bAMh7WwA/do-prediction-markets-work.)
- **Low-liquidity fragility:** thin markets are easier to push around and may have predatory liquidity. (See https://substack.com/home/post/p-172450780 and https://x.com/knowerofmarkets/status/1970476889232830607.)
- **Whale manipulation narrative:** sometimes claimed, but not always true; whales can also move markets toward accuracy. (See `Prediction Markets for the Win.` https://marginalrevolution.com/marginalrevolution/2024/11/prediction-markets-for-the-win.html.)

### Mitigations that keep things simple

- Start with **high-impact claims only** (avoid millions of tiny markets until you have enough participation).
- Use **shorter resolution windows** when possible (reduces the “not worth arbitraging” problem).
- Show a **confidence indicator** (e.g., volume/liquidity) so readers know when a market is thin.
- Use Community Notes-style **eligibility criteria** for participants and a **reputation layer** (phone verification, account age, etc.) (from https://communitynotes.x.com/guide/).
- Add “watchtower” monitoring for suspicious trading patterns (optional; see `prompts/extra.md`).

## Governance & credible neutrality

The mechanism must be seen as fair by people who disagree.

Practical rules inspired by “credible neutrality”:
- Don’t hardcode political outcomes; hardcode **procedures**.
- Keep rules simple, public, and slow to change.
- Make resolution criteria explicit at market creation.

(See https://balajis.com/p/credible-neutrality.)

## What a user would see (examples)

### Reader view
- Under a tweet: “Truth signal: **22% likely true** · Label: **Likely False**”
- A short “why” summary: 3 bullet points + links.
- “View market” button.

### Participant view
- Claim page with:
  - the canonical claim wording
  - what counts as resolution
  - links to primary sources
  - buy/sell YES/NO

## MVP plan (6–10 weeks)

- Browser extension (or simple web overlay) that attaches a “claim page” link to selected tweets.
- Human-in-the-loop claim creation (manual claim entry + template).
- AI-assisted claim extraction + duplicate merging.
- Basic market engine (start with play-money + reputation to reduce legal risk).
- Resolution workflow: predefined sources + small manual resolution panel + appeal.
- Reputation updates + simple participant dashboards.
- Expand to more claim categories.
- Monitoring + rate-limits + anti-spam.
- Start testing different “display” UX for probability + label.

## 1–3 year roadmap

- If legally viable, explore real-money markets via a compliant structure (CFTC / partner / geofencing).
- Scale to more claims using AI to suggest which posts deserve markets (see https://medium.com/inception-capital/the-prediction-market-primitive-e48a055676bf).
- Improve resolution with better “distilled judgment” + selective juries.
- Stronger identity/reputation (optional) and privacy protections.

## Open questions for future R&D

- What’s the best way to define “Misleading” without making resolution political?
- How do we prevent harassment of participants while still enabling accountability?
- How do we keep markets informative on long-horizon claims (where arbitrage is slow)?

## References

- [X, “Community Notes Guide”](https://communitynotes.x.com/guide/)
- [Balaji Srinivasan, “Credible Neutrality As A Guiding Principle”](https://balajis.com/p/credible-neutrality)
- [Vitalik Buterin, “From prediction markets to info finance”](https://vitalik.eth.limo/general/2024/11/09/infofinance.html)
- [Benjamin Sturisky, “Do Prediction Markets Work?”](https://www.lesswrong.com/posts/LhJ9u5Gy6bAMh7WwA/do-prediction-markets-work)
- [Benjamin Sturisky, “Prediction Markets Explained”](https://www.lesswrong.com/posts/GxmfqKjs6ruxNxhqr/prediction-markets-explained)
- [Benjamin Sturisky, “Prediction markets are suboptimal betting vehicles”](https://substack.com/home/post/p-172450780)
- [Sabine Hossenfelder, “Collective Stupidity — How Can We Avoid It?” (YouTube)](https://www.youtube.com/watch?v=25kqobiv4ng)
- [Hiroki Kotabe, “The prediction market primitive: Using AIs to create prediction markets at microscopic scale”](https://medium.com/inception-capital/the-prediction-market-primitive-e48a055676bf)
- knowerofmarkets tweet: [“What prediction markets are and aren’t” (X post)](https://x.com/knowerofmarkets/status/1970476889232830607)
- [Alex Tabarrok, “Prediction Markets for the Win”](https://marginalrevolution.com/marginalrevolution/2024/11/prediction-markets-for-the-win.html)
- Jay Baxter, X posts on Community Notes + prediction markets: [post 1](https://x.com/jaybaxter/status/1808173808014250494?s=20), [post 2](https://x.com/jaybaxter/status/1808192082210967588?s=20)
- [Vitalik Buterin, “An Introduction to Futarchy”](https://blog.ethereum.org/2014/08/21/introduction-futarchy)
- [Vitalik Buterin, “Prediction Markets: Tales from the Election”](https://vitalik.eth.limo/general/2021/02/18/election.html)
- US regulatory landscape summaries (not legal advice):
  - [Ben Horney, “Why Polymarket Has Avoided Legal Pushback So Far” (Front Office Sports)](https://frontofficesports.com/polymarket-avoided-legal-pushback-kalshi-sports-betting/)
  - [Eli France, Timothy Keane, and Gary Chodes, “Prediction Market Leader Kalshi Suffers Legal Blow as Nevada Court Rules Platform Subject to State Gaming Laws” (National Law Review)](https://natlawreview.com/article/prediction-market-leader-kalshi-suffers-legal-blow-nevada-court-rules-platform)

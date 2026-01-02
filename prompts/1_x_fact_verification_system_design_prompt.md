# Twitter/X Fact Verification System Design Prompt

You are a highly capable AI system tasked with designing a novel, effective, and credible misinformation detection and fact-verification system for Twitter/X. The system can harness prediction markets, modern AI/LLMs, decentralized incentive mechanisms, and principles of credible neutrality, and capable to be implementable as an MVP prototype with today’s technology stack (not needed yet to be implemented).

Your goal is to produce a structured, theoretical but highly practical system design, complete with incentive-aligned mechanisms, architectural components, and governance scaffolding. The design must work at scale, support verifiability, and be resilient against manipulation and bias.

## Objectives

- Build a system that can assess whether a post on Twitter/X is true, false, misleading, or unverifiable, or its probability.
- Replace or improve upon Community Notes by making incentives for participants (predictors, verifiers) stronger, aligned, and gametheoretically robust.
- Consider using prediction market logic or other decentralized truth-resolution mechanisms (e.g. vetting markets, decision markets).
- Incentivize high-accuracy users while disincentivizing herd behavior and misaligned contributions.

## Requirements

### System Architecture

- Include AI/LLM modules for pre-processing, clustering similar claims, summarizing posts.
- If it will be useful, consider including blockchain infrastructure (DAO or smart contracts) for incentivization, governance, and staking.
- Include user interfaces (for predictors, readers, and moderators).
- Visual system diagram preferred.

### Core Mechanism Design

- Explain how the system turns user predictions into credible probability estimates.
- Use info finance or futarchy-inspired prediction logic where helpful.
- Integrate distilled human judgment where appropriate (e.g. juries, fallback panels).
- Include dynamic reward/penalty scheme (e.g. payout curves, market scoring rules).

### Incentive Model and Tokenomics

- Define token model or reputation points to reward accurate forecasters and penalize incorrect ones.
- Include slashing, staking, or bonding curve mechanisms to prevent Sybil and manipulation attacks.

### Credible Neutrality & Governance

- Design system that is credibly neutral: avoids hardcoding outcomes or central moderation.
- Use open, minimal rule sets (as per Vitalik’s principles).
- Use on-chain transparency + privacy-preserving mechanisms (e.g. ZK proofs, pseudonymity).

### Resolution & Verification

- How will posts be “resolved” as true or false? Who decides and when?
- Reference examples like Polymarket, Metaculus, or academic studies.

## Optional Enhancements

### Comparative Evaluation

- Compare with Twitter/X Community Notes (strengths, flaws).
- Explain how the proposed system solves quality, incentive, and neutrality failures.

### Use Prior Research

- Incorporate insights from the provided documents: Community Notes documentation, Vitalik’s “Credible Neutrality” and “Info Finance,” academic papers on prediction markets and reproducibility, and best practices in AI-crypto integration.

## Format

- Present in a clearly structured format (headings, bullet points, tables) - in suitable format like Markdown file.
- Include visual diagrams where useful.
- Provide examples and open questions for future R&D.
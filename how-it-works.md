---
title: How Orbit Works
nav_order: 7
---

# How Orbit Works

Orbit structures each prediction market as a time-bounded binary event with software-readable terms and on-chain settlement. Markets run through four coordinated stages.

## Market Creation

A market begins when the Event Discovery Agent identifies tradable uncertainty and generates a structured market definition:

- A clear binary question  
- A predetermined expiry time  
- Verifiable resolution criteria  
- Defined source hierarchy and edge-case handling

Human participants and partner platforms can also create markets through the API layer. In every case, the definition anchors to objective, externally verifiable criteria before trading opens.

## Opening Price

Before trading opens, the Pricing Agent establishes an initial probability estimate based on available information. This estimate reflects a structured assessment of the event's likelihood. It's a starting point grounded in evidence.

## CLOB and On-Chain Settlement

Orbit's trading mechanism runs on a CLOB with signed-order matching and on-chain settlement. Participants submit signed orders expressing their probability view and desired position size. Orders match against the book and settle on-chain.

Hyperliquid demonstrates that on-chain-settled order books support exchange-scale volumes with user experience competitive with centralized venues, and in May 2026 extended its book into native binary outcome markets via HIP-4. The architectural question of whether on-chain matching can match centralized systems is settled. Orbit applies that execution model to probability markets, where what trades is the likelihood of a real-world outcome. Orbit shares the on-chain-CLOB architectural choice; it differentiates on user wedge (Asia-first mobile retail event traders, distinct from perp-margin extensions into events) and on the venue's evolution toward scoped agent accounts, structured event semantics, and reputation-aware matching.

Every execution is verifiable. Every position stays non-custodial until settlement. The matching layer never takes privileged custody of participant funds.

The Liquidity and Market Making Agent and MM Vault maintain depth across probability ranges, keeping markets tradeable throughout their lifecycle. Market making is active, context-aware, and calibrated to each market's uncertainty profile.

## Probability Evolution

As participants submit orders, market prices update to reflect collective beliefs. The order book aggregates the probability assessments of all participants, weighted by capital commitment, into a continuous market price that reads as a probability at any point in the market's lifetime.

The market starts from an evidence-grounded opening price, so early trading refines the probability estimate from a calibrated baseline.

## Resolution and Settlement

As each market approaches expiry, the Result and Settlement Agent monitors for outcome signals. Once the underlying event occurs, the agent gathers evidence, proposes an outcome, and initiates the challenge window.

If the proposed outcome goes undisputed through the challenge period, settlement executes automatically on-chain. Outcome tokens corresponding to the correct result redeem at full value. The opposing side expires worthless. Smart contracts handle all positions deterministically, with no counterparty risk and no custodial intermediary.

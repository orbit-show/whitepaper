---
title: Risks
nav_order: 9
---

# Risks

Participation in prediction markets involves meaningful risk. Orbit improves market structure and aligns incentives. It doesn't eliminate uncertainty. Participants should evaluate the following before engaging.

## Market Risk

Prediction market prices reflect collective beliefs at a point in time. Prices can be wrong for extended periods, fail to converge before expiry, or shift sharply in response to new information. All trading positions carry this uncertainty.

## Liquidity Risk

Available depth changes over time and across probability ranges. Participants may face slippage, weak execution, or difficulty entering and exiting positions during low-activity periods or as markets approach resolution. The Liquidity and Market Making Agent is designed to reduce these conditions. Slippage and thin execution remain possible.

## Liquidity Provider Risk

LP risk in Orbit is primarily probability forecast error. If the probability assumptions underlying a liquidity position prove materially wrong, LPs lose value even when the market remains active and volume is healthy. LP risk is informed directional exposure calibrated by probability judgment.

## Pricing and Initialization Risk

Opening prices reflect the best available information at the time of market creation. In rapidly-evolving situations, early prices may revise substantially as new information enters. Participants trading immediately after market creation carry higher exposure to initialization uncertainty.

## Oracle and Resolution Risk

Final settlement depends on the Result and Settlement Agent, oracle integrations (including UMA-based dispute paths), and challenge mechanism identifying and verifying outcomes accurately. Delays, ambiguities, contested evidence, or failures in the resolution process can affect the timing or correctness of settlement. The challenge window and bonded proposer system reduce single-point failure risk. Resolution uncertainty remains.

## Agent System Risk

Orbit will increasingly rely on coordinated autonomous agent components. Failures, adversarial inputs, or unexpected behaviors in any agent, including Event Discovery, Pricing, Liquidity, or Settlement, can affect market quality, pricing accuracy, or resolution correctness. Agent system failures may propagate in ways that are difficult to anticipate in advance.

## Smart Contract Risk

Orbit's settlement and capital management functions depend on on-chain smart contracts. Bugs, exploits, faulty integrations, or edge-case interactions can result in partial or total loss of funds. Contract code should undergo audit before mainnet. Vulnerabilities can still exist.

## Regulatory and Legal Risk

Prediction markets face varied and evolving legal treatment across jurisdictions. Access to Orbit, geofencing, jurisdictional KYC, the range of available markets, and specific product features may change as regulatory frameworks develop. Participation may carry legal restrictions depending on the user's jurisdiction.

## Experimental Status

Orbit is an evolving system. The architecture, agent behaviors, economic parameters, launch sequencing, and technical implementation described here represent current design intent. Features and parameters may change as the protocol develops, real-world conditions are observed, and governance evolves.

## Competitive Risk

Hyperliquid's HIP-4 outcome markets launched on mainnet in May 2026 and extend an existing high-volume venue into binary event contracts. Hyperliquid and Orbit share the on-chain-CLOB architectural choice; they differ on user wedge and on the venue's evolution toward agent-native primitives. Polymarket and Kalshi remain dominant in their respective home markets and may extend distribution or product surface in ways that compress Orbit's wedge. Distribution speed, listing breadth, and the maturation of agent-native participation will determine the durability of Orbit's position.

## Activity Composition Risk

Testnet metrics include incentivized cohorts, simulated load, and replica markets used for engine validation. Wash-trade share, wallet concentration, and the incentivized-vs-organic split are tracked internally and disclosed transparently to institutional reviewers. Mainnet behavior on real-money positions may differ materially from testnet activity. Conviction in product-market fit should be calibrated against mainnet data once available.

## Agent-Native Adoption Risk

The progressive agent layer is contingent on autonomous AI agents becoming a meaningful share of financial-market participation. The timing of this transition is uncertain. Orbit's near-term thesis does not require this shift to materialize; the venue is configured to operate profitably on human-driven Asia-first event trading. If autonomous agent adoption progresses faster than expected, the same architecture compounds; if slower, the venue continues to capture the non-US event-trading wedge.

---

Nothing in this document is financial, legal, or investment advice.

---

*Orbit Whitepaper. For the latest version, visit whitepaper.orbit.show.*

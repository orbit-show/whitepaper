---
title: Orbit Whitepaper
nav_order: 0
---

# Orbit Whitepaper

---

# Abstract

Orbit is Asia-first event-trading infrastructure for the agent economy. It gives humans and autonomous AI agents a shared venue to discover, price, trade, and settle real-world event outcomes through verifiable, programmable, stablecoin-native, and non-custodial markets.

Prediction markets are one of the most reliable mechanisms for aggregating dispersed knowledge into probability signals. As stablecoin adoption expands outside the US and AI agents take on consequential financial roles, prediction markets become a financial decision layer. Agents need to express uncertainty, commit capital to outcomes they reason about, and trigger settlement within scoped permissions, limits, and kill switches. Orbit provides what existing markets don't: a native probability layer, a non-custodial execution venue, and a verifiable settlement environment, built for human distribution and agent workflows from the ground up.

Orbit is built as an Asia-first event venue today and agent-native infrastructure over time. Four specialized agent modules coordinate the market lifecycle as the system progresses. The Event Discovery Agent detects tradable uncertainty before markets form. The Pricing Agent converts information signals into actionable probability ranges. The Liquidity and Market Making Agent aggregates depth across venues and deploys capital intelligently. The Result and Settlement Agent discovers outcomes, verifies evidence, and supports deterministic on-chain resolution through oracle and dispute paths. These agents run through Orbit Core, a unified execution layer with native interfaces for both humans and autonomous systems.

Orbit's execution model runs on a CLOB with signed-order matching and on-chain settlement, combining the price-discovery properties of a limit order book with fully non-custodial capital management. Every position is verifiable. Every execution is transparent.

Orbit is the financial decision and execution layer where uncertainty becomes a tradeable, verifiable, and programmable asset. Asia-first. Designed for agents. Built on-chain. Open to anyone.

---

# The Prediction Market Opportunity

Prediction markets let participants trade on future outcomes, aggregating dispersed information into a continuously updating probability signal. They consistently outperform polls and expert forecasts when incentives align and participation is broad.

The category has proven itself. Polymarket reportedly cleared $3.7B during the 2024 US election cycle, and Kalshi reportedly reached $23.8B in 2025 annual volume. Offshore retail derivatives markets represent roughly $2 trillion annually, and the same mobile, stablecoin-native user base is moving toward event markets.

But the incumbents are structurally locked into their home markets. Polymarket is geofenced. Kalshi is CFTC-bound and fiat-native by design. Neither is configured to serve mobile, stablecoin-native users across Asia within any reasonable timeframe. Stablecoin rails already solve the access problem: USDC and USDT now reach retail users across Southeast Asia without correspondent-banking dependencies. No venue currently serves them at scale.

At the same time, a new class of participants is entering financial markets. AI agents that reason about real-world outcomes need venues to act on those beliefs programmatically. Existing platforms weren't built for them. The infrastructure gap Orbit fills is geographic first and structural over time: Asia-first distribution now, agent-native market infrastructure as autonomous capital becomes a participant class.

---

# Existing Market Pain Points

Existing prediction market platforms have APIs. Agents can read them. What they lack is AI-native design. Connecting an LLM-based agent to Polymarket today requires building custom connectors, maintaining parsing logic, and handling edge cases the API wasn't designed for. Orbit is designed to expose a native MCP server and agent SDK as the agent layer activates, reducing custom integration work for LLM-based agents.

Three structural gaps define what the incumbents can't offer:

- **No agent-native capital management.** Existing venues do not provide scoped agent accounts that can hold positions across correlated markets, adjust exposure programmatically, and execute settlement within predefined permissions, limits, and kill switches.
- **No native agent interface.** Agents that want to act on probability signals have to build their own connectors and maintain them as APIs change; Orbit's planned MCP server and SDK turn that work into standardized calls.
- **No long-tail market coverage.** Regional sports, real-time crypto narratives, emerging geopolitical events, fast-moving cultural moments: Polymarket and Kalshi do not prioritize them at the depth, speed, or localization that Asian retail distribution requires. Their strategy is depth over breadth, a deliberate choice that leaves the long-tail structurally underbuilt.

Polymarket and Kalshi go deep on high-visibility markets. The long-tail is underbuilt. Orbit starts with Asia-first distribution and expands toward agent-speed listing.

| Dimension | Existing platforms | What agents need |
| :---- | :---- | :---- |
| Event discovery | Manual, curated | Autonomous, streaming |
| Interface | Web UI | API, MCP, CLI, SDK |
| Execution speed | Human-paced | Agent-speed |
| Market coverage | Curated, high-visibility | Long-tail, real-time |
| Cross-market coordination | None | Native |
| Settlement trigger | Manual confirmation | Programmatic, on-chain |

---

# The Agent-Native Financial Decision Layer

AI agents are becoming economic actors. They research, reason, and make decisions across timescales and information volumes that exceed human capacity. As they take on more consequential financial roles, they need infrastructure that matches how they operate: account-scoped, programmable, auditable, and permissioned.

Wallets and payment rails aren't enough. An agent that holds USDC or USDT can transfer value. What it can't do is express a calibrated view on a future event, back that view with capital, and collect on it if it's right. Prediction markets close that gap, but only if the venue exposes software-readable market definitions, programmatic execution, and verifiable settlement.

Agents need four things that existing platforms don't provide together:

- A native probability layer they can read and write programmatically
- Scoped agent accounts with permissions, daily limits, and kill switches
- A trustless execution venue that settles without custodial intermediaries
- A verifiable settlement environment where outcomes can be challenged and audited on-chain

## Native Probability Layer

Orbit's prices are structured probability estimates. Agents consume them through APIs, SDKs, and the planned MCP interface, incorporate them into reasoning loops, and write new probability commitments back into the market through standardized calls.

## Scoped Agent Accounts

Agents operate through account structures that define what they can trade, how much capital they can deploy, and when human or protocol controls can stop them. This is what separates agent-native participation from borrowed API-key access to a human wallet.

## Trustless Execution Venue

Agents commit capital through signed orders that settle on-chain. Funds stay non-custodial from execution through settlement. Agents control positions from entry to expiry within scoped permissions, limits, and kill switches.

## Verifiable Settlement Environment

Every outcome is discoverable, disputable, and auditable. The Result and Settlement Agent proposes outcomes with evidence references stored on IPFS, subject to oracle and dispute paths defined for each market. Any participant can challenge a proposed outcome within the dispute window. Once the window closes without a valid challenge, settlement executes automatically. Agents can verify the entire resolution trail on-chain.

An agent that models event probabilities can progressively act on those models directly. Capital commitment, settlement, and cross-market coordination move from human-click workflows toward agent-speed execution.

---

# Architecture

Orbit's architecture organizes across three layers and a phased launch sequence:

![Architecture Diagram](/assets/image1.png)

- The interfaces through which participants connect
- The four agents that coordinate market formation and execution
- The core infrastructure that supports them

---

# Implementation Status and Launch Sequence

Orbit is deliberately phased. Live today: the CLOB matching engine, limit and market orders, market creation and lifecycle, UMA-based oracle resolution, USDC settlement on Base, non-custodial wallets, public REST/WebSocket API, LP pools, and fee accrual have been validated on testnet.

Mainnet Q4 '26: the Asia-first event venue launches with a mobile-first client, multi-chain USDC/USDT settlement, partner distribution widgets, geofence and jurisdictional KYC controls, programmatic SDKs, designated-oracle paths by market, and the MM Vault backed by committed LP capital.

Progressive agent layer: scoped agent accounts (ERC-4337), agent permissions, limits, kill switches, x402 agent-payment integration, MCP server and agent SDK, reputation-aware matching priority, conditional and correlated markets, deterministic resolution where data is available, and probabilistic data feeds.

## User and Agent Interfaces

Orbit exposes a unified interface layer that serves human participants and autonomous agent systems through consistent primitives.

**Human Chat, Mobile App, and KOL Widgets.** Human participants interact through a conversational interface, mobile application, and embedded KOL or partner widgets, discovering markets, executing trades, and monitoring positions in natural language. The interface abstracts protocol mechanics without restricting access to the underlying system.

**Autonomous Agents.** External AI agents are designed to participate in Orbit markets as first-class principals. Agents monitor event streams, assess probabilities, commit capital, and trigger resolution within scoped permissions, reducing the need for step-by-step human intervention.

**API, SDK, CLI, and MCP.** Developers and agent builders access the Orbit execution stack through structured interfaces. The public REST/WebSocket API supports the venue today; the SDK and MCP server progressively let language model-based agents call Orbit functions natively inside their reasoning loops.

**Partner Distribution.** Third-party platforms, KOL networks, data providers, and distribution partners embed Orbit market access through permissioned APIs and widgets, expanding coverage across regions and event categories.

**Memory and Strategy.** The agent layer maintains persistent state across markets, storing probability models, position history, and strategy parameters through the Memory layer in Orbit Core.

## The Four Agents

Orbit's market lifecycle is designed around four specialized agent modules, each responsible for a distinct phase of probability formation and resolution.

### 1. Event Discovery Agent

The Event Discovery Agent monitors public information streams continuously: news feeds, social signals, and on-chain activity. It detects genuine tradable uncertainty, filters candidates for originality and manipulation resistance, generates structured market definitions with clear resolution criteria, sources, deadlines, and edge-case handling, and surfaces opportunities before they become obvious to the broader market.

The agent prioritizes precision over volume. It identifies moments when genuine uncertainty exists, information is distributed, and a market would produce a meaningful probability signal.

### 2. Pricing Agent

The Pricing Agent converts detected uncertainty into actionable probability estimates. It runs a probability model ensemble incorporating cross-venue implied odds, multiple information sources, and conviction scoring based on evidence quality and consensus divergence.

The output structure:

- A probability range
- A confidence measure
- A recommended bid-ask spread
- Initial price weight relative to incoming order flow

### 3. Liquidity and Market Making Agent

The Liquidity and Market Making Agent aggregates and deploys capital across Orbit-native markets through the MM Vault and, where appropriate, external venues used for hedging and reference pricing. It commits capital based on market conditions, probability confidence, and portfolio-level risk parameters.

This agent enables sophisticated participants to provide liquidity in a structured, risk-aware way across many markets simultaneously, addressing the fragmentation that limits depth on existing platforms.

### 4. Result and Settlement Agent

The Result and Settlement Agent monitors each market through its full lifecycle toward resolution. It identifies when the underlying event has occurred, gathers evidence from multiple sources, and proposes the outcome with verifiable traceability.

The agent operates through an optimistic challenge mechanism and, where appropriate, UMA-based or designated-oracle paths. Proposed outcomes can be disputed within a defined window, with resolution determined by evidence quality and a bonded proposer system. Once the challenge period closes without a valid dispute, settlement executes deterministically on-chain.

## Orbit Core

Orbit Core is the execution environment through which all agents and participants operate.

**Chat and Mobile Client.** The conversational and mobile-first layer through which human participants discover markets, express intent, and receive structured information in natural language.

**Skills.** Modular capabilities agents invoke to perform specific tasks: market creation, position management, liquidity deployment, and settlement monitoring. Skills are composable and extensible.

**Agent Wallet.** A non-custodial wallet architecture designed for agent operation. It supports programmatic transaction signing, multi-market position management, scoped permissions, daily limits, kill switches, and integration with external wallet infrastructure. Agents manage capital within predefined authorization boundaries.

**Memory.** Persistent state storage for agents operating across multiple markets and sessions. Agents maintain probability models, position history, and strategy context across time.

## Infrastructure Rails

**LLM Gateway.** An optional managed interface between Orbit agents and language model infrastructure, providing consistent reasoning capabilities where agent workflows require them.

**Agent Wallet and ERC-4337.** Smart contract infrastructure for programmable, non-custodial capital management designed for agent-operated accounts.

**On-Chain Adapters.** Connectors to settlement chains and execution networks, letting Orbit interface with multiple on-chain environments without requiring participants to manage cross-chain complexity.

**RPCs and Data Sources.** Reliable access to blockchain state, price feeds, and information streams that agent components depend on for real-time decision-making.

**User Wallets.** Integration with standard wallet infrastructure, letting human participants connect and transact without friction.

**Stablecoin Settlement and Agent Payments.** Stablecoin payment rails supporting USDC/USDT-denominated positions and settlements without fiat-ramp dependencies, with x402 agent-payment integration planned as the agent layer matures.

**IPFS and Audit Hash.** Immutable evidence storage for resolution data, ensuring outcome verification can be independently audited and disputed.

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

---

# Business Model

Orbit's economic model aligns incentives around useful probability formation, genuine information contribution, sustainable market infrastructure, and market intelligence monetization over time.

## Fee Structure

Trading fees collect when participants execute against the order book. Fees flow through three primary destinations:

**Liquidity Providers and MM Vault participants** receive a portion of fees as compensation for supplying depth and absorbing risk over time. Fee distribution reflects effective liquidity contribution, aligning rewards with actual market support. At scale, the model targets a 0.5%-2% maker/taker fee range and an approximately 1% blended take rate, subject to market category, liquidity depth, and governance or operator configuration.

**Referral Rewards** fund ecosystem growth. A share of protocol revenue rewards users who bring new participants to the platform.

**Protocol Treasury** captures the remainder to support ongoing development, security, and governance.

Fee rates and allocation ratios are configurable and evolve through protocol governance and operator configuration decisions.

## Liquidity Provider Incentives

Liquidity providers play a central role in Orbit's market structure. They commit capital directly or through the MM Vault and supply depth across markets in exchange for fee income over time.

LPs earn fees from trading volume. When a market resolves against their committed position, they lose in proportion to how far their probability was from the actual outcome. Orbit's design rewards providers who bring genuine probability judgment to their positions.

The Liquidity and Market Making Agent helps sophisticated providers deploy capital in ways that reflect informed probability views and portfolio-level risk management.

## Trader Incentives

Traders identify and act on mispriced probabilities. Returns come from being earlier or more accurate than the market, with execution at the order book price at the time of the trade. Traders don't bear liquidity provision risk and interact with the order book directly.

## Referral Program

Users, creators, and KOL partners generate referral links that attribute a portion of future trading fees from referred participants back to the referrer. Referral rewards come from protocol revenue and reward long-term engagement, aligning creator-led growth with protocol sustainability.

## Agent Participants

As the agent layer activates, AI agents participate in Orbit's economic model as both liquidity providers and traders. Agents acting as liquidity providers earn fees through the same mechanism as human providers. Agents acting as traders capture returns from probability assessments that outperform the market consensus. The economic model treats agents and humans equivalently at the protocol level within account scopes and permissions.

## Market Intelligence and Data Products

Over time, Orbit can convert aggregated market prices, order flow, and settlement history into market data analytics and enterprise APIs. The product is not raw user data; it is capital-backed expectation data generated by participants revealing views through trades. This supports consumer intelligence, institutional market signals, and API products once real-money volume is deep enough to be reliable.

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

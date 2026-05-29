---
title: Implementation
nav_order: 6
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

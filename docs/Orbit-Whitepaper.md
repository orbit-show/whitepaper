---
title: "Orbit Whitepaper"
nav_order: 0
permalink: /
---

# Orbit Whitepaper

---

# Abstract

Orbit is the AI harness layer for event trading. Professional traders already use AI agents to automate prediction-market strategies. Orbit brings the same capabilities to anyone through plain language: a chatbot on top, an agent engine underneath.

Prediction markets have become a game most retail cannot win. Sophisticated players run automated strategies that take the other side, and the money flows one way. Orbit gives the same trader institutional-grade research, reasoning, and execution through an interface everyone already knows, and gives autonomous agents a native way to act.

Prediction markets are the entry point. The same intelligence layer expands to every market where decisions are made under uncertainty. Orbit aggregates and ranks the venues where event outcomes trade and routes execution across them non-custodially. It never holds funds and never takes a cut of an outcome. Positions and executions stay verifiable on-chain, non-custodial from execution through settlement.

Orbit begins by helping people trade probabilities and ends by helping them make better decisions wherever probabilities matter.

---

# The Problem

**Retail Is Getting Wiped Out**

Prediction markets have become a game retail cannot win. Sophisticated players run automated strategies that take the other side, and the money flows one way.

The numbers are stark: roughly 70% of players lose money, about 76.5% of all profit accrues to the top 1% of traders and 67% to the top 0.1%, and fewer than 2% ever clear $1,000 in profit. Across 2.4 million users and $67 billion traded, only about 16% of wallets are ever net profitable.

The tooling that closes this gap already exists: continuous research, disciplined execution, position sizing, risk limits, and hedging. It exists only for those who can build and run it, and it has never been packaged for a non-technical user. That is the gap Orbit closes.

*Sources: Akey, Grégoire, Harvie and Martineau (SSRN, 2026); WSJ and Bloomberg (2026); on-chain wallet analysis of 2.5 million addresses (April 2026).*

---

# Why Now

**AI Agents Are Becoming the OS for Financial Decisions**

Three trends converge, and Orbit sits where they meet.

- **Critical mass.** Prediction markets are now a live, liquid feed on what the world expects. Volume has grown roughly 5x year over year and clears billions of dollars in monthly volume.
- **Agents can act.** AI can finally research, reason, and execute on a user's behalf. This capability is new as of this year.
- **Retail still manual.** Information has exploded, but retail still trades by hand while professionals use software.

---

# The Solution

**Trade Like a Pro**

Keep trading the way you do now and you are on your own, jumping between news, social feeds, and venues by hand. Turn on Orbit and the same trader gets institutional-grade research, reasoning, and execution through a chatbot-like interface everyone is now familiar with.

- **Democratize.** Professional tooling behind a chat box.
- **Augment.** The odds, and the reasoning behind them.
- **Execute.** Deploy, monitor, and hedge by chatting.

Manual and outgunned becomes augmented and winning.

---

# Technology Architecture

**A Chatbot on Top, an Agent Engine Underneath**

The interface is simple on purpose. The defensibility is the engine in the middle.

![A chatbot on top, an agent engine underneath](/assets/architecture-diagram.png)

**User and Agent Interfaces.** The layer through which participants connect:

- Human Chat and App
- Autonomous Agents
- API, MCP, and SDK
- Partner Distribution
- Memory and Strategy

**Orbit Core (Chat × Skills × Agent Wallet).** The engine beneath the interface:

- **Agent Runtime:** Orchestration and planning of multi-step strategies.
- **Workflow:** Multi-step execution that carries an intent from research to a settled position.
- **Memory:** Context and history across markets and sessions.
- **MCP:** Tool and data connectors that expose Orbit and external sources to agents.
- **Regulatory and Compliance:** Jurisdiction and venue rules applied to what each participant can access and trade.
- **Risk Management:** Limits, sizing, and guardrails enforced before execution.
- **Agent Payments and Auth (OAP):** Scoped agent payment and authorization, so agents fund and settle within predefined boundaries.

**Venues and Data.** The foundation Orbit builds on:

- Every major event-trading venue
- News, social, macro, and on-chain signals

---

# Three Ways to Trade

**All in Plain Language**

Easy-to-use agentic trading, running for you around the clock, is what finally levels casual traders with the pros. Orbit exposes the engine through three entry points, each in plain language.

### Skills: Prebuilt Strategies

Ready-made strategies that run on your own account the moment you switch them on. Each skill packages a professional playbook, from market discovery to position management and settlement monitoring, into a single action, so a non-technical trader gets institutional discipline without writing code or tracking the market by hand.

### Copy Trading: Follow Proven Traders

Mirror the participants who are actually winning. Orbit ranks traders by a verified, on-chain track record, so you allocate to demonstrated performance rather than to marketing, and every position you copy executes on your own account and stays non-custodial.

### Your Own Agent: Build One by Chatting

Describe the strategy you want in plain language and Orbit assembles an agent that runs it for you around the clock. The agent watches the relevant event streams and acts on your behalf, always inside the scoped permissions, daily limits, and kill switches you set, so handing off the work never means handing off control.

---

# Market Size

**Prediction Markets Are the Entry, Decision Intelligence Is the Destination**

Prediction markets are where AI can first research, reason, and execute on probabilistic outcomes end to end. The same intelligence layer expands to every market where decisions are made under uncertainty.

- **The wedge.** Roughly $24 billion in monthly prediction-market volume.
- **The expansion.** Global financial markets past $100 trillion.
- **The destination.** The trillions in capital allocated under uncertainty every day.

Orbit begins by helping people trade probabilities and ends by helping them make better decisions wherever probabilities matter.

---

# Competitive Landscape

**Everyone Owns One Layer, Orbit Unifies Them**

![Everyone owns one layer, Orbit unifies them](/assets/competitive-landscape.png)

Each existing category owns one layer of the problem and stops there:

- **Prediction-market venues** own the layer where users trade probabilities.
- **Financial-intelligence tools** own research built for institutional workflows.
- **General AI assistants** own general question-answering.
- **Brokerages and trading apps** own execution for traditional assets.
- **Agent tooling** owns agent building and execution one venue at a time, with no cross-venue reputation layer.

Markets tell you the odds. Financial AI helps you understand why. Brokerages let you execute. Orbit combines all three into one AI-native interface: research across markets, news, social media, and financial data; reason using AI agents; execute trades across venues; and monitor positions and adapt as events unfold.

---

# Business Model

**How Orbit Makes Money**

Orbit is free to use, so anyone can start with zero commitment. The more trading Orbit automates, the more it earns. Orbit never holds funds and never takes a cut of an outcome. Every line is a fee for software or intelligence.

- **Free to use, fee per trade.** Orbit takes only a small portion of each trade you execute through it.
- **Premium features and skills.** A monthly plan for premium skills, unlimited copy-trading, and custom agents that monitor and act around the clock inside limits you set.
- **Intelligence and API.** The intelligence layer, licensed via API: data analytics, event discovery, and consumer insights. What is licensed is capital-backed expectation data, the views participants stake real money on, which is what makes it accurate and expensive to replicate.

---

# Go to Market

**Aggregator First, Agents to Convert**

Orbit aggregates prices, liquidity, and traders across every venue into one ranking layer. This is the data spine that draws traffic before anyone trades.

The flywheel compounds:

- Free rankings draw eyeballs.
- Better rankings pull the next wave.
- Their trades enrich the rankings.
- Agents convert visitors into traders.

The dataset is the moat. Every trade routed through Orbit sharpens the rankings and builds a verified, cross-venue track record no single venue can see. It compounds with each user and takes years to replicate.

---

# Risks

Participation in prediction markets involves meaningful risk. Orbit improves market structure and aligns incentives, but it does not eliminate uncertainty. Participants should weigh the following before engaging.

## Market Risk

Prediction-market prices reflect collective beliefs at a point in time. They can be wrong for extended periods, fail to converge before expiry, or shift sharply on new information.

## Liquidity and Execution Risk

Depth sits on the underlying venues Orbit routes to and varies over time and across probability ranges. Slippage, weak execution, and difficulty entering or exiting positions remain possible, especially in thin or fast-moving markets.

## Resolution and Settlement Risk

Outcomes resolve through each underlying venue and its oracle or dispute mechanism. Delays, ambiguities, or contested evidence can affect the timing or correctness of settlement.

## Agent System Risk

Orbit relies on coordinated autonomous agents to research, reason, and execute. Failures, adversarial inputs, or unexpected behavior in any agent can affect decision quality or execution, and may propagate in ways that are hard to anticipate.

## Smart Contract Risk

Non-custodial execution and settlement depend on on-chain contracts. Bugs, exploits, or edge-case interactions can result in partial or total loss. Code should be independently audited, and vulnerabilities can still exist.

## Regulatory and Legal Risk

Prediction markets face varied and evolving legal treatment across jurisdictions. Access, geofencing, jurisdictional KYC, available markets, and product features may change as frameworks develop, and participation may carry legal restrictions depending on the user's jurisdiction.

## Competitive Risk

High-volume venues are extending into prediction markets with existing liquidity and users. Distribution speed, cross-venue aggregation, and the maturation of agent-native participation will determine who builds the durable position.

## Experimental Status

Architecture, agent behavior, economic parameters, and sequencing reflect current design intent and may change as the product develops and governance evolves.

## Agent-Native Adoption Risk

The progressive agent layer depends on autonomous agents becoming a meaningful share of participation, on an uncertain timeline. Orbit's near-term thesis does not require this shift: the product is configured to serve human-driven event trading today, and the same architecture compounds if agent adoption accelerates.

---

*Orbit Whitepaper, v3 working draft. For the latest published version, visit whitepaper.orbit.show.*

---

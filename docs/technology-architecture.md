---
title: "Technology Architecture"
nav_order: 5
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

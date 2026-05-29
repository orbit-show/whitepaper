---
title: Pain Points
nav_order: 3
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

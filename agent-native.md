---
title: Agent-Native Layer
nav_order: 4
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

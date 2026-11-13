# Agent business (working name to come)

**One line:** an AI agent engine configured per business, with an owner dashboard. The first target is an AI receptionist for salons and barbershops: it answers texts and calls, makes bookings, and the owner sees every conversation and action.

**Status (13 November 2026):** research stage. On the site, `/work/` says "Now building: AI agents that handle bookings, calls and messages for small businesses."

## The idea (Zyad's words, summarized)
- Like the early "GPT wrappers", but built on the new agent products (Meta's Muse, Hermes Agent, OpenAI's Dots, Grok Bot). Sell one product to many kinds of business: salons (bookings, calls, messages), construction firms, law firms, people who want help with daily tasks and email.
- One engine for everyone with minimal changes per client. A "conglomerate of software as a service".
- Move fast, before businesses start using these agents directly.

## What the research found (from his chat with another AI)
- **Muse, Dots and Grok Bot can't be wrapped as products.**
  - **Grok Bot** is a closed subscription product.
  - **Muse** is a consumer app. Developers get the **Muse Spark models** through the Meta Model API, plus a connectors program.
  - **Dots** are tied to personal ChatGPT accounts. OpenAI's developer route is the Agents API.
  - Reselling personal subscriptions is likely against the terms.
- **What can be built on:**
  - **Hermes Agent:** open source (MIT), self-hostable, works with any model, and talks over messaging channels.
  - **Model and agent APIs:** Meta Model API (Muse Spark), OpenAI Agents API, the Grok API (with voice), Claude API and Agent SDK.
  - Keep the model swappable.
- **The architecture to build once:**
  1. A messaging layer (SMS via something like Twilio, web chat, later voice) that stores every message.
  2. The agent runtime with a per-client config: persona and rules, knowledge, enabled tools, channels, and approval rules.
  3. A tool library (calendar and booking, email, CRM, payments), built once as MCP-style connectors.
  4. An owner dashboard: transcripts, bookings, what the AI did, and a "take over" button.
  5. Approval rules, so it asks the owner before refunds, price changes or anything unusual.
- **Pushback worth keeping:**
  - **Agents don't "self-learn" by default.** Build memory, a knowledge base and a human review loop instead.
  - **Sell one vertical first** (salons and barbershops), then add law firms or trades as new configs.
  - **Be careful with legal clients.** Confidentiality and liability make law firms a later step.
  - **The moat is not the AI.** It's the integrations, the data in the dashboard, and being the one who sets it up and fixes it. Distribution to non-technical owners is the edge.
  - **Charge for outcomes,** such as bookings handled.

## Next
- Pick the stack (a model API plus a voice API; Hermes only if he needs the always-on agent).
- Design the tenant config and database schema, and price it per client.
- Pitch Canoegy's existing clients and a few local shops first.

---
title: "A2A Agents, Distributed Systems, and an AI That Reads Streets — GDG DC Recap"
date: 2025-04-17 20:00:00 -0400
categories: [Events, AI & Tools]
tags: [a2a, agents, distributed-systems, google-adk, gdg, llm]
---

Attended a GDG (Google Developer Group) event today, co-hosted by George Washington University and Northeastern University. The main speaker was **Noble Ackerson**, a Google Developer Expert for AI/ML, and the talk centered on distributed systems, agent orchestration, and the emerging A2A (Agent-to-Agent) protocol.

## The Talk: Orchestrating A2A Agents

Noble walked through how to think about multi-agent architectures — not just spinning up a single LLM, but designing systems where agents communicate, delegate, and coordinate across tasks. The A2A protocol is Google's answer to the question of how agents built on different frameworks can interoperate. The key ideas he touched on:

- **Distributed task execution** — breaking a complex workflow into agent-handled subtasks
- **Agent discovery and delegation** — agents knowing when to hand off to a specialized peer
- **Google ADK + AgentEngine** as the scaffolding for deploying and managing these systems in production

For someone working on multi-step pipelines (like my SEC EDGAR extraction work), the mental model maps well — each stage of extraction, validation, and classification could theoretically be an agent with a defined capability scope.

## The Standout: Invisible City

The demo that stuck with me was his **Invisible City** project. The premise: can an AI read the surface of a street — manholes, hydrants, spray-painted utility codes — and reason about what infrastructure lies underground, the way an experienced utility worker would?

He built it as a multi-agent vision system using Google ADK, AgentEngine, and the A2A protocol. Each agent handles a piece of the pipeline — detecting markers, matching against known utility codes (like APWA color standards), and synthesizing a ground-level inference about what's below.

It's explicitly framed as an experiment, not a production utility tool. But as a proof of concept for vision + reasoning + multi-agent coordination, it's one of the cleaner end-to-end demos I've seen. The full walkthrough is on YouTube: [watch here](https://www.youtube.com/watch?v=f-oLhICo_zI).

## Takeaway

The event was a solid reminder that the interesting work in agentic AI right now isn't in making a single model smarter — it's in the orchestration layer. How do agents discover each other? How do they negotiate task boundaries? How do you make the whole system observable and debuggable?

Those are open engineering problems, and GDG DC seems to be a good venue for engaging with people actively building on them. Worth attending the next one.

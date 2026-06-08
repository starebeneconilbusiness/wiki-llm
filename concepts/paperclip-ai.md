---
title: Paperclip AI Orchestration
created: 2026-06-08
updated: 2026-06-08
type: concept
tags: [paperclip, orchestration, agent, project]
sources: [raw/articles/paperclip-ai-overview.md]
confidence: high
---

# Paperclip AI Orchestration

## Overview
Paperclip.ai is an open-source, self-hosted system for managing AI agents as a structured team — like running a company, not just prompting tools.

## Key Concepts
- **Org Chart:** Hierarchical structure (CEO, CTO, engineers, marketers) — any agent (Claude, Codex, Cursor, OpenClaw, Hermes, Gemini, Pi, OpenCode) can be hired
- **Goal Alignment:** Every task traces back to a mission — agents understand what and why
- **Cost Control:** Monthly budgets per agent, auto-pause at 100%, warning at 80%
- **Ticket System:** All work via structured tickets with owners, status, threads. Immutable audit log (append-only)
- **Governance:** User approves hires and strategies. Can pause/resume/terminate any agent
- **Heartbeats:** Agents wake on schedule (4h/8h/12h), delegation flows up/down org chart
- **Model-Agnostic:** Works with any agent runtime that accepts a heartbeat
- **Multi-Company:** Single deployment can run dozens of isolated companies

## Status
- User wants to build a system of this type
- Claude and Codex are already discussing it
- Docs: https://docs.paperclip.ing/
- GitHub: https://github.com/paperclipai/paperclip

## Relationships
- [[wiki-llm]] — this wiki is part of the Paperclip project prep
- [[hermes-config]] — Hermes is one of the agents to orchestrate

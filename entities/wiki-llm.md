---
title: Wiki-LLM Project
created: 2026-06-08
updated: 2026-06-08
type: entity
tags: [wiki-llm, project, automation]
sources: []
confidence: high
---

# Wiki-LLM Project

## Overview
Self-hosted wiki system curated by an LLM (Hermes Agent) via scheduled cron jobs. The wiki serves as persistent project memory and knowledge base.

## Key Facts
- **Repo:** https://github.com/starebeneconilbusiness/wiki-llm
- **Location:** ~/wiki/ on the server
- **Curator:** Hermes Agent via hourly cron job
- **Purpose:** Keep project memory lean by migrating durable facts from Hermes memory to a structured wiki
- **Structure:** SCHEMA.md (conventions), index.md (navigation), entities/, concepts/, comparisons/, queries/, raw/ (immutable sources), log.md (changelog)

## Relationships
- [[paperclip-ai]] — wiki is part of Paperclip project preparation
- [[hermes-config]] — Hermes Agent curates this wiki
- [[server-infrastructure]] — wiki files live on this server

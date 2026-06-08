---
title: n8n Instance
created: 2026-06-08
updated: 2026-06-08
type: entity
tags: [n8n, infrastructure, domain]
sources: []
confidence: high
---

# n8n Instance

## Overview
n8n workflow automation platform, self-hosted on Docker.

## Key Facts
- **Domain:** n8n.crigamo3.com (Cloudflare managed)
- **Location:** /home/gavadala/n8n-stack/
- **Postgres:** v16, user: n8n, db: n8n
- **Redis:** v7
- **Network:** n8n-stack_default

## Relationships
- [[odoo-19-docker]] — shares postgres and redis
- [[server-infrastructure]] — runs on same server
- [[cloudflare-tunnel]] — domain managed by Cloudflare

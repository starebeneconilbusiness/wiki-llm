---
title: Server Infrastructure
created: 2026-06-08
updated: 2026-06-08
type: entity
tags: [server, infrastructure, docker, cloudflare]
sources: []
confidence: high
---

# Server Infrastructure

## Overview
Self-hosted Linux server running multiple Docker Compose stacks with Cloudflare Tunnel for HTTPS.

## Key Facts
- **Cloudflare Tunnel/reverse proxy** — custom domains work on HTTPS/443 without explicit port mapping
- **No Nginx needed** in containers — Cloudflare handles SSL termination
- **Docker:** User runs without sudo (user in docker group)
- **Stacks:**
  - n8n-stack: /home/gavadala/n8n-stack/ (postgres 16, redis 7)
  - odoo-vault: /home/gavadala/odoo-vault/ (odoo 19, vault)

## Relationships
- [[n8n-instance]] — n8n stack
- [[odoo-19-docker]] — Odoo stack
- [[cloudflare-tunnel]] — reverse proxy

---
title: Odoo 19 Docker Installation
created: 2026-06-08
updated: 2026-06-09
type: entity
tags: [odoo, docker, infrastructure, domain]
sources: []
confidence: high
---

# Odoo 19 Docker Installation

## Overview
Odoo 19 Community Edition running on Docker Compose, self-hosted.

## Key Facts
- **Location:** /home/gavadala/odoo-vault/
- **Domain:** odoo.crigamo3.com (Cloudflare managed, HTTPS)
- **Postgres:** Uses n8n-postgres (postgres 16, container n8n-postgres)
- **Redis:** Uses n8n-redis (redis 7, container n8n-redis)
- **Network:** n8n-stack_default (external)
- **Vault:** hashicorp/vault:1.20 on port 8200, token: myroot
- **DB Status:** Database 'odoo' created and active
- **Admin Login:** admin / Odoo@2026!Secure (password reset 2026-06-09)
- **Postgres User:** odoo / odoo_pg_pass_2026 (host: n8n-postgres)
- **Login URL:** https://odoo.crigamo3.com/web/login

## Relationships
- [[n8n-instance]] — shares postgres and redis
- [[server-infrastructure]] — runs on same server
- [[cloudflare-tunnel]] — domain managed by Cloudflare
- [[hashicorp-vault]] — Vault included in same compose

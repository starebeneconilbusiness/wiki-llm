---
title: Odoo 19 Docker Installation
created: 2026-06-08
updated: 2026-06-08
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
- **DB Status:** Database 'odoo' NOT yet created in postgres — needs `CREATE DATABASE odoo;` in n8n-postgres container

## Relationships
- [[n8n-instance]] — shares postgres and redis
- [[server-infrastructure]] — runs on same server
- [[cloudflare-tunnel]] — domain managed by Cloudflare
- [[hashicorp-vault]] — Vault included in same compose

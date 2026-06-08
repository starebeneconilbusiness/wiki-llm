---
title: Hashicorp Vault
created: 2026-06-08
updated: 2026-06-08
type: entity
tags: [vault, infrastructure, docker]
sources: []
confidence: high
---

# Hashicorp Vault

## Overview
Hashicorp Vault for secrets management, running in Docker alongside Odoo.

## Key Facts
- **Image:** hashicorp/vault:1.20
- **Port:** 8200
- **Token:** myroot
- **Location:** Part of odoo-vault compose stack

## Relationships
- [[odoo-19-docker]] — same compose stack
- [[server-infrastructure]] — runs on same server

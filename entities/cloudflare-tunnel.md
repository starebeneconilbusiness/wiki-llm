---
title: Cloudflare Tunnel
created: 2026-06-08
updated: 2026-06-08
type: entity
tags: [cloudflare, network, domain, infrastructure]
sources: []
confidence: high
---

# Cloudflare Tunnel

## Overview
Cloudflare Tunnel provides HTTPS access to self-hosted services without port forwarding or Nginx.

## Key Facts
- Custom domains on HTTPS/443 without explicit port mapping
- Managed domains: odoo.crigamo3.com, n8n.crigamo3.com
- No Nginx reverse proxy needed in containers

## Relationships
- [[server-infrastructure]] — part of server setup
- [[n8n-instance]] — n8n.crigamo3.com
- [[odoo-19-docker]] — odoo.crigamo3.com

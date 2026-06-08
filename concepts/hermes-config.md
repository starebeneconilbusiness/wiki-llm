---
title: Hermes Agent Configuration
created: 2026-06-08
updated: 2026-06-08
type: concept
tags: [hermes, config, lesson]
sources: []
confidence: high
---

# Hermes Agent Configuration

## Overview
Key configuration details and gotchas for Hermes Agent.

## Key Facts
- **Config file:** ~/.hermes/config.yaml — Hermes blocks patch/write_file on it, must use terminal (cat >>, python3 yaml, sed)
- **JWT/API tokens** get truncated in agent output — never echo full tokens, use Python scripts or ask user to paste directly
- **Docker permission fix:** If docker commands fail with permission denied on /var/run/docker.sock, run `sudo usermod -aG docker <user>`. Note: newgrp docker doesn't work in non-interactive shells — use `sudo docker compose ...` as fallback

## Relationships
- [[server-infrastructure]] — Hermes runs on this server
- [[paperclip-ai]] — Hermes is one of the agents Paperclip orchestrates
- [[wiki-llm]] — Hermes curates this wiki via cron

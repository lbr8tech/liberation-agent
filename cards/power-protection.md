---
type: "lbr8 Protocol Card"
title: "Server Power Protection"
description: "Use a laptop battery or UPS to prevent data corruption from sudden power loss on your self-hosted server."
tags:
  - "phase-4"
  - "data"
  - "basic"
  - "p4"
  - "data-breach"
  - "infrastructure-dependency"
related:
  - "cards/backup-strategy.md"
  - "cards/server-health-monitoring.md"
draft: true
---
> ⚠️ **This card is a work in progress.** It has not been reviewed for accuracy or completeness. Use at your own risk — verify any recommendations against primary sources before acting on them.


## Steps

### General

Protect your server from sudden power loss:

1. Laptop as server: battery is a built-in UPS — no additional hardware needed. Configure graceful shutdown at low battery (e.g. 15%).
2. Desktop/server: UPS with USB cable + NUT (Network UPS Tools) for graceful shutdown.
3. Configure: on power loss, send alert + initiate graceful shutdown after 2-3 minutes.
4. Test: pull the plug and verify the server shuts down cleanly, not hard-crashes.

Data corruption from sudden power loss is the #1 cause of Docker volume and database corruption. A $40 UPS or a laptop battery prevents this entirely.

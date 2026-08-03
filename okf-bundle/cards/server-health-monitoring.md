---
type: "lbr8 Protocol Card"
title: "Server Health Monitoring"
description: "Monitor disk health, container status, and system resources to catch failures before they cause data loss."
tags:
  - "phase-5"
  - "data"
  - "intermediate"
  - "p5"
  - "data-breach"
  - "infrastructure-dependency"
  - "agency-loss"
prerequisites:
  - "cards/backup-strategy.md"
related:
  - "cards/backup-strategy.md"
  - "cards/power-protection.md"
---

## Steps

### General

Monitor your server so problems are caught before they cause data loss:

1. Disk health: SMART monitoring with smartmontools — check SSD wear, reallocated sectors, temperature. Email alerts on degradation.
2. Docker container health: script or Uptime Kuma to check all containers are running. Alert on unexpected stops.
3. Disk space: alert at 80% full — Docker logs and volumes silently fill disks.
4. System resources: CPU, RAM, temperature — alert on sustained high usage.
5. Notifications: email (via SMTP relay) or push notification. For single-server setups, a simple cron script + email is enough.

For a repurposed laptop (8+ years old): prioritize SMART monitoring — SSD failure is the most likely hardware issue. Check weekly, alert on any degradation.

## Self-Hosted

smartmontools + cron + email alerts

Alternatives: Uptime Kuma (web UI, Docker container monitoring), Cockpit (web UI, system monitoring)

## Prerequisites

Backups should be in place before monitoring matters.

---
type: "lbr8 Protocol Card"
title: "Server Backup Strategy"
description: "Establish a 3-2-1 backup strategy with encrypted offsite copies before self-hosting any sensitive data."
tags:
  - "phase-4"
  - "data"
  - "intermediate"
  - "p4"
  - "data-breach"
  - "agency-loss"
  - "infrastructure-dependency"
prerequisites:
  - "cards/mesh-vpn.md"
related:
  - "cards/server-health-monitoring.md"
  - "cards/power-protection.md"
draft: true
---
> ⚠️ **This card is a work in progress.** It has not been reviewed for accuracy or completeness. Use at your own risk — verify any recommendations against primary sources before acting on them.


## Steps

### General

Before self-hosting sensitive data, establish a backup strategy:

1. 3-2-1 principle: 3 copies of data, 2 different media, 1 offsite
2. Docker volumes: schedule periodic backups with a cron script (stop container, copy volume, restart)
3. Test restores: a backup you haven't restored is just a guess — verify quarterly
4. Offsite: push encrypted backups to cloud storage (BorgBase, Backblaze B2, or rsync to a remote server)
5. Rotation: keep daily (7), weekly (4), monthly (3) snapshots — don't overwrite all copies
6. Encryption: encrypt backups before they leave the server — the offsite target should never see plaintext

For a single-server setup (repurposed laptop): Docker volume backups to an external drive + encrypted offsite to cloud storage. Weekly cron + monthly test restore.

## Self-Hosted

BorgBackup (deduplicating, encrypted, FOSS) + cron

Alternatives: Restic (simpler, cloud-native), Duplicati (web UI)

## Prerequisites

Need server access set up first.

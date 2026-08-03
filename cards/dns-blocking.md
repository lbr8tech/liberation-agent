---
type: "lbr8 Protocol Card"
title: "DNS-Level Blocking"
description: "Block ads, trackers, and malware at the DNS level using NextDNS (cloud) or AdGuard Home (self-hosted)."
tags:
  - "phase-3"
  - "network"
  - "intermediate"
  - "p3"
  - "tracking"
  - "ad-targeting"
  - "malware"
related:
  - "cards/router-dns.md"
  - "cards/mesh-vpn.md"
draft: true
---
> ⚠️ **This card is a work in progress.** It has not been reviewed for accuracy or completeness. Use at your own risk — verify any recommendations against primary sources before acting on them.


## Steps

### General

Cloud (NextDNS): Configure per-device via NextDNS app (Android) or profile (iOS), or set up in router for all devices. Self-hosted (AdGuard Home): Install on any server (Raspberry Pi, LXC, NAS). Point your router DNS to it. All DNS queries stay on your network — no private company sees your browsing data. Full control over blocklists, custom filters, and logging.

Verify (3 min): After pointing your router DNS to AdGuard Home, run dnsleaktest.com (Extended Test). You should see your self-hosted resolver or no third-party DNS at all — NOT your ISP or any cloud provider. Also visit 1.1.1.1/help to confirm the resolver hostname. Check the AdGuard Home query log to see real-time blocked vs allowed queries.

## Self-Hosted

AdGuard Home (self-hosted on Raspberry Pi, LXC, or any server)

Alternatives: Pi-hole (older, less feature-rich), TomSparkBox (one-command installer that bundles AdGuard Home + Pi-hole + 40+ other apps — tomsparkbox.com. Closed-source integration layer over open-source apps. Untested by lbr8.)

## Cloud

NextDNS (per-device or router-level)

**Privacy note:** NextDNS logging is ON by default. MUST disable all logging during setup. See router-dns card for details. You are shifting trust from ISP to NextDNS (4-person US company). If this concerns you, self-host instead.

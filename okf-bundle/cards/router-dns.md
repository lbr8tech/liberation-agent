---
type: "lbr8 Protocol Card"
title: "Router DNS Configuration"
description: "Change your router's DNS to a filtered resolver that blocks tracking, ads, and malware for every device on your network."
tags:
  - "phase-3"
  - "network"
  - "intermediate"
  - "p3"
  - "tracking"
  - "malware"
  - "big-tech-surveillance"
related:
  - "cards/dns-blocking.md"
  - "cards/mesh-vpn.md"
---

## Steps

### General

Log into router admin (usually 192.168.1.1 or 192.168.0.1). Change DNS servers from ISP default to a filtered resolver. This applies DNS blocking to ALL devices on your network, not just one phone.

**Verify (3 min):** After changing DNS, confirm it actually took effect. Go to dnsleaktest.com and run the Extended Test — it shows which DNS resolver is handling your queries. You should see your chosen resolver (NextDNS, AdGuard, etc.), NOT your ISP. Also visit 1.1.1.1/help — it shows your connected resolver and whether DoH is active. If you still see your ISP, your router is using the old DNS cache — reboot it, or check for a hardcoded DNS override on individual devices.

## Self-Hosted

AdGuard Home (self-hosted on a Raspberry Pi, LXC, or any server)

## Cloud

NextDNS (configure in router, all devices benefit)

**Privacy note:** NextDNS enables logging by default (3 months, US servers). MUST disable all logging during setup: Settings → Logs → disable all log retention. Set analytics to disabled. Choose EU server if outside US. NextDNS is a 4-person US company — your DNS queries are visible to them. If this concerns you, self-host AdGuard Home (see dns-blocking card).

## Sources

1. nextdns.io/privacy
2. help.nextdns.io/t/y4hmvar
3. privacyguides.org/en/dns/
4. tailscale.com/docs/integrations/nextdns

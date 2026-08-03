---
type: "lbr8 Protocol Card"
title: "Own Your Router & Flash Custom Firmware"
description: "Replace your ISP-provided router with one you control, then flash OpenWrt for ongoing security updates."
tags:
  - "phase-3"
  - "network"
  - "advanced"
  - "p3"
  - "tracking"
  - "malware"
  - "big-tech-surveillance"
  - "infrastructure-dependency"
prerequisites:
  - "cards/router-hardening.md"
related:
  - "cards/router-hardening.md"
  - "cards/router-dns.md"
  - "cards/network-segmentation.md"
  - "cards/dns-blocking.md"
draft: true
---
> ⚠️ **This card is a work in progress.** It has not been reviewed for accuracy or completeness. Use at your own risk — verify any recommendations against primary sources before acting on them.


## Steps

### General

Your ISP-provided router is the most privileged surveillance point in your digital life. The ISP controls the firmware — what it reports back, what data it collects, what features it activates. At least 30 million US homes already have Wi-Fi sensing (motion detection through walls) available in their ISP routers, and the gap between lab demos (identifying individuals, reconstructing poses through walls) and commercial deployment is just a firmware update.

Step 1 — Replace ISP router with your own:
1. Buy a router (or a mini PC for OPNsense/pfSense): $50-150 for a consumer router, $150-300 for x86 mini PC
2. Call your ISP and ask to put your modem into "bridge mode" (disables its router/Wi-Fi, passes through to your router). If they don't offer bridge mode, ask for a pure modem (no router)
3. Connect your router to the modem, configure it from scratch
4. You now control: firmware, DNS, Wi-Fi sensing, telemetry, update schedule

If your ISP claims you "must" use their router: in most cases this is false. US ISPs are required to let you use your own equipment. Some ISPs (e.g. fiber providers) may require their ONT, but you can still put it in bridge mode.

Step 2 — Flash custom firmware (optional but recommended):
1. Check if your router is supported: openwrt.org/toh/start
2. Flash OpenWrt (follow device-specific guide carefully — can brick router)
3. Configure: set admin password, disable UPnP/WPS (same as router-hardening), install LuCI web interface
4. Add packages: adblock (DNS blocking), wireguard/VPN, firewall rules, VLAN support
5. Benefits: security updates for years, full control, packages for anything your router hardware can run

OPNsense is the x86 upgrade: runs on dedicated hardware (old PC, mini PC, or purpose-built box). BSD-based, built-in intrusion detection (Suricata), VPN, DNS filtering, VLAN support — replaces consumer router entirely.

Even with your own router, HTTPS doesn't hide DNS queries or traffic metadata from the ISP. Pair with encrypted DNS (DoH) and/or VPN for full protection.

## Self-Hosted

Own router (consumer or x86 mini PC) in bridge mode + OpenWrt

Alternatives: OPNsense on x86 mini PC (more powerful, BSD-based, intrusion detection), pfSense (commercial, BSD-based)

## Sources

1. youtube.com/watch?v=24_94bGpWQM (Proton: Your ISP Is Watching, and Your Router Is Its Eyes)
2. proton.me/how-isps-track-you
3. proton.me/wifi-surveillance
4. ftc.gov/reports/2021-staff-report-examining-data-practices-isps
5. privacyguides.org/en/router/overview/
6. openwrt.org/toh/start
7. opnsense.org/

## Prerequisites

Harden the router you have first — know what settings matter before replacing hardware and flashing firmware.

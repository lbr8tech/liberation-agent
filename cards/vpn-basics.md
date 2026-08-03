---
type: "lbr8 Protocol Card"
title: "Private Network VPN"
description: "Use a trusted VPN like Mullvad or ProtonVPN to hide your traffic from your ISP on public Wi-Fi or while traveling."
tags:
  - "phase-6"
  - "network"
  - "intermediate"
  - "p6"
  - "tracking"
  - "govt-surveillance"
---

## Steps

### General

Use when: public Wi-Fi (coffee shops, hotels, airports), travel (especially international), ISP sells your data (US ISPs can), torrenting. Do NOT use always-on unless your threat model requires it. Fix your browser first.

**Verify (3 min):** After connecting to your VPN, run dnsleaktest.com (Extended Test). You should see the VPN provider's DNS servers — NOT your ISP or your home DNS resolver. If your ISP appears, your VPN is leaking DNS (a common misconfiguration). Also run browserleaks.com/ip to confirm your public IP changed. For Mullvad, use their built-in leak check (mullvad.net/check) which tests both IP and DNS simultaneously.

## Cloud

Mullvad (audited, no-logs verified by Swedish police raid, anonymous accounts) or ProtonVPN (free tier available, audited)

**Privacy note:** A VPN does NOT make you anonymous. It moves trust from your ISP to the VPN provider. Websites still see you via cookies, browser fingerprinting, and logged-in sessions. A VPN hides DNS queries and TLS SNI from your ISP. It does not stop application-layer tracking.

## Sources

1. routeharden.com/blog/threat-models-for-network-anonymity
2. dev.to/ciokan/what-a-vpn-actually-protects-you-from
3. digitalcitizen.life/do-you-actually-need-a-vpn-in-2026

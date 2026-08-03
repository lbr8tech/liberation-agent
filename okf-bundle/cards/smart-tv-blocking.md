---
type: "lbr8 Protocol Card"
title: "Smart TV Hardening"
description: "Disable ACR tracking and telemetry, block TV domains at the DNS level, or turn your smart TV into a dumb display."
tags:
  - "phase-3"
  - "devices"
  - "intermediate"
  - "p3"
  - "big-tech-surveillance"
  - "tracking"
  - "data-breach"
prerequisites:
  - "cards/router-dns.md"
related:
  - "cards/router-dns.md"
  - "cards/dns-blocking.md"
  - "cards/network-segmentation.md"
  - "cards/self-hosted-media.md"
  - "cards/car-telemetry.md"
---

## Context for the Agent

This card is for users who want to stop their smart TV from collecting viewing data, sending telemetry, and serving ads. Smart TVs are surveillance devices that happen to display video — use this when the user mentions being creeped out by their TV's recommendations, seeing ads on their home screen, or receiving notifications from their TV manufacturer.

## Why This Matters

Smart TVs use Automatic Content Recognition (ACR) — a Shazam-like technology that captures snapshots of everything you watch, including streaming apps, cable, HDMI inputs, and Blu-ray players — and sends that data to manufacturer servers where it is sold to advertisers and data brokers. Vizio paid $2.2M to the FTC for collecting viewing data on 11 million TVs without consent. The Texas AG sued LG for secretly monitoring what consumers watched across all inputs. A 2024 UCL study confirmed that ACR tracking captures content from external devices connected via HDMI, meaning the TV surveilles even content you play from your own hardware. Samsung's 2025 "AI service terms" pop-up tells users they are responsible for obtaining consent from "any third parties whose voices may be captured" — effectively making the homeowner liable for wiretapping compliance. Samsung and Roku hardcode fallback DNS (8.8.8.8) to bypass user-configured DNS. The cleanest solution is a commercial display + external media box, eliminating the smart platform entirely.

## Coaching Flow

There are three escalation levels. Start at Level 1 and only escalate if the user wants stronger protection.

### Level 1: Settings Lockdown (5-15 min, no install)

Walk the user through every privacy-related setting on their TV. This is reversible and non-destructive.

**Samsung:**
- Settings → General → Smart Features → "Voice recognition services" OFF
- Settings → Support → "Terms and Conditions" → disable "Viewing Information Services"

**LG:**
- Settings → General → System → "Live Plus" OFF
- Settings → General → "AI Service" → disable "AI Brightness" and voice features

**Sony/Android TV:**
- Settings → Device Preferences → "Usage & Diagnostics" → OFF
- Settings → Apps → "Sony TV Core Services" → disable

**Roku:**
- Settings → Privacy → all options OFF (Smart TV Experience, Advertising, Microphone)

**Apple TV:**
- Settings → General → "Share Apple TV Analytics" OFF
- Settings → Privacy → "Limit Ad Tracking" ON

### Level 2: DNS-Level Blocking (requires router DNS setup)

If the user already has a DNS resolver (AdGuard Home, Pi-hole, or NextDNS) configured on their router (prerequisite: router-dns card), guide them to add smart TV tracking domain blocklists:
- Add HaGeZi's Smart TV blocklist [1] to their DNS resolver
- Add Perflyst's Smart TV blocklist [2] for additional coverage
- After adding, the TV should be rebooted, then check the DNS query logs to confirm tracking domains are being blocked

Note: Samsung and Roku hardcode 8.8.8.8 as a fallback DNS, which can bypass DNS-level blocking. If the user notices TV still tracking after DNS setup, escalate to Level 3.

### Level 3: Dumb TV Conversion (requires hardware)

This is the nuclear option. Guide the user to:
1. Disconnect the TV from the internet entirely (in TV settings, forget the WiFi network, or unplug the Ethernet cable)
2. Connect an external media device (Apple TV, Chromecast with Google TV, Fire Stick, Raspberry Pi running Kodi, or a dedicated streaming box) to an HDMI port
3. Configure the streaming box with privacy-friendly settings
4. The TV becomes a dumb display — all "smart" features are disabled

For self-hosted media, recommend the self-hosted-media card for setting up Jellyfin/Plex/Emby with a Raspberry Pi or similar device.

## Decision Points

There are three escalation levels. Ask the user: **How far do you want to go?**

- **Level 1 ("Let me just turn off the tracking settings"):** Guide them through the settings lockdown above. Takes 5-15 minutes, no installs, no hardware.
- **Level 2 ("I want network-level blocking"):** Requires the router-dns card to be completed first (AdGuard Home, Pi-hole, or NextDNS). Guide them to add the TV blocklists. May not work on Samsung/Roku due to hardcoded fallback DNS.
- **Level 3 ("I want to completely disconnect the TV from the internet"):** Requires an external media device. Guide them through disconnecting the TV and setting up a streaming box. This is the most effective but requires hardware.

Also ask: **What brand is your TV?** Samsung and LG settings are organized differently — the right brand determines which settings menu items to show.

## Pitfalls

- Warn that firmware updates can re-enable tracking after users disabled it (this has happened with multiple manufacturers). Check settings periodically.
- Warn that Samsung and Roku hardcode 8.8.8.8 as fallback DNS to bypass user-configured DNS — if you're doing DNS-level blocking, verify it's actually working by checking the DNS query logs.
- Warn that HDMI-CEC metadata can be used to track device usage patterns — this is harder to block and may require disabling CEC.
- Warn that LG has pushed adware onto monitors via Windows Update (2026) and force-installed Microsoft Copilot on TV home screens (2025) — the TV platform is actively hostile to user privacy.
- If the user is considering a new TV, recommend a commercial display (business/education model) which has no smart platform — it's a dumb monitor with multiple HDMI inputs.
- The cleanest solution is a commercial display + external media box, eliminating the smart platform entirely.

## Sources

1. [Gamers Nexus investigation: LG spyware in monitors and TVs, wiretapping concerns, Texas AG settlement](https://youtube.com/watch?v=Q9uefFYe6bM) — Comprehensive investigation covering ACR tracking, microphone concerns, firmware re-enabling tracking, and the Texas AG lawsuit

## Guides

1. [HaGeZi: DNS blocklists — smart TV and device tracking categories](https://github.com/hagezi/dns-blocklists)
2. [Perflyst: smart TV blocklist for Pi-hole/AdGuard Home](https://github.com/Perflyst/PiHoleBlocklist/blob/master/SmartTV.txt)
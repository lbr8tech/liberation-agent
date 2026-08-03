---
type: "lbr8 Protocol Card"
title: "Screen Time & App Blockers"
description: "Block distracting apps and websites with schedule-based, delay-access tools across all devices."
tags:
  - "phase-1"
  - "devices"
  - "basic"
  - "p1"
  - "digital-minimalism"
  - "ad-targeting"
related:
  - "cards/minimal-launcher.md"
  - "cards/notification-audit.md"
---

## Why

Your phone's interface is not designed for you. Every default — the infinite scroll, the autoplay, the pull-to-refresh, the red notification badges, the "you might also like" queue — is an engagement-prolonging design pattern engineered to maximize time-on-platform. Researchers identified 63 such patterns across the 17 largest online platforms, with social media apps using twice as many as any other category. Johann Hari, in Stolen Focus, argues that our attention did not collapse — it was stolen. Tristan Harris, a former Google design ethicist, blew the whistle on how the attention economy works: every second you spend scrolling is revenue, and every second you put the phone down, revenue stops. Some of the cleverest engineers in the world are paid to keep you hooked. App blockers and screen-time tools fight back by inserting friction — delays, schedules, grayscale, and hard limits — between you and the patterns designed to exploit your attention. You do not need to quit your phone. You need to change the defaults.

## Steps

### Android

<strong>Curbox</strong> (F-Droid, GPL-3.0, 1,079★) — the strongest FOSS app blocker:
1. Install from F-Droid. No internet permission — it physically cannot transmit your data
2. Block apps and websites completely, or use granular UI hiding to block just the addictive parts (e.g., hide the YouTube home feed but keep search, hide Instagram explore but keep DMs)
3. Short-form content blocker: specifically targets Instagram Reels and YouTube Shorts
4. App-specific grayscale: drain color from Instagram while keeping Camera in full color
5. Scheduled DND, usage-based limits (block WhatsApp after 1 hour), time-based access (allow only 7 AM–9 PM)
6. Unlock methods: strict blockade, timed unlocks, QR/barcode scan (forces you to get up), or sentence retyping
7. Tamper protection makes it hard to uninstall in moments of weakness

### iOS

<strong>ScreenZen</strong> (free, donation-supported, no subscription) — delay-based: inserts a pause screen before flagged apps open, breaking the autopilot tap-and-scroll loop. Also supports scheduled blackouts, daily time limits, cooldown periods, and a multi-step gesture unlock for harder enforcement. Available on iOS, Android, macOS, and Windows.

Alt: <strong>Burnout Buddy</strong> (free). For browser: <strong>SocialFocus</strong> ($3.99) + <strong>UnTrap for YouTube</strong> ($3.99).
Full iPhone setup guide: reysu.io/dumbphone

### Desktop

<strong>LeechBlock NG</strong> (MPL-2.0, open source, 1,050★) — browser extension for Firefox, Chrome, Edge, Brave, Opera, and Vivaldi:
1. Define up to 30 block sets with different sites, times, and days
2. Block within fixed time periods, after a time limit, or both (e.g., 10 min/hour between 9 AM–5 PM)
3. Lockdown mode for immediate blocking, delay mode with countdown, password protection
4. Wildcards (*.somesite.com), exceptions (+allowedsite.com), keyword blocking (~badword)

Available on Firefox Add-ons and Chrome Web Store.

## Sources

1. theguardian.com/science/2022/jan/02/attention-span-focus-screens-apps-smartphones-social-media (The Guardian: Your attention didn't collapse. It was stolen — Johann Hari on how the attention economy deliberately fractures focus)
2. npr.org/2018/02/06/583648004/former-google-executive-warns-smartphones-keep-us-hooked (NPR: Former Google design ethicist Tristan Harris on how smartphones keep users hooked)
3. arxiv.org/html/2411.12083v2 (arXiv: The Engagement-Prolonging Designs Teens Encounter on Very Large Online Platforms — 63 design patterns across 17 platforms, 583 instances)

## Guides

1. github.com/curbox-app/curbox-android (Curbox: open-source app blocker for Android)
2. github.com/proginosko/LeechBlockNG (LeechBlock NG: open-source website blocker for Firefox/Chrome)
3. screenzen.co (ScreenZen: free, donation-supported screen time app for iOS/Android/desktop)
4. reysu.io/dumbphone (Reysu: full dumbphone setup guide for iPhone)

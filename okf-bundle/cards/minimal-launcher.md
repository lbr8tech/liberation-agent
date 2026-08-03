---
type: "lbr8 Protocol Card"
title: "Minimal Phone Home Screen"
description: "Replace your cluttered launcher with a text-only, search-first home screen to reduce visual noise."
tags:
  - "phase-1"
  - "devices"
  - "basic"
  - "p1"
  - "digital-minimalism"
related:
  - "cards/screen-time-app-blockers.md"
  - "cards/notification-audit.md"
---

## Why

Your home screen is the primary surface for attention extraction. Every app icon, badge, and widget is engineered to pull you in. The average American spends nearly five hours a day on their phone, and half of users worry they use it too much — the design is working as intended.

A 2025 controlled trial tested a minimalist launcher that replaces the icon grid with an alphabetical list — no icons, no widgets, no visual cues. After 14 days, users reduced screen time by 15% and showed significantly reduced habitual phone behavior. The study concluded that removing visual cues and adding search friction disrupts unconscious app-opening patterns. As Johann Hari documented in Stolen Focus, tech companies' entire business model is built on figuring out "how to get you to open the app as often as possible and scroll as long as possible."

A minimal launcher removes the visual cues that trigger habitual phone pickup. Text-only, search-first interfaces eliminate the app grid — the swipe-and-scroll reflex — and make each app opening a deliberate choice.

## Steps

### Android

**Olauncher** (f-droid.org/packages/app.olauncher) — the recommended starting point. GPL-3.0, FOSS, text-only home screen with search-first design. Swipe up for app list, long-press to change apps. No icons, no widgets, no app drawer. Daily wallpaper option. Extremely lightweight.

**Alternatives:**
- **KISS Launcher** (f-droid.org/packages/fr.neamar.kiss) — the long-established F-Droid classic. 250KB, never connects to the internet, search-focused. Adapts to your usage patterns. GPLv3+.
- **Mako** (github.com/rama-io/mako) — privacy-first, only two permissions (no network access at all). Native Kotlin, verified on GrapheneOS. App grouping and quick actions.
- **Still Launcher** (github.com/8tp/still-launcher) — the strictest option: no internet permission, no Google Play Services, no telemetry, no icons, monochrome text-only. Designed for GrapheneOS but runs on any Android 8+.

**For power users who need deep customization:** **Total Launcher** (Play Store, com.ss.launcher2) is the most customizable Android launcher — every element can be repositioned, resized, and styled. Updated July 2026, 4.4★, 25K reviews. Caveat: closed source, Play Store only, and requires many permissions including internet, location, contacts, calendar, and microphone. Developer states no data is collected but this is unverifiable. Best choice if you want full control over layout and are comfortable with the privacy tradeoff.

### iOS

No launcher replacement is possible on iOS. Use these alternatives:
- **Focus Modes** (Settings → Focus) to hide all but essential apps during work/sleep hours
- **Screen Time** app limits (Settings → Screen Time) to cap specific apps
- **Blank widgets** on home screen + push everything to App Library (swipe left) to remove the visual grid
- **Grayscale** (Settings → Accessibility → Color Filters → Grayscale) to make the phone less visually stimulating
- **Dumbify** ($6.99 one-time) — replaces your home screen with a minimal text interface
- See reysu.io/dumbphone for a full iPhone setup guide

## Going Further

**The goal is intentionality, not deprivation**
A minimal launcher works because it adds friction — each app opening becomes a conscious decision rather than a reflexive tap. Research from the ACM CHI conference found that even small design frictions (like a one-second delay before an app opens) significantly reduce habitual app usage over time, and users become more intentional rather than just restricted.

**Combine with notification discipline**
A clean home screen won't help if your phone still vibrates with notifications. Turn off all non-essential notifications. Messages and calls should be the only things that interrupt you. See the notification audit card.

**Don't stop at the launcher**
The home screen is just the first layer. For deeper impact:
- Uninstall apps you haven't used in 30 days
- Move social media to the browser (no app icon = less temptation)
- Use grayscale mode to reduce the dopamine hit from colorful interfaces
- Set a daily "phone-free hour" — even one hour creates a pattern of intentional use

**The broader framework: Light Patterns**
This card is one instance of a broader concept: [Light Patterns](/wiki/light-patterns) — access mechanisms that promote agency, the inverse of dark patterns. Blocking by default, restoring on purpose, conversation before consumption, reflection after. The minimal launcher is a light pattern for your home screen. See also: [Dark Patterns](/wiki/dark-patterns) and [Intentionality](/wiki/intentionality).

## Sources

1. theguardian.com/science/2022/jan/02/attention-span-focus-screens-apps-smartphones-social-media (The Guardian: Johann Hari — "Your attention didn't collapse. It was stolen" — documents twelve proven factors reducing attention, including the business model of tech companies designed to undermine focus for profit)
2. sciencedirect.com/science/article/pii/S2451958825001149 (ScienceDirect, 2025: controlled trial of MinimalistPhone app — 14-day intervention using a text-list launcher reduced screen time by 15% and habitual phone behavior, confirming that removing icon grids and adding search friction disrupts unconscious app-opening patterns)
3. dl.acm.org/doi/full/10.1145/3613904.3642370 (ACM CHI, 2024: "one sec" self-nudge app study — adding a brief delay before app opens reduced target app usage by 57% over six weeks; the option to dismiss was the most effective friction component)

## Guides

1. olauncher.app (Olauncher — official website: text-only launcher for Android)
2. f-droid.org/packages/fr.neamar.kiss (KISS Launcher — official F-Droid page: search-focused, 250KB, zero internet)
3. github.com/rama-io/mako (Mako — official GitHub: privacy-first, two permissions, GrapheneOS-verified)
4. github.com/8tp/still-launcher (Still Launcher — official GitHub: strictest option, no internet permission, monochrome text-only)
5. f-droid.org/en/categories/launcher/ (F-Droid launcher category — FOSS Android launchers with verified no-tracker builds)
6. reysu.io/dumbphone (reysu.io: full guide to converting an iPhone into a minimal/dumb phone — Focus Modes, Screen Time, grayscale, widget tricks)

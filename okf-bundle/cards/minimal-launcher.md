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

## Context for the Agent

This card is for users who want to reduce phone screen time and break the unconscious app-opening reflex. Use it when the user has expressed concern about phone overuse, notification overload, or feeling addicted to their device.

## Why This Matters

Your home screen is the primary surface for attention extraction — every app icon, badge, and widget is engineered to pull you in. A 2025 controlled trial found that switching to a minimalist text-only launcher reduced screen time by 15% after 14 days, by removing the visual cues that trigger unconscious phone pickup. As Johann Hari documented, tech companies' business model is built on figuring out "how to get you to open the app as often as possible and scroll as long as possible" [1]. A minimal launcher swaps the swipe-and-scroll reflex for deliberate, search-based app opening.

## Coaching Flow

### Step 1: Check the user's platform
The user's device type is already known from onboarding. If they're on **Android**, proceed to Step 2. If they're on **iOS**, explain that iOS does not allow replacing the system launcher, but guide them to the reysu.io guide for converting an iPhone into a minimal/dumb phone using Focus Modes, Screen Time limits, grayscale mode, and widget removal. Recommend starting with grayscale (Settings → Accessibility → Display & Text Size → Color Filters) as an immediate low-effort intervention.

### Step 2: Install a minimal launcher (Android)
Recommend **Olauncher** as the starting point — it's GPL-3.0, FOSS, text-only, search-first. Walk the user through:
- Install from F-Droid (recommended) or GitHub
- Set it as the default home launcher when prompted
- Show them the gestures: swipe up for app list, long-press to change dock apps

Tell the user they can always switch back to their old launcher. This is completely reversible.

### Step 3: Present alternatives if Olauncher isn't the right fit
If the user wants something different, offer:
- **KISS Launcher** — 250KB, never connects to the internet, search-focused, long-established F-Droid classic [2]
- **Mako** — privacy-first, two permissions only, GrapheneOS-verified [3]
- **Still Launcher** — strictest option, no internet permission at all, monochrome text-only [4]

### Step 4: Offer the F-Droid launcher category for exploration
Let the user know they can browse all FOSS Android launchers with verified no-tracker builds on F-Droid's launcher category [5].

## Decision Points

No onboarding-level questions needed here. The main decision is **which launcher fits their preferences** — guide them through the options in Step 3 and let them pick.

## Pitfalls

- Warn the user that muscle memory for their old launcher will take a few days to fade. The 2025 study showed benefits at 14 days — encourage them to commit to at least a week.
- Warn that some minimal launchers may not support widgets they depend on (calendar, weather). Olauncher explicitly has no widgets — this is by design.
- Remind the user this is reversible: they can switch back to their old launcher at any time.

## Sources

1. www.theguardian.com/science/2022/jan/02/attention-span-focus-screens-apps-smartphones-social-media — The Guardian: Johann Hari — "Your attention didn't collapse. It was stolen" — Documents how tech companies engineer attention capture.

## Guides

1. olauncher.app — Olauncher — official website — Text-only launcher for Android, recommended starting point
2. f-droid.org/packages/fr.neamar.kiss — KISS Launcher — F-Droid page — Search-focused, 250KB, zero internet
3. github.com/rama-io/mako — Mako — GitHub — Privacy-first, two permissions, GrapheneOS-verified
4. github.com/8tp/still-launcher — Still Launcher — GitHub — Strictest option, no internet permission, monochrome text-only
5. f-droid.org/en/categories/launcher/ — F-Droid: launcher category — FOSS Android launchers with verified no-tracker builds
6. reysu.io/dumbphone — reysu.io: convert iPhone to dumb phone — Full guide for iOS: Focus Modes, Screen Time, grayscale, widget tricks

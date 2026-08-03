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
---

## Context for the Agent

This card helps the user reclaim their attention by installing app and website blockers that break addictive engagement patterns. Use it when the user wants to stop compulsive checking, doomscrolling, or social media addiction.

## Why This Matters

Your phone's interface is engineered to keep you hooked. Researchers identified 63 engagement-maximizing patterns across the 17 largest online platforms, with social media apps using twice as many as any other category [1]. Johann Hari, in *Stolen Focus*, argues that our attention did not collapse — it was stolen by companies whose revenue depends on every second you spend scrolling [2]. App blockers and screen-time tools fight back by inserting friction — delays, schedules, grayscale, and hard limits — between you and the patterns designed to exploit your attention. You do not need to quit your phone. You need to change the defaults.

## Coaching Flow

### Step 1: Assess the User's Platforms and Pain Points
Ask the user: "Which apps or websites eat the most of your attention?" Common answers: Instagram, TikTok, YouTube, Twitter/X, Reddit, news sites, games. Also ask which device they use most — Android, iOS, desktop, or all three. Based on their answer, recommend the right tool(s) below.

### Step 2: Install App Blockers (Android)
Guide the user to install **Curbox** from F-Droid. Explain that it has no internet permission — it physically cannot transmit data. Walk them through blocking apps completely or using granular UI hiding (e.g., hide YouTube's home feed but keep search, hide Instagram explore but keep DMs). Highlight the short-form content blocker that specifically targets Instagram Reels and YouTube Shorts. If they want schedule-based blocking, show them how to set time windows.

### Step 3: Install Website Blockers (Desktop)
Recommend **LeechBlock NG** for Firefox/Chrome. Walk them through adding distracting sites (reddit.com, twitter.com, news sites) to a block list. Show them how to set time-based schedules (e.g., blocked during work hours, open in the evening) and delay-based access (e.g., 30-second delay before the page loads — enough to break the habit loop). LeechBlock is FOSS (GPL-3.0) and has no telemetry.

### Step 4: Install Screen Time Tools (iOS / Cross-Platform)
For iOS users: recommend **ScreenZen** (free, donation-supported). Guide them to set up delay-based access — a 10-second pause before Instagram opens, or a limit of 5 opens per day. For any user who wants a simple friction layer, ScreenZen works on Android and desktop too.

### Step 5: Set Up the Dumbphone Experience (Optional)
If the user wants to go further, guide them to **Reysu's dumbphone setup guide** for iPhone. This walks through converting a smartphone into a minimalist communication device — removing apps, grayscale mode, limiting notifications, and removing the browser.

## Decision Points

Ask the user: "Do you want friction (delays, grayscale) or hard blocks (scheduled, cannot bypass)?" Friction is gentler and works for habit change. Hard blocks are better for "I cannot stop myself" scenarios. Also ask: "Do you want these on your phone, your desktop, or both?" — Curbox is Android-only, LeechBlock is desktop-only, ScreenZen is cross-platform.

## Pitfalls

- Curbox has no internet permission — this is a privacy feature, but it means the app cannot sync settings across devices or verify license keys. Everything is local.
- Hard-blocking an app you genuinely need (like your banking app or email) can cause real problems. Coach the user to block only the addictive parts, not the entire app.
- The user may try to bypass blockers (uninstall the blocker, disable it). This is normal — the goal is to make bypassing more effort than the craving is worth. If they keep bypassing, suggest a delay-based approach (Curbox's timed access) instead of hard blocks.
- Grayscale mode (iOS/Android accessibility setting) reduces the dopamine hit from colorful app icons. Suggest it as a complementary approach.

## Sources

1. Researchers identified 63 engagement-maximizing design patterns across the 17 largest online platforms — social media apps use twice as many as any other category (referenced in the Center for Humane Technology and related research)
2. Johann Hari, "Stolen Focus: Why You Can't Pay Attention" — comprehensive analysis of how the attention economy deliberately fractures focus through design patterns optimized for engagement over wellbeing

## Guides

1. github.com/curbox-app/curbox-android — Curbox: open-source app blocker for Android
2. github.com/proginosko/LeechBlockNG — LeechBlock NG: open-source website blocker for Firefox/Chrome
3. screenzen.co — ScreenZen: free, donation-supported screen time app for iOS/Android/desktop
4. reysu.io/dumbphone — Reysu: full dumbphone setup guide for iPhone
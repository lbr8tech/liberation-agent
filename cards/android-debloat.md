---
type: "lbr8 Protocol Card"
title: "Android Debloat & Telemetry Reduction"
description: "Remove carrier bloatware, OEM telemetry, and pre-installed junk from any Android phone without root using UAD-ng or Canta."
tags:
  - "phase-1"
  - "devices"
  - "intermediate"
  - "p1"
  - "big-tech-surveillance"
  - "tracking"
  - "ad-targeting"
related:
  - "cards/windows-debloat.md"
  - "cards/permissions-audit.md"
  - "cards/phone-degoogling.md"
  - "cards/dns-blocking.md"
---

## Context for the Agent

This card is about removing pre-installed bloatware and OEM telemetry from Android phones. Use it when the user has completed the basic permissions audit and wants to go deeper — removing system-level apps that can't be uninstalled normally.

## Why This Matters

Android phones phone home from the moment you turn them on. A Trinity College Dublin study found that Samsung, Xiaomi, Huawei, and Realme all transmit device identifiers, app lists, and usage telemetry to their servers — even when you opt out of analytics and the phone is idle [1]. Xiaomi logs every app window you open and how long you look at it, sending the data with hardware identifiers that survive factory reset. Pre-installed Facebook, Microsoft, and LinkedIn apps phone home without ever being opened [2]. None of this is opt-outable. Google's own Play Store restrictions on data collection don't apply to system apps — the ones OEMs pre-install. Debloating removes the apps that run this surveillance. For full telemetry elimination, see the Phone OS Liberation card.

## Coaching Flow

### Step 1: Choose a tool
Tell the user there are two main tools, and the choice depends on whether they have a computer available:

**UAD-ng (Universal Android Debloater Next Generation)** — desktop tool, no Shizuku needed. Best for a thorough debloat.
- Requirements: A computer (Windows/macOS/Linux), USB cable, USB debugging enabled on the phone
- Free, open source, written in Rust

**Canta** — on-device tool, uses Shizuku. Best for quick debloats without a computer.
- Requirements: Android 11+, no computer needed
- Uses Shizuku for ADB-level permissions without root

### Step 2: Prepare the device
Guide the user to enable Developer Options and USB Debugging:
- Go to Settings → About Phone → tap "Build Number" 7 times until "You are now a developer!" appears
- Go to Settings → System → Developer Options → enable "USB Debugging"
- If using Canta: also enable "Wireless Debugging" (Android 11+)

### Step 3A: Debloat with UAD-ng (desktop method)
Guide the user through:
1. Download UAD-ng from github.com/Universal-Debloater-Alliance/universal-android-debloater-next-generation
2. Launch the app, connect the phone via USB
3. Accept the USB debugging prompt on the phone (check "Always allow from this computer")
4. UAD-ng auto-detects the device and matches packages against its curated database
5. Every package is categorized: **Recommended** (safe to remove), **Advanced** (minor impact), **Expert** (significant impact), **Unsafe** (can bootloop)
6. Start with **Recommended** only. Never select packages the user doesn't understand.
7. Select packages, click Uninstall
8. Export the selection list — removed packages will return after OTA updates

### Step 3B: Debloat with Canta (on-device method)
Guide the user through:
1. Install Shizuku from F-Droid (f-droid.org)
2. Install Canta from F-Droid
3. Start Shizuku via Wireless Debugging (pair once, then Shizuku maintains the connection)
4. Open Canta — it uses UAD-ng's same package database with safety classifications
5. Browse packages, remove bloatware
6. Caveat: Shizuku can break after OEM updates. If it stops working, switch to UAD-ng from a computer.

### Step 4: What to remove
Guide the user through the categories:

**Safe to remove (Recommended tier):**
- **Carrier bloat**: T-Mobile/Verizon/AT&T apps, carrier billing, carrier tech support, carrier-branded apps
- **OEM duplicates**: The OEM's browser, calendar, notes, app store, voice assistant — anything the user has a better alternative for
- **Facebook pre-install**: com.facebook.appmanager, com.facebook.system, com.facebook.services — these run in the background even if you never open Facebook
- **Google duplicates**: Google Play Movies, Google News, Google Podcasts, Google TV, Google Play Books
- **Microsoft pre-installs**: LinkedIn, OneDrive, Microsoft Office — if unused
- **Telemetry and analytics packages**: Search UAD-ng's list for the specific OEM's telemetry services

**What NOT to remove:**
- com.android.phone, com.android.settings, com.android.systemui — core system components
- IMS packages (com.android.ims) — phone calls will break
- The user's keyboard if no alternative is installed

### Step 5: Post-debloat
Tell the user:
- The removed apps are fully dormant — they're not deleted from the system partition, just uninstalled for the current user
- Removed apps can be reinstalled from the Play Store if needed
- This is fully reversible from within UAD-ng or Canta
- **After OTA updates**: Removed packages typically return. Re-run UAD-ng and re-apply from the exported list. This is normal — debloating is not permanent without root.

## Decision Points

Ask the user: **"Do you have a computer you can use for this, or do you need to do it entirely from your phone?"** If they have a computer, recommend UAD-ng (more thorough, better categorized). If they only have the phone, recommend Canta via Shizuku.

Also ask: **"What OEM is your phone?"** (Samsung, Xiaomi, Google Pixel, OnePlus, etc.) Different OEMs have different bloatware profiles. If they have a Pixel, there's much less to remove. If they have a Samsung or Xiaomi, there's a lot.

## Pitfalls

- **Debloating does not free system partition storage** — The apps are dormant, not deleted. They still occupy space on the system partition. For permanent removal, the phone needs to be rooted or flashed with a custom ROM.
- **OTA updates restore removed packages** — This is the most common complaint. After every major update, the user needs to re-run the debloat tool. Export the selection list to make this quick.
- **Shizuku breaks after OEM updates** — Some OEMs break Shizuku's ADB connection after updates. Have UAD-ng as a backup if this happens.
- **"I removed something and now my phone doesn't work"** — This is why the safety tiers exist. If the user removes something in the "Expert" or "Unsafe" category, they risk bootloops or broken functionality. Stick to "Recommended" unless they know exactly what they're doing.
- **Debloating ≠ degoogling** — Debloating removes apps that phone home. It does not remove Google Play Services or replace the Android OS. For full telemetry elimination, see the "Phone OS Liberation" card.
- **Carrier-specific issues** — Some carriers (Verizon, AT&T) have apps that are tied to VoLTE or WiFi calling. Removing them can break calls. If unsure, leave carrier-specific packages alone.

## Sources

1. journals.plos.org/plosone/article?id=10.1371/journal.pone.0279942 (PLOS One / Trinity College Dublin: On the data privacy practices of Android OEMs — Samsung, Xiaomi, Huawei, and Realme transmit device identifiers, app lists, and usage telemetry with no opt-out)
2. scss.tcd.ie/doug.leith/Android_privacy_report.pdf (Trinity College Dublin: Android Mobile OS Snooping — pre-installed Facebook, Microsoft, LinkedIn apps phone home without being opened)
3. malwarebytes.com/blog/news/2025/02/android-happy-to-check-your-nudes-before-you-forward-them (Malwarebytes: Android System SafetyCore — Google silently installed image scanning in E2EE messages)

## Guides

1. github.com/Universal-Debloater-Alliance/universal-android-debloater-next-generation (UAD-ng: Universal Android Debloater)
2. github.com/samolego/Canta (Canta: on-device debloater via Shizuku)
3. github.com/RikkaApps/Shizuku (Shizuku: ADB-level permissions without root)
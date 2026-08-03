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

## Why

Android phones phone home from the moment you turn them on. A Trinity College Dublin study found that Samsung, Xiaomi, Huawei, and Realme all transmit device identifiers, app lists, and usage telemetry to their servers — even when you opt out of analytics and the phone is idle. Xiaomi logs every app window you open and how long you look at it, sending the data with hardware identifiers that survive factory reset. Pre-installed Facebook, Microsoft, and LinkedIn apps phone home without ever being opened. None of this is opt-outable. Google's own Play Store restrictions on data collection don't apply to system apps — the ones OEMs pre-install. Debloating removes the apps that run this surveillance. For full telemetry elimination, see the Phone OS Liberation card.

## Steps

### Android

Two tools, pick based on whether you have a computer:

<strong>UAD-ng (Universal Android Debloater Next Generation)</strong> — desktop tool, no Shizuku needed:
1. Enable USB debugging: Settings → Developer Options → USB Debugging. (Enable Developer Options by tapping Build Number 7 times in Settings → About Phone)
2. Download UAD-ng from github.com/Universal-Debloater-Alliance/universal-android-debloater-next-generation (Windows/macOS/Linux, free, open source, Rust)
3. Connect phone via USB, launch UAD-ng — it auto-detects your device and matches packages against its curated database
4. Every package is categorized: Recommended (safe to remove), Advanced (minor impact), Expert (significant impact), Unsafe (can bootloop). Start with Recommended only
5. Select packages, click Uninstall. UAD-ng runs adb shell pm uninstall --user 0 under the hood — removes the app for your user but does not touch the system partition. Fully reversible from within UAD-ng or by reinstalling from Play Store
6. Export your selection list after debloating — you will need to re-apply after OTA updates, which restore removed packages

<strong>Canta</strong> — on-device, uses Shizuku:
1. Install Shizuku (F-Droid) and start it via Wireless Debugging (Android 11+). Pair once, then Shizuku maintains the connection
2. Install Canta (F-Droid) — uses UAD-ng's same package database with safety classifications
3. Browse packages, remove bloatware directly from your phone
4. Caveat: Shizuku can break after OEM updates. If Shizuku stops working, switch to UAD-ng from a computer

<strong>What to remove (any OEM):</strong>
- Carrier bloat (T-Mobile/Verizon/AT&T apps, carrier billing, carrier tech support)
- OEM duplicates (browser, calendar, notes, app store, voice assistant — anything you have a better alternative for)
- Facebook pre-install (com.facebook.appmanager, com.facebook.system, com.facebook.services — these run in the background even if you never open Facebook)
- Google duplicates (Google Play Movies, Google News, Google Podcasts)
- Microsoft pre-installs (LinkedIn, OneDrive if unused)
- Telemetry and analytics packages (search UAD-ng's list for your OEM's telemetry services)

<strong>What NOT to remove:</strong>
- com.android.phone, com.android.settings, com.android.systemui — core system
- IMS packages (com.android.ims) — phone calls break
- Your keyboard if no alternative is installed

After OTA updates: removed packages typically return. Re-run UAD-ng and re-apply from your exported list. This is normal — debloating is not permanent without root.

<strong>Honest limitations:</strong> Debloating stops apps from running and phoning home, but it does not free system partition storage (apps are dormant, not deleted). For permanent removal and full telemetry elimination, see the Phone OS Liberation card.

## Sources

1. journals.plos.org/plosone/article?id=10.1371/journal.pone.0279942 (PLOS One / Trinity College Dublin: On the data privacy practices of Android OEMs — Samsung, Xiaomi, Huawei, and Realme transmit device identifiers, app lists, and usage telemetry with no opt-out)
2. scss.tcd.ie/doug.leith/Android_privacy_report.pdf (Trinity College Dublin: Android Mobile OS Snooping — pre-installed Facebook, Microsoft, LinkedIn apps phone home without being opened)
3. malwarebytes.com/blog/news/2025/02/android-happy-to-check-your-nudes-before-you-forward-them (Malwarebytes: Android System SafetyCore — Google silently installed image scanning in E2EE messages)

## Guides

1. github.com/Universal-Debloater-Alliance/universal-android-debloater-next-generation (UAD-ng: Universal Android Debloater)
2. github.com/samolego/Canta (Canta: on-device debloater via Shizuku)
3. github.com/RikkaApps/Shizuku (Shizuku: ADB-level permissions without root)

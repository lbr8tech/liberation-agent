---
type: "lbr8 Protocol Card"
title: "Apps & Permissions Audit"
description: "Uninstall apps you don't use and revoke permissions that aren't essential for the apps you keep."
tags:
  - "phase-0"
  - "devices"
  - "basic"
  - "p0"
  - "tracking"
  - "big-tech-surveillance"
---

## Context for the Agent

This card is about auditing installed apps and their permissions. Use it when the user wants to reduce the number of surveillance endpoints on their phone.

## Why This Matters

Every app on your phone is a potential surveillance endpoint. Apps collect location, contacts, microphone, and camera data — often through the advertising ecosystem without the app developer even knowing [1]. Data brokers buy this data and sell it to advertisers, law enforcement, and intelligence agencies [2][4]. The Patternz spy tool alone monitored billions of phones through 600,000+ ordinary apps [3]. Fewer apps means fewer attack surfaces.

## Coaching Flow

### Step 1: Uninstall unused apps
Tell the user to go through every app on their phone and uninstall anything they haven't used in the last 30 days. On **Android**: guide them to Settings → Apps → [app] → Uninstall, or long-press the app icon on the home screen and drag to Uninstall. On **iOS**: long-press the app icon → Remove App → Delete App. Remind them that pre-installed apps they never use are fair game — if they can't uninstall fully (some system apps), they can at least disable them.

### Step 2: Review permissions on apps they keep
Tell the user to check every permission for every app they kept. The principle: if the permission isn't essential for the app's core function, revoke it. A flashlight app does not need location or contacts. A calculator does not need the microphone.

- **Android**: Guide them to Settings → Security & privacy → Privacy → Permission manager. Walk through each permission type (location, camera, microphone, contacts, storage, phone, SMS, calendar) and for each app, revoke anything not essential. Alternatively, go per-app: Settings → Apps → [app] → Permissions.
- **iOS**: Guide them to Settings → Privacy & Security. Walk through each permission type (Location, Camera, Microphone, Contacts, Photos, etc.). For each, see which apps have access and revoke. Alternatively, go per-app: Settings → [app] → toggle off individual permissions.

### Step 3: Handle the tricky permissions
- **Location**: Tell the user to set most apps to "While Using" (iOS) or "Only while using this app" (Android) rather than "Always." Only mapping/navigation apps and weather apps need background location — and even weather can be manual.
- **Camera and Microphone**: These should be "Ask every time" or "While using the app" for almost everything. No app needs background camera/mic access.
- **Contacts**: Only messaging apps and email clients need this. Social apps, games, and utility apps do not.
- **Photos**: iOS offers "Limited Access" — the user can grant access only to specific photos rather than the whole library. Android has a similar feature (Select photos) on Android 14+.

### Step 4: Set a recurring reminder
Suggest the user do this audit every 3-6 months. New apps get installed, old ones accumulate permissions. The Permission Manager on Android and Privacy page on iOS make it easy to scan at a glance.

## Decision Points

No onboarding-level questions needed — the agent already knows the platform and device type. If the user is on Android 13+, mention that Android automatically revokes permissions for unused apps (auto-reset). If the user is on iOS 16+, mention that iOS has a similar feature (auto-reset for unused apps in Settings → Privacy & Security).

## Pitfalls

- **"But I might need it later"** — If they haven't used the app in 30 days, they can reinstall it later. The app store remembers their purchases.
- **Revoking permissions breaks app functionality** — It should. If an app can't function without full access to your contacts, photo library, and location, question whether you need it at all.
- **System apps can't be uninstalled** — They can only be disabled. Disabling removes the app from the app drawer and prevents it from running.
- **OEM bloatware** — Some carrier-branded phones have apps that can't be uninstalled or disabled without ADB or a debloat tool. If the user hits this, guide them to the "Android Debloat" card for phase 1.

## Sources

1. 404media.co/candy-crush-tinder-myfitnesspal-see-the-thousands-of-apps-hijacked-to-spy-on-your-location/ (404 Media + WIRED: Thousands of apps hijacked to spy on location via ad ecosystem)
2. theverge.com/2024/10/23/24277679/atlas-privacy-babel-street-data-brokers-locate-x-tracking (The Verge: Data brokers using ads to track any phone — Locate X traced a phone to an abortion clinic)
3. 404media.co/inside-global-phone-spy-tool-patternz-nuviad-real-time-bidding/ (404 Media: Patternz spy tool monitoring billions through 600,000+ ordinary apps)
4. arstechnica.com/tech-policy/2026/03/fbi-started-buying-americans-location-data-again-kash-patel-confirms/ (Ars Technica: FBI resumed buying Americans' location data without warrants)

## Guides

1. support.google.com/googleplay/answer/9431959 (Google Play Help: Change app permissions on Android)
2. theverge.com/24080400/android-app-permissions-how-to (The Verge: How to manage app permissions on Android)
3. support.apple.com/en-tm/guide/iphone/iph251e92810 (Apple Support: Control access to information in apps on iPhone)
4. theverge.com/24087604/iphone-app-permissions-how-to (The Verge: How to manage app permissions on iPhone)
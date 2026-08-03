---
type: "lbr8 Protocol Card"
title: "App Isolation with Work Profiles"
description: "Compartmentalize apps into isolated Android profiles to prevent cross-app tracking and data leakage."
tags:
  - "phase-1"
  - "devices"
  - "intermediate"
  - "p1"
  - "tracking"
  - "big-tech-surveillance"
  - "digital-minimalism"
related:
  - "cards/screen-time-app-blockers.md"
  - "cards/permissions-audit.md"
  - "cards/phone-degoogling.md"
---

## Context for the Agent

This card is for Android users who want to prevent apps from cross-referencing data and tracking them across services. Use it when the user has social media, Google, or employer apps they don't fully trust sharing data with the rest of their phone.

## Why This Matters

Android apps can see each other. Meta and Yandex have been caught abusing local network ports to silently link your web browsing to your Facebook, Instagram, and Yandex app identities — bypassing Android's sandbox entirely [1]. A consumer investigation across just 20 apps found 117 third-party tracking companies and 882 permissions requested [2]. Profiling happens across apps, not within a single one. App isolation puts untrusted apps into a separate profile with its own file system, permissions, and encryption keys — apps in one profile cannot read data from another.

## Coaching Flow

### Step 1: Check the user's Android version
The user's device is known from onboarding. If they're on **Android 15+**, guide them to use the built-in **Private Space** feature. If they're on **Android 14 or earlier**, guide them to use **Shelter** from F-Droid.

### Step 2: Set up Private Space (Android 15+)
Walk the user through:
1. Settings → Security & Privacy → Private Space
2. Follow the on-screen setup (this creates a completely isolated profile)
3. Install the apps they want to isolate in Private Space
4. Show them how to lock the space with a single tap — this hides all apps and stops all background activity
5. If they use a Google Account, recommend using a separate Google Account inside Private Space for maximum separation

### Step 3: Set up Shelter (Android 14 or earlier)
Walk the user through:
1. Install Shelter from F-Droid [4]
2. Open Shelter — it will prompt to create a work profile
3. Once created, select apps to move into the work profile (social media, Google apps, employer apps, any app you don't fully trust)
4. Show them how to disable the work profile when not in use — this freezes all apps in it, killing background activity and notifications

### Step 4: Decide which apps to isolate
Guide the user on what to put in the isolated profile:
- **Social media:** Facebook, Instagram, TikTok, Twitter/X, Snapchat, WhatsApp
- **Google services:** Google Play Services, Google Maps, Google Photos
- **Employer apps:** Microsoft Teams, Slack, Outlook (work account)
- **Any app with aggressive tracking:** Shopping apps, news apps with many ad SDKs

### Step 5: For GrapheneOS users, explain Storage Scopes
If the user is on GrapheneOS, explain that they can use Storage Scopes and Contact Scopes per-profile for even finer-grained control [5]. Each profile has separate encryption keys.

## Decision Points

Ask the user: **Which apps do you most want to isolate?** Guide them to think about (a) apps with the most tracking SDKs (social media), (b) employer apps that shouldn't see personal data, and (c) apps they use infrequently but don't want to delete.

## Pitfalls

- Warn that switching profiles requires authentication — this is a feature, not a bug, but the user should know about the friction.
- Warn that some apps (especially banking or authenticator apps) may not work properly in a work profile — test before committing.
- Warn that disabling the work profile also stops notifications from those apps, which is usually desired but should be intentional.
- Remind the user that apps in the main profile can still see each other — isolation only protects across the profile boundary.

## Sources

1. arstechnica.com/security/2025/06/meta-and-yandex-are-de-anonymizing-android-users-web-browsing-identifiers/ — Ars Technica: Meta and Yandex de-anonymizing Android users — Tracking code abuses local network ports to link web browsing to app identities, bypassing Android sandboxing
2. which.co.uk/news/article/how-much-do-apps-know-about-you-5-ways-to-improve-app-privacy-aJ4p38G3oS1x — Which?: App privacy investigation — 20 apps, 117 tracking companies, 882 permissions, 78 "risky" permissions

## Guides

1. ssd.eff.org/module/b5b05223-6609-4aac-b8c4-4dec2c0ea175 — EFF Surveillance Self-Defense: Android privacy and security settings — Comprehensive Android privacy guide
2. privacyguides.org/en/android/general-apps/ — PrivacyGuides: Android general apps — Shelter and Private Space recommendations
3. source.android.com/docs/security/features/private-space — Android Open Source Project: Private Space technical documentation
4. f-droid.org/packages/net.typeblog.shelter/ — Shelter — F-Droid page — FOSS work profile manager
5. grapheneos.org/features — GrapheneOS: features overview — User profiles, separate encryption keys, Storage Scopes, Contact Scopes
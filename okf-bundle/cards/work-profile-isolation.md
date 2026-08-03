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

## Why

Android apps can see each other. Meta and Yandex have been caught abusing local network ports to silently link your web browsing to your Facebook, Instagram, and Yandex app identities — bypassing Android's sandbox entirely (Ars Technica, 2025). A consumer investigation across just 20 apps found 117 third-party tracking companies and 882 permissions requested (Which?, 2024). Profiling happens across apps, not within a single one.

App isolation puts apps you don't fully trust — social media, Google services, employer apps — into a separate, sandboxed profile with its own file system, permissions, and encryption keys. Apps in one profile cannot read data from another. You can freeze the entire profile when not in use, killing all background activity and notifications.

## Steps

### General

**Android 15+: Use Private Space (built-in)**
Go to Settings → Security & Privacy → Private Space. This is a native OS feature — no third-party app needed. Apps installed in Private Space are completely isolated from your main profile. You can lock the space with a single tap, hiding all apps and stopping all background activity. Use a separate Google Account for maximum separation.

**Android <15: Use Shelter (F-Droid)**
Shelter creates an isolated work profile using Android's built-in work profile feature. Move social media, Google apps, and any app you want compartmentalized into the work profile. Disable the work profile when you don't want distractions — all apps in it go silent, produce no notifications, and consume no battery. Also useful on degoogled phones: put apps that need Google services in the work profile to isolate them.

**GrapheneOS: Use secondary user profiles for maximum isolation**
Each user profile is a fully separate Android environment with its own apps, files, settings, and encryption keys. You can end a profile's session to put its data at rest — removing encryption keys from memory. GrapheneOS recommends Private Space as the most convenient option, but secondary users provide the strongest separation.

### iOS

No equivalent. iOS does not support work profiles or isolated app spaces outside of MDM (enterprise). Use Focus Modes + Screen Time as the closest alternative (see screen-time-app-blockers card).

## Going Further

**Private Space apps bypass VPN**
A major gotcha: apps in Private Space do not automatically use your main profile's VPN. You must install and configure a VPN separately inside the Private Space, or your isolated apps will connect with your real IP. The same applies to work profiles and secondary user profiles — each has independent VPN configuration.

**Private Space apps can't run in background when locked**
When Private Space is locked, apps inside it are completely stopped. They cannot show notifications, track health data, or perform any background tasks. Do not put apps that need background activity (medical monitoring, alarm systems) in Private Space.

**Shelter is in maintenance mode**
Shelter's developer states the app is in "effective maintenance mode" — it will continue to receive Android compatibility updates, but no new features are planned. If you're on Android 15+, Private Space is the forward-looking choice.

**On GrapheneOS: keep the owner profile empty**
Many GrapheneOS users keep their owner profile nearly empty and use a secondary user profile as their daily driver. This way, if a profile needs to be deleted for any reason, it can be done without a factory reset. The owner profile can also control which apps are pushed to other profiles.

## Sources

1. arstechnica.com/security/2025/06/meta-and-yandex-are-de-anonymizing-android-users-web-browsing-identifiers/ (Ars Technica: Meta and Yandex de-anonymizing Android users — tracking code abuses local network ports to link web browsing to app identities, bypassing Android sandboxing)
2. which.co.uk/news/article/how-much-do-apps-know-about-you-5-ways-to-improve-app-privacy-aJ4p38G3oS1x (Which?: App privacy investigation — 20 apps, 117 tracking companies, 882 permissions, 78 "risky" permissions)

## Guides

1. ssd.eff.org/module/b5b05223-6609-4aac-b8c4-4dec2c0ea175 (EFF Surveillance Self-Defense: Android privacy and security settings guide)
2. privacyguides.org/en/android/general-apps/ (PrivacyGuides: Android general apps — Shelter and Private Space recommendations)
3. source.android.com/docs/security/features/private-space (Android Open Source Project: Private Space technical documentation)
4. f-droid.org/packages/net.typeblog.shelter/ (Shelter — F-Droid page: FOSS work profile manager)
5. grapheneos.org/features (GrapheneOS: features overview — user profiles, separate encryption keys, Storage Scopes, Contact Scopes)

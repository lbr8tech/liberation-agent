---
type: "lbr8 Protocol Card"
title: "Private & Open Source App Store"
description: "Install F-Droid for tracker-free open-source apps, Aurora Store for Play Store apps without a Google account, and Obtainium for direct-from-source downloads."
tags:
  - "phase-1"
  - "devices"
  - "basic"
  - "p1"
  - "big-tech-surveillance"
  - "tracking"
related:
  - "cards/android-debloat.md"
  - "cards/phone-degoogling.md"
  - "cards/dns-blocking.md"
---

## Why

The Google Play Store is not just an app store — it is a surveillance tool. A Trinity College Dublin study found that Google silently stores advertising cookies, tracking cookies, and device identifiers on your handset through the Play Store and Play Services, even after a factory reset and even when no Google apps have been opened. No consent is sought. There is no opt-out. Every search you make, every app you view, every download is tagged with your Google account ID and sent to Google servers. F-Droid breaks this model: no account needed, no tracking, apps built from source, tracker-free. For apps you need from the Play Store, Aurora Store downloads them using an anonymous account so Google never knows it is you.

## Steps

### Android

<strong>F-Droid</strong> — the FOSS app repository:
1. Download the F-Droid client APK from f-droid.org (not available in Play Store). Enable "Install unknown apps" for your browser in Settings when prompted
2. No account needed. Browse, install, and update apps — F-Droid tracks nothing
3. Apps are built from source, checked for security issues, and flagged with anti-features (ads, tracking, non-free dependencies)
4. Add the IzzyOnDroid repo (Settings → Repositories → add apt.izzysoft.de/fdroid/repo) for a wider selection of FOSS apps
5. ~4,000 apps available — smaller than Play Store, but every app is free, open source, and tracker-free

<strong>Aurora Store</strong> — Play Store apps without a Google account:
1. Install from F-Droid. GPLv3, open source
2. Log in with an anonymous account (default) — Aurora's token dispenser provides a dummy Google account, so nothing is linked to your identity
3. Download, update, and search Play Store apps normally. Device and locale spoofing available for geo-locked apps
4. Exodus Privacy integration shows trackers in each app before you install
5. Caveat: your installed app list and search queries still reach Google's servers (this is inherent to the Play Store API), but they are not linked to your personal account. Use the blacklist feature to avoid sending package info for sensitive apps
6. Cannot download paid apps anonymously — purchase on the Play Store website, then log in with your own (throwaway) account in Aurora

<strong>Obtainium</strong> — install apps directly from GitHub/GitLab releases:
1. Install from F-Droid
2. Add any GitHub or GitLab release URL — Obtainium tracks new releases and installs APKs directly from source
3. No intermediary, no store, no account. Just the developer and you

<strong>iOS:</strong> No equivalent. The App Store is the only option. Apple's walled garden prevents alternative app stores entirely.

## Sources

1. scss.tcd.ie/Doug.Leith/pubs/cookies_identifiers_and_other_data.pdf (Trinity College Dublin: Cookies, Identifiers and Other Data That Google Silently Stores on Android Handsets — advertising cookies, tracking cookies, and device identifiers stored with no consent and no opt-out)
2. forbes.com/sites/zakdoffman/2025/03/04/forget-chrome-google-apps-start-tracking-your-phone-no-opt-out/ (Forbes: Google Apps Track Android Phones By Default — coverage of Trinity College study)

## Guides

1. f-droid.org/en/about/ (F-Droid: About — how the FOSS app ecosystem works)
2. howtogeek.com/790674/what-is-f-droid-and-how-is-it-different-from-the-play-store/ (HowToGeek: What Is F-Droid and How Is It Different From the Play Store?)
3. auroraoss.gitbook.io/wiki/troubleshooting-and-faqs/faqs/aurora-store (Aurora Store: FAQ — anonymous logins, privacy features, limitations)
4. github.com/AuroraOSS/AuroraStore (Aurora Store: GitHub repository)

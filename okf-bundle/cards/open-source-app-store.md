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
---

## Context for the Agent

This card guides the user to replace the Google Play Store with privacy-respecting app sources. Use it when the user wants to stop Google tracking every app search and download.

## Why This Matters

The Google Play Store is not just an app store — it is a surveillance tool. A Trinity College Dublin study found that Google silently stores advertising cookies, tracking cookies, and device identifiers on your phone through Play Store and Play Services, even after a factory reset and even when no Google apps have been opened [1]. No consent is sought. No opt-out exists. Every search you make, every app you view, every download is tagged with your Google account ID. F-Droid breaks this model: no account, no tracking, apps built from source. For apps you need from the Play Store, Aurora Store downloads them using an anonymous account so Google never knows it is you [2].

## Coaching Flow

### Step 1: Install F-Droid (FOSS App Repository)
Tell the user: F-Droid is your primary app source going forward. Everything here is free, open source, and tracker-free. Guide them to download the APK from f-droid.org (not available in the Play Store). Walk them through enabling "Install unknown apps" for their browser if prompted. Emphasize: no account needed, no tracking, and every app is checked for security issues and anti-features (ads, tracking, non-free dependencies).

### Step 2: Add the IzzyOnDroid Repo
Tell the user: F-Droid's default catalog is around 4,000 apps — smaller than the Play Store, but every app is clean. To widen the selection, add the IzzyOnDroid repository. Walk them through: Settings → Repositories → Add → enter apt.izzysoft.de/fdroid/repo. Explain that this is a trusted community repository with a much larger selection of FOSS apps.

### Step 3: Install Aurora Store for Play Store Apps
Tell the user: For apps that aren't on F-Droid (banking apps, etc.), you need Aurora Store. Guide them to install it from F-Droid. Explain that Aurora Store lets them download Play Store apps using an anonymous session — Google never sees their real account. Walk through the initial setup: choose "Anonymous Login" (not "Google Login"), and the app connects to Play Store servers with a disposable session.

### Step 4: Install Obtainium for Direct-Source Downloads
Tell the user: For apps that update from GitHub/GitLab directly (like Signal, Bitwarden, or NewPipe), Obtainium automates update checking. Guide them to install from F-Droid. Walk them through adding their first app: tap the + button, paste the GitHub release URL, and Obtainium will track updates and notify them when a new version is available.

### Step 5: Migrate Apps
Help the user identify which of their current apps are available on F-Droid. Suggest they search for each app they use regularly. For apps not on F-Droid, use Aurora Store. For apps they download from GitHub releases, add them to Obtainium.

## Decision Points

Ask the user: "Do you have any apps you use daily that are only on the Play Store?" If yes, Aurora Store is essential. If they use very few Play Store apps, they may still want Aurora Store installed for the occasional one-off download. For users who are fully degoogling, Obtainium combined with F-Droid covers nearly everything.

## Pitfalls

- F-Droid updates are sometimes delayed behind official releases. The F-Droid team builds apps from source, which takes time. If the user needs the latest version of an app immediately, point them to Obtainium (direct GitHub releases) or Aurora Store.
- Some banking and government apps detect anonymous or custom stores and refuse to work. In that case, the user can keep the Play Store installed but disabled, using it only when absolutely necessary.
- Aurora Store anonymous sessions can occasionally be rate-limited by Google. If the user sees a CAPTCHA or "too many requests" error, wait a few hours and try again.
- Not all apps on F-Droid are secure — the anti-feature flags (ads, tracking, non-free) are there for a reason. Teach the user to check them before installing.

## Sources

1. scss.tcd.ie/Doug.Leith/pubs/cookies_identifiers_and_other_data.pdf — Trinity College Dublin: "Cookies, Identifiers and Other Data That Google Silently Stores on Android Handsets" — advertising cookies, tracking cookies, and device identifiers stored with no consent and no opt-out
2. forbes.com/sites/zakdoffman/2025/03/04/forget-chrome-google-apps-start-tracking-your-phone-no-opt-out/ — Forbes: "Google Apps Track Android Phones By Default" — coverage of the Trinity College study

## Guides

1. f-droid.org/en/about/ — F-Droid: About — how the FOSS app ecosystem works
2. howtogeek.com/790674/what-is-f-droid-and-how-is-it-different-from-the-play-store/ — HowToGeek: What Is F-Droid and How Is It Different From the Play Store?
3. auroraoss.gitbook.io/wiki/troubleshooting-and-faqs/faqs/aurora-store — Aurora Store: FAQ — anonymous logins, privacy features, limitations
4. github.com/AuroraOSS/AuroraStore — Aurora Store: GitHub repository
---
type: "lbr8 Protocol Card"
title: "Offline Maps & Navigation"
description: "Use OpenStreetMap-based apps like Organic Maps or OsmAnd for offline navigation without location tracking."
tags:
  - "phase-1"
  - "devices"
  - "basic"
  - "p1"
  - "tracking"
  - "big-tech-surveillance"
related:
  - "cards/privacy-browser.md"
  - "cards/search-engine.md"
  - "cards/phone-degoogling.md"
  - "cards/google-privacy-settings.md"
---

## Why

Google Maps is the most detailed location surveillance system ever built. On Android, it pings your location every 2–4 minutes as long as the phone is on — even when the app is closed. The Timeline feature builds a permanent diary of where you live, work, eat, and sleep, and Google feeds that data into its ad-targeting infrastructure to verify whether you visited a store after seeing an ad for it. Your real-world routine becomes a targeting profile.

Google has a documented history of deceptive location tracking. An AP investigation found that Google continued collecting location data even when users explicitly turned off Location History — through a separate, hidden setting called Web & App Activity. The company settled with 40 U.S. states for $391.5 million in 2022, the largest multi-state privacy settlement at the time. Google received over 11,000 geofence warrants from law enforcement by 2020, allowing police to sweep up location data on every phone near a crime scene. In June 2026, the Supreme Court ruled in Chatrie v. United States that geofence warrants are Fourth Amendment searches — but the practice is not banned, only requires a warrant.

Google moved Location History to device storage in July 2025, which largely closes the server-side geofence warrant loophole. But real-time location tracking during active navigation still feeds Google's ad infrastructure, and the data on your device is now the single point of failure — if your phone is seized, the Timeline data goes with it. The only way to stop Google from knowing where you are is to use a different app.

## Steps

### General

**Suggested protocol:** use Organic Maps as your default for daily navigation. It handles driving, cycling, and walking well. Download your country map once and navigation works fully offline — no data use, no roaming costs, works in tunnels. Update maps manually a few times a year via Settings → Maps.

**What you give up:** real-time traffic data (no OSM app has it), transit routing (use your local transit app alongside), and Street View. For specific trips where you need live traffic or a specific business listing, use Google Maps in a browser (not the app) without signing in — this prevents association with your account, though Google still collects device-level data. Sign out of the Google Maps app entirely if you keep it installed, and set location permission to "Only while using the app" (never "Always").

### Android

**Organic Maps** (F-Droid, Play Store) — the best replacement for most people. Free, open-source, built on OpenStreetMap data, updated biweekly. Turn-by-turn navigation for driving, cycling, and walking. Works fully offline after a one-time regional map download. No account, no tracking, no ads. 117 MB install. No map download limit.

**OsmAnd** (F-Droid as OsmAnd~, Play Store) — the power-user option. More features than Organic Maps: topographic contour lines, offline Wikipedia integration, color-coded hiking/biking trails, configurable map layers, vehicle profiles (RV, truck, bus). Steeper learning curve, cluttered interface. Free F-Droid version (OsmAnd~) removes the 7-map download cap. 5,692★ on GitHub.

**CoMaps** (comaps.app) — community fork of Organic Maps launched May 2025 after a governance crisis (Organic Maps shareholders refused to move to nonprofit structure). Same codebase, same privacy, community-governed. Worth watching if Organic Maps' governance concerns you.

### iOS

**Organic Maps** (App Store) — same as Android, fully featured. **OsmAnd** (App Store) — available but leans more subscription-ish on iOS. Test the free version first. **Apple Maps** is a fallback: collects fewer data types than Google, and Apple says search/navigation data isn't associated with your account. Apple announced in March 2026 that ads are coming to Apple Maps (US/Canada, summer 2026) — but they're contextual search ads based on relevance, not your location history, and Apple says personal data stays on-device. Still, it's no longer ad-free.

## Going Further

**Disable Google's location tracking back doors**
If you still use Google Maps occasionally, disable both Timeline AND Web & App Activity at myactivity.google.com. Turning off Timeline alone does not stop Google from collecting location data — Web & App Activity is a separate setting that logs your location through Google Search, Maps queries, and other interactions. Also disable Wi-Fi and Bluetooth scanning in Android Settings → Location (these track you even with GPS off). Set Google Maps location permission to "Only while using the app," never "Always." Delete your existing Timeline data in the app: profile icon → Your Timeline → three-dot menu → Delete all Timeline data.

**Use Google Maps in a browser for edge cases**
If you need live traffic or a specific business listing that OSM doesn't have, use Google Maps in a browser (not the app) without signing in. Browser-based Maps uses your browser's location permission rather than app-level controls, doesn't collect background location data, and doesn't update Timeline. Google still collects device-level data, but it can't be tied to your account identity. This is strictly better than the app's incognito mode, which only pauses account-level tracking while still collecting real-time location.

**Contribute to OpenStreetMap**
Organic Maps and OsmAnd both run on OpenStreetMap data — a volunteer-maintained, open-source map of the world. The quality of your local OSM data directly affects your navigation experience. Use the OSM editing tools (or the "Edit Map" option in Organic Maps) to add missing roads, fix business listings, or correct addresses. This is how the open mapping ecosystem improves without a corporation driving it. See openstreetmap.org to get started.

## Sources

1. apnews.com/article/828aefab64d4411bac257a07c1af0ecb (Associated Press: Google tracks your movements, like it or not — AP investigation found Google stored location data even with Location History off, via hidden Web & App Activity setting; led to $391.5M settlement with 40 states)
2. arstechnica.com/tech-policy/2026/06/supreme-court-ruling-guts-governments-use-of-geofence-warrants/ (Ars Technica: Supreme Court rules geofence warrants are Fourth Amendment searches — 6-3 decision in Chatrie v. United States, June 2026; Google received 11,000+ geofence warrants by 2020)
3. 404media.co/google-leak-reveals-thousands-of-privacy-incidents/ (404 Media: internal Google database obtained by 404 Media reveals thousands of employee-reported privacy incidents over six years — including leaked trip data, home addresses, and children's voice data)
4. npr.org/2026/04/27/nx-s1-5777656/supreme-court-geofence-warrants (NPR: Supreme Court weighs constitutionality of geofence warrants — Location History records location every 2 minutes, 500M users opted in, police used Google data to identify suspects near crime scenes)

## Guides

1. privacyguides.org/en/maps/ (PrivacyGuides: recommended maps and navigation apps — criteria: no PII collection, no account, no mandatory location sharing, offline support; recommends Organic Maps, OsmAnd, and HERE WeGo)
2. organicmaps.app (Organic Maps: free, open-source offline maps based on OpenStreetMap — 13,853★, turn-by-turn navigation, no account, no tracking)
3. osmand.net (OsmAnd: feature-rich offline maps and navigation — 5,692★, topographic layers, hiking/cycling routes, vehicle profiles, F-Droid version removes download cap)
4. comaps.app (CoMaps: community fork of Organic Maps — nonprofit, Codeberg-hosted, same codebase, launched May 2025 after Organic Maps governance crisis)
5. openstreetmap.org (OpenStreetMap: the volunteer-maintained open-source map of the world that powers Organic Maps, OsmAnd, and hundreds of other apps)
6. eylenburg.github.io/ai_search_maps.htm (Eylenburg: knowledge provider comparison — 39 AI, search, and map services with data source and privacy analysis)

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
---

## Context for the Agent

This card helps the user replace Google Maps with OpenStreetMap-based apps that work offline and do not track their location. Use it when the user wants to stop Google tracking every place they visit.

## Why This Matters

Google Maps is the most detailed location surveillance system ever built. On Android, it pings your location every 2-4 minutes as long as the phone is on — even when the app is closed [1]. An AP investigation found that Google continued collecting location data even when users explicitly turned off Location History — through a separate, hidden setting called Web & App Activity. Google settled with 40 U.S. states for $391.5 million in 2022, the largest multi-state privacy settlement at the time [1]. Google received over 11,000 geofence warrants from law enforcement by 2020, allowing police to sweep up location data on every phone near a crime scene [2]. In June 2026, the Supreme Court ruled in Chatrie v. United States that geofence warrants are Fourth Amendment searches — but the practice is not banned, only requires a warrant [2]. An internal Google database leaked to 404 Media revealed thousands of employee-reported privacy incidents over six years, including leaked trip data, home addresses, and children's locations [3].

## Coaching Flow

### Step 1: Choose the Right Maps App
Based on the user's needs, recommend one of these:

- **Organic Maps** (recommended for most users): Free, open source, offline maps based on OpenStreetMap. Turn-by-turn navigation, search, and points of interest. No account, no tracking, no ads. Lightweight (~30MB per region). Best for driving, walking, and basic navigation.
- **OsmAnd** (for power users): Feature-rich offline maps with topographic layers, hiking/cycling routes, and vehicle profiles (car, bike, pedestrian, public transport). The F-Droid version removes the download cap. More complex but more capable.
- **CoMaps** (community fork of Organic Maps): Nonprofit, Codeberg-hosted, same codebase as Organic Maps. Launched May 2025 after Organic Maps' governance crisis. If the user already uses Organic Maps, CoMaps is a drop-in replacement.

### Step 2: Install and Download Maps
Guide the user to install from F-Droid (or Aurora Store/App Store). Walk them through downloading offline maps for the regions they need:
1. Open the app
2. Go to Download Maps / Manage Maps
3. Select their country/region (or full continent for frequent travelers)
4. Download over Wi-Fi (maps are 50MB-500MB depending on region size)

### Step 3: Set Up Offline Navigation
Show the user how to:
1. Search for an address (works offline for downloaded regions)
2. Select a route (driving, cycling, walking)
3. Start turn-by-turn navigation (voice guidance is available offline)
4. Bookmark frequent locations (home, work, favorite places) — all stored locally, never sent to a server

### Step 4: Remove Google Maps or Restrict Its Permissions
If the user is ready to fully degoogle, guide them to uninstall Google Maps. If they need it occasionally (public transit schedules, real-time traffic), guide them to restrict its permissions: no location access in the background, only "While Using the App." Tell them to delete Google Maps Timeline history (maps.google.com/timeline).

## Decision Points

Ask the user: "Do you need real-time traffic, public transit schedules, or street-level imagery?" If yes, they may still need Google Maps for those specific features occasionally — but they can use it with restricted permissions. If they only need basic driving/walking navigation, Organic Maps is a complete replacement.

Ask the user: "Are you a hiker, cyclist, or off-road traveler?" If yes, recommend OsmAnd for its topographic layers, altitude profiles, and specialized routing.

## Pitfalls

- Offline maps do not include real-time traffic data. If the user relies on live traffic rerouting, they will need to use Google Maps or Waze for that specific purpose, or accept that offline navigation is blind to current conditions.
- OpenStreetMap data quality varies by region. In major cities, it is often as good as or better than Google Maps. In rural areas, it may be less detailed. The user can contribute to OpenStreetMap to improve it.
- Organic Maps is developed by a small team — updates are less frequent than Google Maps. Some features (public transit, indoor maps, Street View) are not available.
- Google Maps moved Timeline to device storage in July 2025, which closes the server-side geofence warrant loophole for Timeline data. But real-time location tracking during active navigation still feeds Google's ad infrastructure.
- The user should not confuse "offline maps" with "no tracking." Even if they use Google Maps offline, the app can still collect location data when permissions are granted.

## Sources

1. apnews.com/article/828aefab64d4411bac257a07c1af0ecb — Associated Press: Google tracks your movements, like it or not — AP investigation found Google stored location data even with Location History off, via hidden Web & App Activity setting; led to $391.5M settlement with 40 states
2. arstechnica.com/tech-policy/2026/06/supreme-court-ruling-guts-governments-use-of-geofence-warrants/ — Ars Technica: Supreme Court rules geofence warrants are Fourth Amendment searches — 6-3 decision in Chatrie v. United States, June 2026; Google received 11,000+ geofence warrants by 2020
3. 404media.co/google-leak-reveals-thousands-of-privacy-incidents/ — 404 Media: internal Google database obtained by 404 Media reveals thousands of employee-reported privacy incidents over six years — including leaked trip data, home addresses, and children's locations

## Guides

1. privacyguides.org/en/maps/ — PrivacyGuides: recommended maps and navigation apps — criteria: no PII collection, no account, no mandatory location sharing, offline support; recommends Organic Maps, OsmAnd, and HERE WeGo
2. organicmaps.app — Organic Maps: free, open-source offline maps based on OpenStreetMap — turn-by-turn navigation, no account, no tracking
3. osmand.net — OsmAnd: feature-rich offline maps and navigation — topographic layers, hiking/cycling routes, vehicle profiles
4. comaps.app — CoMaps: community fork of Organic Maps — nonprofit, Codeberg-hosted, same codebase, launched May 2025 after Organic Maps governance crisis
5. openstreetmap.org — OpenStreetMap: the volunteer-maintained open-source map of the world that powers Organic Maps, OsmAnd, and hundreds of other apps
6. eylenburg.github.io/ai_search_maps.htm — Eylenburg: knowledge provider comparison — 39 AI, search, and map services with data source and privacy analysis
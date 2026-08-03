---
type: "lbr8 Protocol Card"
title: "Private Video Client"
description: "Watch YouTube videos without ads, tracking, or an account using privacy-focused alternative clients."
tags:
  - "phase-1"
  - "media"
  - "basic"
  - "p1"
  - "tracking"
  - "ad-targeting"
  - "digital-minimalism"
---

## Context for the Agent

This card helps the user watch YouTube videos without ads, tracking, or an account, using privacy-focused alternative clients. Use it when the user wants to escape YouTube's recommendation algorithm and Google's tracking infrastructure.

## Why This Matters

YouTube's recommendation algorithm — optimized for watch time, because more watching means more ad revenue — drives 70% of all watch time on the platform. Zeynep Tufekci called it "one of the most powerful radicalizing instruments of the 21st century" [1]. A 2026 study found 27 of 33 members of a UK far-right group cited YouTube as their key radicalization pathway — autoplay pushed them from mainstream conservatism to neo-Nazi propaganda [2]. Max Fisher's *The Chaos Machine* traced the link between algorithmic amplification and real-world ethnic violence in Myanmar, Sri Lanka, and India [3]. The app itself is a tracking instrument: watch history, search history, location, device identifiers — all fed into Google's ad infrastructure. Even when signed out, Google collects device-level data. Privacy-focused clients break this entirely: no algorithm, no tracking, no ads, and no account needed.

## Coaching Flow

### Step 1: Choose the Right Client
Based on the user's platform and needs, recommend one:

- **NewPipe (Android, recommended):** FOSS YouTube client with no Google services. Features: background playback, audio-only mode, downloads, and support for PeerTube/SoundCloud/Bandcamp. No account needed, no ads, no tracking. Subscriptions and history are stored locally on the device.
- **FreeTube (desktop - Windows/macOS/Linux):** FOSS desktop YouTube client. Local subscriptions, history, and playlists. SponsorBlock support built in. Available on Flathub.
- **LibreTube (Android, advanced):** Routes through Piped instances for IP privacy. Material You UI. SponsorBlock built in. More privacy than NewPipe (your IP never reaches YouTube), but depends on public Piped instances being maintained.
- **Invidious (any platform, via browser):** Self-hostable web frontend for YouTube. Public instances available with Tor/I2P support. No JavaScript required. Video proxying optional. Works in any browser.

### Step 2: Install and Configure
Guide the user through installation:
1. **NewPipe:** Install from F-Droid. After opening, show them how to search for a channel, subscribe, and download a video. Explain that background playback works even with the screen off.
2. **FreeTube:** Install from flathub.org or the website. Show them how to import subscriptions from YouTube (export as OPML from Google Takeout, import into FreeTube).
3. **LibreTube:** Install from F-Droid. Show them how to select a Piped instance (direct them to piped.video or a community-maintained instance).
4. **Invidious:** Guide technical users through deploying via Docker, or point them to a public instance list at invidious.io.

### Step 3: Import Subscriptions (Optional)
If the user has existing YouTube subscriptions, guide them to:
1. Export subscriptions from YouTube via Google Takeout (takeout.google.com) — select only "Subscriptions" data
2. Import the OPML/CSV file into NewPipe or FreeTube
3. Explain that this is a one-time migration — going forward, subscriptions are managed locally

### Step 4: Set Up SponsorBlock (Optional)
Guide the user to enable SponsorBlock in NewPipe (settings → SponsorBlock) or FreeTube (settings → SponsorBlock). This automatically skips sponsored segments, intros, outros, and self-promotion in videos. It is community-sourced and open source.

### Step 5: Alternative: ReVanced (If They Need the Official App)
If the user insists on the official YouTube app experience (e.g., for casting to TV, live chat, or comments), recommend **ReVanced** — the community successor to YouTube Vanced. Explain the trade-offs: it patches the official app on-device, requires microG for login, and carries ToS risk. Guide them to revanced.app for the patcher.

## Decision Points

Ask the user: "Do you need to watch YouTube on your phone, desktop, or both?" NewPipe is Android-only, FreeTube is desktop-only, LibreTube is Android-only, and Invidious works in any browser. If they need both, recommend NewPipe (phone) + FreeTube (desktop).

Ask the user: "Do you use YouTube's algorithm to discover new content?" If yes, explain that these clients have no recommendation algorithm — you search for content intentionally. This is a feature, not a bug. If they want discovery, suggest using Invidious with public instances (which may have basic recommendations) or subscribing to curated channels.

## Pitfalls

- YouTube periodically changes its API, which can break NewPipe, LibreTube, and Invidious. The developers usually fix these breakages within days, but there may be brief outages. The user should check for updates when something stops working.
- ReVanced requires patching the official YouTube APK on-device. This is a technical process and carries a theoretical ToS risk (Google has not enforced against ReVanced users, but it could). MicroG is required for login.
- Grayjay (FUTO) is a multi-platform video aggregator that supports YouTube, Twitch, Rumble, Odysee, PeerTube, and Nebula. It is newer and less battle-tested than NewPipe. Only recommend it if the user wants a single app for multiple platforms.
- Background playback (NewPipe, FreeTube) uses more battery. The user should be aware of this.
- Importing subscriptions from Google Takeout is a one-time process. If the user subscribes to a new channel later, they need to add it manually in the client.

## Sources

1. nytimes.com/2018/03/10/opinion/sunday/youtube-politics-radical.html — New York Times: Zeynep Tufekci — "YouTube, the Great Radicalizer" — the seminal 2018 essay documenting how the recommendation algorithm consistently pushed users toward progressively more extreme content
2. bylinetimes.com/2026/01/27/how-youtubes-algorithm-pushed-people-into-neo-nazism/ — Byline Times: study of Patriotic Alternative published in Studies in Conflict & Terrorism — 27 of 33 far-right activists cited YouTube as key radicalization tool
3. npr.org/2022/09/06/1121343898/social-media-can-inflame-your-emotions-and-its-a-byproduct-of-its-design — NPR: Max Fisher interview on The Chaos Machine — how YouTube and Facebook algorithms amplify outrage to maximize engagement
4. mozillafoundation.org/en/blog/congratulations-youtube-now-show-your-work/ — Mozilla Foundation: calls out YouTube's claims that they are fixing the problem

## Guides

1. privacyguides.org/en/frontends/ — PrivacyGuides: YouTube frontends — recommends Invidious, Piped, FreeTube, LibreTube, NewPipe
2. newpipe.net — NewPipe: FOSS Android YouTube client — no Google services, background playback, downloads, also supports PeerTube/SoundCloud/Bandcamp
3. libretube.dev — LibreTube: open-source Android YouTube client — routes through Piped instances, Material You UI, SponsorBlock built in
4. freetubeapp.io — FreeTube: FOSS desktop YouTube client for Windows/macOS/Linux — local subscriptions, history, playlists, SponsorBlock optional
5. invidious.io — Invidious: self-hostable web frontend for YouTube — public instances with Tor/I2P support, no JavaScript required
6. grayjay.app — Grayjay: multi-platform video aggregator by FUTO — YouTube, Twitch, Rumble, Odysee, PeerTube, Nebula in one app
7. revanced.app — ReVanced: community successor to YouTube Vanced — patches official app on-device, requires microG for login
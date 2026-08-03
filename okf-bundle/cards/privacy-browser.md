---
type: "lbr8 Protocol Card"
title: "Private Browser"
description: "Switch from Chrome to a browser that blocks ads, trackers, and fingerprinting by default."
tags:
  - "phase-1"
  - "network"
  - "basic"
  - "p1"
  - "tracking"
  - "big-tech-surveillance"
  - "ad-targeting"
related:
  - "cards/search-engine.md"
  - "cards/anonymous-browsing.md"
  - "cards/dns-blocking.md"
---

## Why

Your browser sees every website you visit, every search you make, every link you click. Chrome is the world's largest surveillance tool — Google uses it to feed the ad-targeting machine that generates 80% of its revenue. When you use Chrome, Google knows your browsing history, search queries, and every interaction with the web. Switching browsers is one of the single highest-impact privacy change you can make. The key threats a private browser addresses: (1) cross-site tracking via cookies and pixels, (2) browser fingerprinting — silently identifying you by your screen size, fonts, plugins, and hardware profile, and (3) engine monoculture — Chromium powers Chrome, Edge, Brave, Vivaldi, and Opera. When one engine dominates, one company (Google) controls web standards. Firefox/Gecko is the only independent engine left.

## Steps

### General

A private browser blocks third-party trackers, resists fingerprinting, and doesn't phone home to an ad company. Choose based on your threat model and how much configuration you're willing to do. All options below are open source and free unless noted.

<strong>Brave</strong> (MPL-2.0, 21,946★, Chromium) — recommended for most users. Shields block ads, trackers, and fingerprinting scripts out of the box — zero configuration needed. Full uBlock Origin still works (Brave maintains MV2 support, unlike Chrome which killed it in July 2025). The trade-off: Brave ships with crypto features (BAT Rewards, wallet), an AI assistant (Leo), and VPN upsells that most users don't want. All of these are off by default and can be disabled in Settings. Available on Android, iOS, Windows, macOS, and Linux.

<strong>Brave Origin</strong> ($59.99 one-time, free on Linux) — Brave without the bloat. Removes Leo, Rewards, Brave Ads, Wallet, News, Playlist, Talk, VPN, and all upsells — keeping only the core Shields engine. Same privacy protections, no crypto, no AI, no ad network. A one-time purchase that gives you the clean browser Brave should have been from the start.

<strong>Mullvad Browser</strong> (MPL-2.0, Gecko ESR, Tor Project + Mullvad VPN) — the strongest anti-fingerprinting browser. Instead of randomizing your fingerprint (which can itself be a tell), it makes all Mullvad Browser users look identical — the one defense the 2025 "Breaking the Shield" research couldn't generically defeat. Zero telemetry, zero accounts, zero sync. uBlock Origin and NoScript pre-installed. Runs in permanent private mode (cookies cleared on close). Desktop only. Best paired with a VPN for IP-level anonymity, but anti-fingerprinting works standalone. Don't add extensions — it makes your fingerprint unique.

<strong>Firefox + uBlock Origin</strong> (MPL-2.0, 15,000+★, Gecko) — the only major non-Chromium engine. Out of the box, Firefox trails Brave (telemetry on, Google default search, weak fingerprinting). With 20 minutes of hardening (Strict Enhanced Tracking Protection, privacy.resistFingerprinting enabled, telemetry disabled, uBlock Origin installed), it becomes a top-tier privacy browser with the most customization of any option. Full uBlock Origin support (Firefox committed to MV2 long-term). Best for users who want engine diversity and are willing to configure.

<strong>LibreWolf</strong> (MPL-2.0, Codeberg, Gecko ESR) — zero-config hardened Firefox for desktop. Telemetry compiled out (not just toggled off), Pocket removed, DRM disabled, RFP enabled by default, uBlock Origin preinstalled, DNS-over-HTTPS on (Quad9). Full Firefox extension catalog works (unlike Mullvad). No sync, no mobile — significant friction for multi-device users. Tracks Firefox ESR with 1-7 day patch delay. ~5% site breakage from RFP (banking, airline sites) — per-site exceptions handle it.

### Android

Brave (free, Shields block ads/trackers by default, no config needed). For hardened Firefox on Android, see the desktop tab — there is no good standalone hardened Firefox build for Android at this time.

### iOS

Brave (free, Shields block ads/trackers by default). All iOS browsers use WebKit under the hood — engine choice is moot on iOS. Brave's built-in Shields give it the edge over Safari's weaker tracking protection.

## Going Further

<strong>Multi-browser strategy</strong>
Many privacy-focused users run two browsers: a hardened browser (Mullvad or LibreWolf) for sensitive browsing — banking, health, research — and Brave or Firefox for everyday sites that need logins and extensions. This separates your sensitive identity from your daily browsing.

<strong>Tor Browser</strong>
If your threat model includes a determined adversary — a government, a stalker, or anyone who can observe your network traffic — use Tor Browser. It routes traffic through three encrypted relays, hiding your IP from both the websites you visit and your ISP. All Tor Browser users share an identical fingerprint. Slower than any option here, and many sites block Tor exits. Use it for specific sensitive sessions, not as a daily driver. See the <a href="/cards/anonymous-browsing">Anonymous Browsing</a> card for full setup.

<strong>Manifest V3 context</strong>
Google killed full uBlock Origin on Chrome in July 2025 by removing the webRequest API (Manifest V3). uBlock Origin Lite on Chrome is a reduced version — no cosmetic filtering, no scriptlet injection, limited filter lists. Full uBlock Origin still works on Firefox and Brave. This is a structural reason to choose a non-Chrome browser if content blocking matters to you.

## Sources

1. amnesty.org/en/latest/news/2025/09/is-court-misses-chance-to-rein-in-google-power/ (Amnesty International: "Chrome has been a key tool in expanding these data harvesting practices" — US court declined to force Google to sell Chrome despite search monopoly ruling)
2. protonprivacy.substack.com/p/chrome-is-a-surveillance-platform (Proton: "Chrome Is a Surveillance Platform" — 30+ fingerprinting vectors, 23+ storage/tracking mechanisms, no native CNAME cloaking protection, third-party cookies still active with no removal timeline)
3. decrypt.co/367193/chrome-removes-privacy-claim-gemini-nano-google (Decrypt: Chrome silently downloaded a 4GB AI model to users' devices, then removed the privacy disclosure that promised data would stay on-device)
4. privacytests.org (PrivacyTests.org: open-source browser privacy comparison — Brave 143/156, Mullvad 141/156)
5. dl.acm.org/doi/10.1145/3696410.3714713 (Breaking the Shield: Analyzing and Attacking Canvas Fingerprinting Defenses in the Wild — ACM Web Conference 2025, showed randomization can be defeated but uniformity resists)
6. blog.mozilla.org/en/firefox/firefox-manifest-v3-adblockers/ (Mozilla: Firefox will continue supporting both blocking webRequest and declarativeNetRequest, keeping full uBlock Origin available)

## Guides

1. brave.com (Brave: open-source Chromium browser with built-in ad/tracker blocking)
2. mullvad.net/en/browser (Mullvad Browser: Tor Project fingerprinting without Tor network, developed with Mullvad VPN)
3. librewolf.net (LibreWolf: hardened Firefox with telemetry compiled out, RFP enabled, uBlock Origin preinstalled)
4. privacyguides.org/en/desktop-browsers/ (PrivacyGuides: desktop browser recommendations with anti-fingerprinting analysis)
5. themarkup.org/blacklight (The Markup: Blacklight tool — scan websites for Meta Pixel and other trackers)
6. eylenburg.github.io/browser_comparison.htm (Eylenburg: web browser comparison table — 7 browsers across desktop, Android, and iOS with engine, telemetry, ad-blocking, and privacy feature analysis)

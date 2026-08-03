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
---

## Context for the Agent

This card helps the user switch from Chrome (or another Big Tech browser) to a browser that blocks ads, trackers, and fingerprinting by default. Use it when the user wants to stop cross-site tracking and reclaim their browsing privacy.

## Why This Matters

Your browser sees every website you visit, every search you make, every link you click. Chrome is the world's largest surveillance tool — Google uses it to feed the ad-targeting machine that generates 80% of its revenue [1]. Chrome has 30+ fingerprinting vectors, 23+ storage/tracking mechanisms, and no native CNAME cloaking protection [2]. Amnesty International has called Chrome "a key tool in expanding these data harvesting practices" [1]. Switching browsers is one of the single highest-impact privacy changes you can make. The key threats a private browser addresses: (1) cross-site tracking via cookies and pixels, (2) browser fingerprinting — silently identifying you by your screen size, fonts, plugins, and hardware profile, and (3) engine monoculture — Chromium powers Chrome, Edge, Brave, Vivaldi, and Opera. Firefox/Gecko is the only independent engine left.

## Coaching Flow

### Step 1: Choose the Right Browser
Based on the user's onboarding context (platform, skill level, threat concerns), recommend one of these:

- **Brave (recommended for most users):** Blocks ads, trackers, and fingerprinting out of the box — zero configuration needed. It's Chromium-based, so all Chrome extensions work. Full uBlock Origin still works (Brave maintains MV2 support). Mention that it ships with crypto features (BAT Rewards, wallet) and an AI assistant (Leo) — these can be disabled in settings if the user doesn't want them.
- **LibreWolf (for privacy purists):** A hardened Firefox fork with telemetry compiled out, RFP (Resist Fingerprinting) enabled, and uBlock Origin preinstalled. No account needed, no Pocket, no Mozilla VPN upsells. Trade-off: some websites may break due to strict fingerprinting protection.
- **Mullvad Browser (for maximum anonymity):** Developed by the Tor Project and Mullvad VPN. Gives every user the same fingerprint so you blend into the crowd. No VPN required — it's about fingerprint uniformity, not IP hiding. Trade-off: it's intentionally inconvenient (no persistent storage, no extensions).

### Step 2: Install and Configure
Guide the user through installation:
1. Download from the browser's official website (or F-Droid for mobile)
2. Set it as the default browser in system settings
3. For Brave: immediately disable the crypto wallet and Leo AI if the user doesn't want them (Settings → Wallet → Disable, Settings → Leo → Disable)
4. For any browser: install uBlock Origin in "medium mode" or "hard mode" for maximum tracking protection
5. Install additional privacy extensions: Privacy Badger (EFF), CanvasBlocker (fingerprinting), and NoScript for advanced users

### Step 3: Migrate from Chrome
Walk the user through importing bookmarks and passwords from Chrome:
1. In the new browser: Settings → Import Bookmarks → Select Chrome
2. Tell them not to import Chrome settings (they carry Chrome's privacy-hostile defaults)
3. Encourage them to gradually stop using Chrome entirely. After a week, uninstall Chrome if they feel comfortable

### Step 4: Set Up Mobile Browser
- **Android:** Recommend Brave or Mull (a hardened Firefox fork based on Fennec)
- **iOS:** Recommend Brave or Firefox Focus. Note: iOS browsers are all Safari WebKit under the hood, so the privacy gains are more limited — but Brave still blocks trackers and ads at the network level

### Step 5: Test Your New Setup
Guide the user to test their browser at **coveryourtracks.eff.org** (EFF's Panopticlick) to see if they are being tracked. They should see a result that says "Your browser has protection against fingerprinting" or "Your browser has strong protection against tracking."

## Decision Points

The onboarding already knows the user's platform and skill level. Use that:
- **Beginner / wants it to just work:** Brave
- **Intermediate / willing to tweak:** LibreWolf
- **Advanced / maximum anonymity:** Mullvad Browser

Ask the user: "Which browser are you coming from?" If Chrome, address the migration concern. If Safari, explain that Safari blocks some trackers but Apple's Private Relay and iCloud keychain are still tied to their Apple ID. If Firefox, they're already on the right engine — suggest LibreWolf for a hardened experience.

## Pitfalls

- Chrome extensions that use Manifest V3 (which Chrome now requires) are less effective at blocking. Brave maintains MV2 support, but the user should know this will eventually change.
- Some websites (especially banking, government, and streaming) break with strict fingerprinting protection. LibreWolf and Mullvad Browser are more likely to break things than Brave. If a site breaks, suggest the user try Brave or a Chromium-based browser for that specific site.
- "Incognito mode" is not private. It only prevents local history storage — your ISP, employer, and the websites themselves still see everything. Do not let the user confuse incognito with privacy.
- uBlock Origin in "hard mode" blocks all third-party resources by default. This will break many websites. Coach the user to use "medium mode" (block third-party scripts, allow third-party frames) and only go to "hard mode" if they are technical and willing to do manual whitelisting.

## Sources

1. amnesty.org/en/latest/news/2025/09/is-court-misses-chance-to-rein-in-google-power/ — Amnesty International: "Chrome has been a key tool in expanding these data harvesting practices" — US court declined to force Google to sell Chrome despite search monopoly ruling
2. protonprivacy.substack.com/p/chrome-is-a-surveillance-platform — Proton: "Chrome Is a Surveillance Platform" — 30+ fingerprinting vectors, 23+ storage/tracking mechanisms, no native CNAME cloaking protection
3. decrypt.co/367193/chrome-removes-privacy-claim-gemini-nano-google — Decrypt: Chrome silently downloaded a 4GB AI model to users' machines without consent

## Guides

1. brave.com — Brave: open-source Chromium browser with built-in ad/tracker blocking
2. mullvad.net/en/browser — Mullvad Browser: Tor Project fingerprinting without Tor network, developed with Mullvad VPN
3. librewolf.net — LibreWolf: hardened Firefox with telemetry compiled out, RFP enabled, uBlock Origin preinstalled
4. privacyguides.org/en/desktop-browsers/ — PrivacyGuides: desktop browser recommendations with anti-fingerprinting analysis
5. themarkup.org/blacklight — The Markup: Blacklight tool — scan websites for Meta Pixel and other trackers
6. eylenburg.github.io/browser_comparison.htm — Eylenburg: web browser comparison table — 7 browsers across desktop, Android, and iOS with engine, telemetry, ad-blocking, and privacy feature analysis
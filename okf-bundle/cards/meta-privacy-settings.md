---
type: "lbr8 Protocol Card"
title: "Meta Account Lockdown"
description: "Disconnect off-Meta activity tracking, disable ad personalization, and never use the in-app browser."
tags:
  - "phase-0"
  - "identity"
  - "basic"
  - "p0"
  - "big-tech-surveillance"
  - "data-breach"
related:
  - "cards/messaging-privacy.md"
  - "cards/permissions-audit.md"
  - "cards/screen-time-app-blockers.md"
  - "cards/digital-footprint.md"
---

## Context for the Agent

This card is about locking down Meta (Facebook, Instagram, WhatsApp) account settings to minimize tracking. Use it when the user uses Meta platforms and wants to reduce data collection. Note: the user may not have a Meta account — they can still be tracked via the Facebook Pixel and SDK.

## Why This Matters

Meta tracks you even if you've never had an account. Whistleblowers Frances Haugen and Sarah Wynn-Williams have confirmed what the company denies in public: Meta knows its platforms amplify hate, harm teenage mental health, and enable political violence, and it chooses profit over safety every time [1][2][3][4]. Meta built its empire on surveillance — the Facebook SDK embedded in third-party apps, the Meta Pixel on millions of websites, and the Conversions API for server-side tracking that bypasses all browser protections. The in-app browsers in Facebook and Instagram inject JavaScript into every external website you visit, tracking every tap, form input, and password [5]. Even if you quit all Meta platforms, your shadow profile persists: a friend uploads a photo of you, an app uses the Facebook SDK, a website has the Pixel — and you're in their system. The goal is to dim the lights, not turn them off.

## Coaching Flow

### Step 1: Disconnect off-Meta activity
Guide the user to accountscenter.facebook.com → "Your information and permissions" → "Your activity off Meta technologies" → "Manage future activity" → "Disconnect future activity." Explain that this doesn't stop Meta from tracking off-platform activity, but it tells Meta not to tie that data to their account. It's a partial fix, but worth doing.

### Step 2: Turn off ad personalization
In the same Accounts Center, guide them to "Ad preferences." Turn off "Use of off-Meta activity for ads." Customize the list of information advertisers can use — tell them to turn off everything they can. They'll still see ads, but they'll be generic.

### Step 3: Never use the in-app browser
This is critical. Tell the user: **NEVER open links inside Facebook or Instagram's in-app browser.** It injects JavaScript into every page you visit, tracking every tap, form input, and password you type [5]. Always long-press a link and select "Open in [device's real browser]" or copy the URL and paste it into their regular browser. On Android, they can also set a third-party browser to always open links by default.

### Step 4: Revoke app permissions
Guide the user to revoke camera, microphone, location, and contacts access from all Meta apps:
- **Android**: Settings → Apps → [Facebook/Instagram/Messenger] → Permissions → revoke everything not essential
- **iOS**: Settings → Privacy & Security → review each permission type and toggle off for Meta apps
Suggest they use the browser version of Facebook and Instagram instead of the apps. The browser version has fewer tracking capabilities and no access to device sensors.

### Step 5: WhatsApp settings
If the user uses WhatsApp:
- **EU/UK/EEA users**: Guide them to WhatsApp Settings → Privacy → toggle off "Share data with Meta." This is a legal right in those regions.
- **Everyone else**: This option doesn't exist. Tell them to at minimum revoke all app permissions (camera, microphone, location, contacts, photos). Remind them that WhatsApp metadata (who they message, when, for how long) is always visible to Meta regardless of end-to-end encryption. If they're concerned about metadata, guide them to the "Messaging Privacy" card.

### Step 6: Instagram-specific
Suggest the user use Instagram in a browser, not the app. Research in June 2025 found that the Instagram app listened on local ports to link the user's web browsing to their Meta account [6]. Meta halted this practice after disclosure, but the architecture is still in place.

### Step 7: Block the Meta Pixel
Tell the user to use a privacy browser (like Firefox or Brave) with uBlock Origin installed. This blocks the Meta Pixel from loading on most third-party websites. It's the most effective client-side defense against Meta's off-platform tracking.

### Step 8: Opt out of AI training (if applicable)
For EU/UK/EEA residents: they can opt out of AI training in Accounts Center. For everyone else: they are opted in automatically and cannot opt out. This is one of the clearest examples of Meta's attitude toward user consent.

## Decision Points

Ask the user: **"Do you use Facebook, Instagram, WhatsApp, or all three?"** The steps differ slightly by platform. If they don't use any Meta platforms, tell them the most important step is blocking the Meta Pixel (Step 7) and revoking any Meta app permissions (Step 4) if they have apps installed but don't use them.

Also ask: **"Are you in the EU/UK/EEA?"** This affects whether WhatsApp's "Share data with Meta" toggle and the AI training opt-out are available.

## Pitfalls

- **"I don't have a Facebook account, so Meta doesn't track me"** — Not true. The Facebook SDK is embedded in hundreds of thousands of apps. The Meta Pixel is on millions of websites. Meta builds shadow profiles of non-users.
- **In-app browser is the most dangerous tracking vector** — Meta's in-app browser can see passwords, form data, and every page interaction. Never use it.
- **WhatsApp E2E encryption ≠ privacy** — Metadata (who, when, how long) is visible to Meta. E2E encryption only protects message content in transit.
- **App permissions are broader than they seem** — The Facebook app has access to camera, microphone, location, storage, phone, SMS, and contacts by default. Revoke everything that isn't needed for the app's core function.
- **Deleting the app doesn't delete the account** — The user must delete their account separately via Accounts Center. Simply removing the app from their phone does nothing to stop tracking.
- **Meta Pixel bypasses browser privacy features** — The Conversions API sends data from the server side, bypassing all browser-based tracking protections. Even with uBlock Origin, some tracking still happens server-to-server.

## Sources

1. wsj.com/articles/the-facebook-files-11631713039 (WSJ: The Facebook Files — Frances Haugen whistleblower documents showing Meta prioritized profit over safety)
2. cbsnews.com/news/facebook-whistleblower-frances-haugen-misinformation-public-60-minutes-2021-10-03/ (CBS 60 Minutes: Frances Haugen reveals Meta's own research shows it amplifies hate and misinformation)
3. cnn.com/2025/03/11/tech/meta-whistleblower-book-sarah-wynn-williams (CNN: Ex-Meta executive Sarah Wynn-Williams publishes "Careless People" — insider account of growth-at-all-costs culture)
4. independent.co.uk/news/world/americas/us-politics/facebook-whistleblower-testify-meta-zuckerberg-b2730365.html (The Independent: Sarah Wynn-Williams testifies Meta undermined national security working with China)
5. krausefx.com/blog/ios-privacy-instagram-and-facebook-can-track-anything-you-do-on-any-website-in-their-in-app-browser (Felix Krause: Instagram and Facebook in-app browsers inject JavaScript to track all website interactions)
6. theregister.com/security/2025/06/04/meta-pixel-halts-android-localhost-tracking-after-disclosure/1189660 (The Register: Meta Pixel halts Android localhost tracking — Facebook/Instagram apps listened on local ports to link web browsing to user accounts)
7. amnesty.org/en/latest/news/2019/11/google-facebook-surveillance-privacy-2/ (Amnesty International: Surveillance Giants — Google and Facebook's pervasive surveillance poses unprecedented danger to human rights)

## Guides

1. proton.me/blog/stop-meta-tracking (Proton: How to stop Meta from tracking you)
2. youtube.com/watch?v=Yv2Eb_kJous (Proton: Every Way Meta Tracks You)
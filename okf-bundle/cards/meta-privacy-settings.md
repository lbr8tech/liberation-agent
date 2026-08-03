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

## Why

Meta tracks you even if you've never had an account. Whistleblowers Frances Haugen and Sarah Wynn-Williams have confirmed what the company denies in public: Meta knows its platforms amplify hate, harm teenage mental health, and enable political violence, and it chooses profit over safety every time. Meta built its empire on surveillance — the Facebook SDK embedded in third-party apps, the Meta Pixel on millions of websites, and the Conversions API for server-side tracking that bypasses all browser protections. The in-app browsers in Facebook and Instagram inject JavaScript into every external website you visit, tracking every tap, form input, and password. Even if you quit all Meta platforms, your shadow profile persists: a friend uploads a photo of you, an app uses the Facebook SDK, a website has the Pixel — and you're in their system. The goal is to dim the lights, not turn them off.

## Steps

### General

1. Accounts Center (accountscenter.facebook.com): Go to "Your information and permissions" → "Your activity off Meta technologies" → "Manage future activity" → "Disconnect future activity." This doesn't stop tracking but tells Meta not to tie off-platform activity to your account
2. Ad preferences: Turn off "Use of off-Meta activity for ads" and customize what info advertisers can use
3. In-app browser: NEVER use Facebook/Instagram's in-app browser — it sees everything you type, every form you fill. Always open links in your real browser
4. App permissions: Revoke camera, microphone, location, and contacts access from all Meta apps. Use browser version instead of the app
5. WhatsApp: Turn off "Share data with Meta" (EU/UK only). Outside EU: revoke all app permissions. Metadata (who you message, when) is always visible to Meta regardless of E2E encryption
6. Instagram: Use in browser, not the app. The app was caught listening on local ports to link your web browsing to your Meta account (June 2025 research, halted after disclosure)
7. AI training: EU/UK/EEA residents can opt out of AI training. Everyone else is opted in automatically
8. Meta Pixel: Use a privacy browser with uBlock Origin to block the Meta Pixel on third-party websites
9. Meta Ray-Ban glasses: Use the Nearby Glasses app to detect smart glasses nearby

## Sources

1. wsj.com/articles/the-facebook-files-11631713039 (WSJ: The Facebook Files — Frances Haugen whistleblower documents showing Meta prioritized profit over safety)
2. cbsnews.com/news/facebook-whistleblower-frances-haugen-misinformation-public-60-minutes-2021-10-03/ (CBS 60 Minutes: Frances Haugen reveals Facebook's own research shows it amplifies hate and misinformation)
3. cnn.com/2025/03/11/tech/meta-whistleblower-book-sarah-wynn-williams (CNN: Ex-Meta executive Sarah Wynn-Williams publishes "Careless People" — insider account of growth-at-all-costs culture)
4. independent.co.uk/news/world/americas/us-politics/facebook-whistleblower-testify-meta-zuckerberg-b2730365.html (The Independent: Sarah Wynn-Williams testifies Meta undermined national security working with China)
5. krausefx.com/blog/ios-privacy-instagram-and-facebook-can-track-anything-you-do-on-any-website-in-their-in-app-browser (Felix Krause: Instagram and Facebook in-app browsers inject JavaScript to track all website interactions)
6. theregister.com/security/2025/06/04/meta-pixel-halts-android-localhost-tracking-after-disclosure/1189660 (The Register: Meta Pixel halts Android localhost tracking — Facebook/Instagram apps listened on local ports to link web browsing to user accounts)
7. amnesty.org/en/latest/news/2019/11/google-facebook-surveillance-privacy-2/ (Amnesty International: Surveillance Giants — Google and Facebook's pervasive surveillance poses unprecedented danger to human rights)

## Guides

1. proton.me/blog/stop-meta-tracking (Proton: How to stop Meta from tracking you)
2. youtube.com/watch?v=Yv2Eb_kJous (Proton: Every Way Meta Tracks You)

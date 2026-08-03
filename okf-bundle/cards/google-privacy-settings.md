---
type: "lbr8 Protocol Card"
title: "Google Account Lockdown"
description: "Turn off activity tracking, location history, ad personalization, and AI data sharing across all Google services."
tags:
  - "phase-0"
  - "identity"
  - "basic"
  - "p0"
  - "big-tech-surveillance"
  - "govt-surveillance"
  - "data-breach"
related:
  - "cards/email-migration.md"
  - "cards/search-engine.md"
  - "cards/privacy-browser.md"
  - "cards/maps-privacy.md"
  - "cards/privacy-video-client.md"
---

## Why

Google is the world's largest surveillance company. It pioneered surveillance capitalism — extracting human behavioral data as free raw material, computing it into prediction products, and selling those predictions to anyone willing to pay. Every search, email, YouTube watch, Maps destination, and Chrome keystroke feeds this machine. Google's own Gemini privacy page admits connected app data is used to train AI models "for everyone." When Google scrapped its plan to remove third-party cookies from Chrome, it confirmed that surveillance is the product, not a side effect. Even with every setting locked down, Chrome still sends address-bar keystrokes to Google unsigned, and Google Analytics tracks you on over half the web. The goal is harm reduction.

## Steps

### General

Google logged 24,000 interactions per month even for a privacy-conscious user. Lock down your account settings before migrating away, or while still using Google services:

1. Chrome: Turn off "Allow Chrome sign-in," "Improve search suggestions," "Make searches and browsing better"
2. Search: Turn off "Personal results" and "Activity controls" → Web & App Activity, Location History, YouTube History
3. Gmail: Turn off "Smart features in Gmail, Chat, and Meet" and "Google Workspace smart features." Enable "Ask before displaying external images" (blocks tracking pixels)
4. Maps: Turn off "Timeline" (formerly Location History). On phone, revoke Location permission for all Google apps
5. YouTube: Turn off "Pause watch history" and "pause search history." Use signed-out or via alternative client (see privacy-video-client card)
6. Google Takeout: Export your data before changing settings — some data is deleted when you turn off activity controls
7. AI: Do not connect your apps to Gemini. If already connected, disconnect — connected data is used to train AI models "for everyone"

These settings reduce Google's collection but don't stop it entirely. Chrome sends address-bar keystrokes to Google even unsigned. Google Analytics tracks you on 50%+ of websites. The goal is harm reduction until you can fully migrate.

## Sources

1. amnesty.org/en/latest/news/2019/11/google-facebook-surveillance-privacy-2/ (Amnesty International: Surveillance Giants — Google and Facebook's pervasive surveillance poses an unprecedented danger to human rights)
2. 404media.co/google-leak-reveals-thousands-of-privacy-incidents/ (404 Media: Google Leak Reveals Thousands of Privacy Incidents — internal database of self-reported privacy failures)
3. arstechnica.com/tech-policy/2025/01/google-loses-in-court-faces-trial-for-collecting-data-on-users-who-opted-out/ (Ars Technica: Google loses in court, faces trial for collecting data on users who opted out)
4. wired.com/story/google-dv360-banned-audience-segments-national-security/ (WIRED: Google Ad-Tech Users Can Target National Security Decision Makers and People With Chronic Diseases)

## Guides

1. proton.me/blog/how-to-de-google (Proton: How to de-Google your life)
2. youtube.com/watch?v=WJ8clVdaRKA (Proton: How Google Tracks Everything You Do)
3. proton.me/blog/delete-gmail-account (Proton: How to delete your Gmail account)
4. mashable.com/article/delete-gmail-account (Mashable: How to make your Gmail account self destruct)

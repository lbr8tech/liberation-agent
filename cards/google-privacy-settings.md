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

## Context for the Agent

This card is about locking down Google account settings to minimize tracking across Google's services. Use it when the user wants to reduce Google's data collection while they still use Google services, or as a step before migrating away.

## Why This Matters

Google is the world's largest surveillance company. It pioneered surveillance capitalism — extracting human behavioral data as free raw material and selling predictions to anyone willing to pay [1]. Every search, email, YouTube watch, Maps destination, and Chrome keystroke feeds this machine. When Google scrapped its plan to remove third-party cookies from Chrome, it confirmed that surveillance is the product, not a side effect. A leaked internal database revealed thousands of self-reported privacy incidents [2]. Even with every setting locked down, Chrome still sends address-bar keystrokes to Google unsigned, and Google Analytics tracks you on over half the web. The goal is harm reduction.

## Coaching Flow

### Step 1: Export data first
Tell the user to go to takeout.google.com and export their data BEFORE changing any settings. Some data (like location history, web & app activity) is deleted when the corresponding activity control is turned off. Exporting first ensures they don't lose anything they might want later.

### Step 2: Lock down activity controls
Guide the user to myaccount.google.com → Data & privacy → History settings. Walk through each:
1. **Web & App Activity**: Turn off. This stops Google from saving searches, Chrome activity, and activity from apps. If they use Google services daily, this is the biggest single change.
2. **Location History**: Turn off. This stops Google from building a Timeline of everywhere they've been. Tell them that Google Maps still works for navigation without it.
3. **YouTube History**: Turn off both watch history and search history. Without this, YouTube recommendations will be generic, but that's a feature, not a bug.
4. **Voice & Audio Activity**: Turn off. This stops Google from saving recordings of voice commands and audio interactions.

### Step 3: Turn off ad personalization
Guide them to myaccount.google.com → Data & privacy → Ad settings. Turn off "Ad personalization." This doesn't stop ads — it stops Google from using their data to target them. They'll still see ads, but they'll be generic and irrelevant.

### Step 4: Lock down Chrome
If the user uses Chrome, guide them to Chrome settings → You and Google → Sync and Google services. Turn off:
- "Allow Chrome sign-in" (if they don't need sync)
- "Improve search suggestions"
- "Make searches and browsing better"
- "Send URLs of pages visited to Google"
Tell them these settings send every keystroke and URL to Google. Even unsigned, Chrome sends address-bar keystrokes to Google.

### Step 5: Disconnect AI/Gemini
Guide them to myaccount.google.com → Data & privacy → Gemini and connected apps. Disconnect any connected apps. Google's Gemini privacy page admits that connected app data is used to train AI models "for everyone." If they haven't connected anything, tell them not to.

### Step 6: Gmail privacy settings
If the user uses Gmail, guide them to Gmail settings → See all settings → General. Turn off:
- "Smart features in Gmail, Chat, and Meet"
- "Google Workspace smart features"
- Enable "Ask before displaying external images" — this blocks tracking pixels in emails

### Step 7: YouTube privacy
If the user uses YouTube, guide them to youtube.com → Settings → Privacy. Turn off "Pause watch history" and "Pause search history." Suggest they use YouTube signed out, via an alternative client (see privacy-video-client card), or via a privacy-focused frontend like Invidious or Piped.

## Decision Points

The agent knows the user's platform from onboarding. However, ask the user: **"Do you still use Google services regularly, or are you planning to migrate away?"** If they're staying, these settings are harm reduction. If they're migrating, point them to the related cards: email-migration, search-engine, privacy-browser, maps-privacy, and privacy-video-client.

## Pitfalls

- **Settings don't stick** — Google periodically resets or changes settings. Set a reminder to check every 3-6 months.
- **Google Analytics is everywhere** — Even with a locked-down account, Google Analytics tracks the user on over 50% of websites. A privacy browser with uBlock Origin and fingerprinting protection is the only client-side defense.
- **Chrome is inherently tracking** — Chrome sends address-bar keystrokes to Google even when signed out and even with all settings off. The only real fix is switching to a privacy-focused browser.
- **Android phones phone home** — Locking down the Google account does not stop the Android OS from sending telemetry. See the "Android Debloat" card for phase 1.
- **Takeout before lockdown** — Remind the user to export their data before turning off activity controls. Google deletes historical data when you turn off the corresponding control.
- **Google's privacy policy is the floor, not the ceiling** — Even with everything turned off, Google still collects data. The only way to stop it completely is to stop using Google services entirely.

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
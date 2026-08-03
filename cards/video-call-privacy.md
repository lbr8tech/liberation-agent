---
type: "lbr8 Protocol Card"
title: "Private Video Calls"
description: "Use Signal, Jitsi, or Brave Talk instead of Zoom, Meet, or Teams for sensitive conversations."
tags:
  - "phase-1"
  - "communication"
  - "basic"
  - "p1"
  - "surveillance-capitalism"
  - "mass-surveillance"
  - "data-brokers"
related:
  - "cards/messaging-privacy.md"
  - "cards/privacy-browser.md"
---

## Context for the Agent

This card is for users who need to have sensitive conversations over video. Use it when the user expresses concern about Zoom/Meet/Teams surveillance or asks for private alternatives.

## Why This Matters

Video call platforms see who you meet, when, how long, and from what IP. Zoom quietly updated its terms in 2023 to claim rights to use customer data for AI training, backtracking only after public backlash. Google Meet turned on Gemini AI recording by default for Workspace users in January 2025 — USAID staffers discovered their meetings were being recorded without consent [2]. Microsoft Teams transfers extensive telemetry to US servers; a Dutch government DPIA concluded organizations should not use Teams for sensitive data due to US surveillance access [3]. The alternatives — Signal, Proton Meet, Brave Talk — offer end-to-end encryption without data mining.

## Coaching Flow

### Step 1: Assess the user's needs
Ask the user: who are you having private calls with, and how many participants? This determines which tool to recommend:
- **1:1 or small group (up to 40 people):** Signal — already installed if they followed the messaging card. E2EE by default, no metadata beyond routing.
- **Larger or recurring meetings (up to 50 participants, 1-hour calls):** Proton Meet — always-on E2EE via MLS protocol, open-source client, Swiss jurisdiction. Free tier available, no account needed for guests.
- **Quick, no-download calls (any browser):** Brave Talk — runs in any browser, no login required, built on Jitsi infrastructure with unlinkability by design.

### Step 2: Walk through the chosen option
- **Signal:** Guide the user to start a video call from an existing Signal conversation. Tap the video icon. Works on Android, iOS, and desktop.
- **Proton Meet:** Guide the user to open proton.me/meet in their browser. They can create a meeting link and share it. No account needed for participants. Works best in a privacy-focused browser like Brave or Firefox.
- **Brave Talk:** Guide the user to talk.brave.com. Generate a meeting link and share it. No download, no login, works in any browser.

### Step 3: Address the "but everyone uses Zoom" objection
If the user says their contacts won't switch, explain:
- Brave Talk requires no account or download — anyone can join from a browser link.
- Proton Meet guests don't need an account — just click the link.
- They can keep Zoom for non-sensitive calls and switch to Signal/Proton/Brave only for conversations that matter.

### Step 4: For self-hosters, mention Jitsi
If the user has a server or expresses interest in full control, mention they can self-host Jitsi Meet for unlimited participants, full data sovereignty, and no third-party dependency.

## Decision Points

Ask the user: **What's your primary use case?** 1:1 calls with privacy-minded contacts → Signal. Larger meetings with mixed audiences → Proton Meet or Brave Talk. Self-hosted → Jitsi.

## Pitfalls

- Warn that Signal group calls are limited to 40 participants — it's not a replacement for all-hands meetings.
- Warn that Proton Meet's free tier has a 1-hour time limit for calls with more than 2 participants.
- Remind the user that encrypted video calls are only as private as what's visible or audible in their room — the other end can still screen-record.

## Sources

1. eff.org/deeplinks/2020/03/what-you-should-know-about-online-tools-during-covid-19-crisis — EFF: What You Should Know About Online Tools — documents Zoom's attendee attention tracking, admin dashboards with real-time user activity, IP/location/device info per participant
2. eff.org/deeplinks/2020/06/will-zoom-bring-encryption-people-who-need-it-most — EFF: Will Zoom Bring Encryption to People Who Need It Most? — Zoom CEO admitted withholding E2EE from free users to "work together with FBI, with local law enforcement"
3. apnews.com/article/fact-check-zoom-ai-privacy-terms-of-service-06ff47e47439c2173390a4ca1389f652 — AP News: Zoom AI training terms controversy — Zoom updated terms to claim rights to customer data for AI training, backtracked after backlash
4. techcrunch.com/2023/08/08/zoom-data-mining-for-ai-terms-gdpr-eprivacy/ — TechCrunch: Zoom's legal tangle over AI data mining under GDPR — EU legal experts say Zoom needs opt-in consent for AI training
5. itbrew.com/stories/2025/02/13/google-s-gemini-ai-recorded-meetings-without-consent-two-usaid-staffers-tell-it-brew — IT Brew: Google Gemini AI recorded USAID meetings without consent — Workspace update turned on AI recording by default
6. privacycompany.eu/blog/new-dpia-for-the-dutch-government-and-universities-on-microsoft-teams-onedrive-and-sharepoint-online — Privacy Company: Dutch government DPIA on Microsoft Teams — concluded organizations should not use Teams for sensitive data due to US surveillance access; Teams E2EE is 1:1 only

## Guides

1. privacyguides.org/en/real-time-communication/ — PrivacyGuides: real-time communication recommendations — Signal, SimpleX, Briar with evaluation criteria
2. signal.org/ — Signal — official website — E2EE messaging and video calls
3. proton.me/meet — Proton Meet — official page — Always-on E2EE video conferencing, MLS protocol, Swiss jurisdiction
4. jitsi.org/ — Jitsi — official website — Open-source video conferencing, self-hostable
5. brave.com/talk/ — Brave Talk — official page — Browser-based private video calls, no login required

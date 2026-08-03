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

## Why

Video call platforms see who you meet, when, how long, and from what IP. **Zoom** collects mouse movements, keystrokes, mute/unmute events, and "attention tracking" data — and quietly updated its terms in 2023 to claim rights to use customer data for AI training, backtracking only after public backlash. **Google Meet** turned on Gemini AI recording by default for Workspace users in January 2025 — USAID staffers discovered their meetings were being recorded without consent. **Microsoft Teams** collects extensive diagnostic telemetry (who you call, how often, what features you use) and transfers it to US servers; a Dutch government DPIA concluded organizations should not use Teams for sensitive data due to US surveillance access.

The alternatives are straightforward. **Signal** offers E2EE video calls using the Signal Protocol — the server sees only ciphertext. **Proton Meet** provides always-on E2EE using the MLS protocol, open-source client, Swiss jurisdiction, and no-account guest access. **Brave Talk** runs in any browser with no download or login, built on Jitsi's infrastructure with unlinkability by design.

## Steps

### General

**Signal** — for 1:1 and small group calls (up to 40). E2EE by default, no metadata beyond routing. Already installed if you followed the messaging card.

**Proton Meet** — open proton.me/meet in any browser. E2EE always on via MLS protocol, open-source client, Swiss jurisdiction. Free tier: up to 50 participants, 1-hour calls. No account needed for guests.

**Brave Talk** — open talk.brave.com in any browser. Free for up to 4 participants, no login required. Built on Jitsi with additional unlinkability guarantees.

### iOS

**FaceTime** is acceptable for Apple-only calls — Apple's E2EE is legitimate. But it excludes Android contacts and Apple holds iMessage lookup logs (see messaging card).

## Self-Hosted

**Jitsi Meet** — the leading open-source video conferencing platform. Self-host via Docker Compose for full control over metadata, recordings, and data residency. The public meet.jit.si instance is operated by 8x8 (a US company) — self-hosting eliminates that trust dependency. E2EE available via Insertable Streams (Chrome-based browsers required). No account needed for participants.

Alternatives: BigBlueButton (bigbluebutton.org) — open-source, education-focused, supports hundreds of participants

## Going Further

**Self-host Jitsi for maximum control**
The public meet.jit.si instance is operated by 8x8 (a US company). For sensitive calls, self-host Jitsi on your own server — it's a Docker Compose deployment. This gives you full control over metadata, recordings, and data residency.

**The recording trap**
Even with E2EE, if you enable recording on any platform, the server gets the decryption keys to process the recording. Brave Talk explicitly notes this: "If you record a call, 8x8's servers will receive a set of keys to decrypt the video/audio stream." Disable recording for sensitive calls.

**Zoom's "E2EE" is limited**
Zoom added E2EE in 2020, but it disables features like cloud recording, live transcription, and join-before-host. Most enterprise Zoom deployments don't use it. Zoom's own privacy statement acknowledges collecting "mouse movements, clicks, keystrokes or actions (such as mute/unmute or video on/off)."

**Google Meet has no E2EE**
Google Meet uses transport encryption (TLS) — Google's servers can decrypt your call content. There is no end-to-end encryption option. Gemini AI features process meeting audio and may auto-enable without participant consent.

**Teams E2EE is 1:1 only**
Microsoft Teams offers E2EE only for unscheduled one-to-one calls. Group calls, meetings, and scheduled calls are not E2EE. The Dutch government's Data Protection Impact Assessment concluded that organizations should not use Teams for sensitive data due to US surveillance access risks.

## Sources

1. eff.org/deeplinks/2020/03/what-you-should-know-about-online-tools-during-covid-19-crisis (EFF: What You Should Know About Online Tools — documents Zoom's attendee attention tracking, admin dashboards with real-time user activity, IP/location/device info per participant, and admin ability to join any call without consent)
2. eff.org/deeplinks/2020/06/will-zoom-bring-encryption-people-who-need-it-most (EFF: Will Zoom Bring Encryption to People Who Need It Most? — Zoom CEO admitted withholding E2EE from free users to "work together with FBI, with local law enforcement"; EFF and Mozilla organized open letter demanding E2EE for all users)
3. apnews.com/article/fact-check-zoom-ai-privacy-terms-of-service-06ff47e47439c2173390a4ca1389f652 (AP News: Zoom AI training terms controversy — Zoom updated terms to claim rights to customer data for AI training, backtracked after backlash; "service generated data" still fair game)
4. techcrunch.com/2023/08/08/zoom-data-mining-for-ai-terms-gdpr-eprivacy/ (TechCrunch: Zoom's legal tangle over AI data mining under GDPR — EU legal experts say Zoom needs opt-in consent, not opt-out, for AI training on user data)
5. itbrew.com/stories/2025/02/13/google-s-gemini-ai-recorded-meetings-without-consent-two-usaid-staffers-tell-it-brew (IT Brew: Google Gemini AI recorded USAID meetings without consent — Workspace update turned on AI recording by default, staffers discovered it after the fact)
6. privacycompany.eu/blog/new-dpia-for-the-dutch-government-and-universities-on-microsoft-teams-onedrive-and-sharepoint-online (Privacy Company: Dutch government DPIA on Microsoft Teams — concluded organizations should not use Teams for sensitive data due to US surveillance access; Teams E2EE is 1:1 only)

## Guides

1. privacyguides.org/en/real-time-communication/ (PrivacyGuides: real-time communication recommendations — Signal, SimpleX, Briar; includes criteria for evaluating secure messengers)
2. signal.org/ (Signal — official website: E2EE messaging and video calls)
3. proton.me/meet (Proton Meet — official page: always-on E2EE video conferencing, MLS protocol, Swiss jurisdiction)
4. jitsi.org/ (Jitsi — official website: open-source video conferencing, self-hostable)
5. brave.com/talk/ (Brave Talk — official page: browser-based private video calls, no login required)

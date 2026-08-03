---
type: "lbr8 Protocol Card"
title: "E2E Messaging"
description: "Use Signal for end-to-end encrypted messaging, voice, and video calls that no one else can read."
tags:
  - "phase-1"
  - "communication"
  - "basic"
  - "p1"
  - "big-tech-surveillance"
  - "govt-surveillance"
  - "data-breach"
---

## Context for the Agent

This card helps the user switch to Signal for end-to-end encrypted messaging, voice, and video calls. Use it when the user wants to stop WhatsApp, iMessage, or SMS from exposing their message content and metadata to surveillance.

## Why This Matters

Your messaging app knows who you talk to, when, how often, and from where. That metadata — not the message content — is what surveillance is built on. An FBI document obtained by Rolling Stone revealed WhatsApp delivers metadata to law enforcement in near-real-time using a pen register — unique among major messaging apps [1]. The Guardian reported that US authorities investigated whistleblower claims that Meta employees and contractors could access WhatsApp message content, though the investigation was abruptly shut down [2]. The EFF found that Meta AI on WhatsApp processes messages outside E2EE, and data is usable for AI training and ad targeting [3]. iMessage encrypts in transit, but Apple retains who-you-messaged logs for 25 days and holds iCloud Backup encryption keys — full message history is available with a warrant. SMS has no encryption at all — carriers see everything and sell metadata to data brokers. Signal collects almost nothing: no content, no contact lists, no metadata beyond your phone number and last connection. It is open source, independently audited, and non-profit.

## Coaching Flow

### Step 1: Install Signal
Guide the user to download Signal from signal.org (not the Play Store — use the official APK or F-Droid). Walk through the setup:
1. Register with their phone number (Signal is phone-number-based)
2. Set a PIN (this encrypts the local database — if the PIN is lost, the database is unrecoverable)
3. Enable "Registration Lock" to prevent SIM swap attacks
4. Set up their profile name and photo (optional — these are E2EE too)

### Step 2: Find and Invite Contacts
Guide the user to:
1. Allow Signal to access contacts (optional — contacts are hashed on-device, never sent to Signal's servers)
2. Signal shows which contacts are already on Signal. If a contact isn't, the user can send them an invite link
3. Suggest they send a message to one contact first to verify everything works

### Step 3: Verify Contacts' Safety Numbers
For high-value contacts (family, legal counsel, journalists), walk the user through verifying safety numbers:
1. Open the conversation → conversation settings → View Safety Number
2. Compare the number in person, via QR code, or via a trusted out-of-band channel
3. Once verified, Signal shows ✅ Verified in the conversation
4. Explain that this protects against man-in-the-middle attacks

### Step 4: Configure Privacy Settings
Walk the user through Signal's privacy settings:
1. **Screen Lock:** Enable within Signal (adds an extra layer of protection)
2. **Screen Security:** Block screenshots in the app's recent apps view
3. **Disappearing Messages:** Set a default timer (1 week recommended — messages auto-delete after expiry)
4. **Sealed Sender:** Enabled by default — hides sender identity from Signal's servers
5. **Always Relay Calls:** Hide IP address during voice/video calls (slightly lower quality, much higher privacy)

### Step 5: Migrate from WhatsApp
Guide the user through the migration:
1. Option A: Inform their contacts via WhatsApp that they are moving to Signal (send a quick message)
2. Option B: Export WhatsApp chat history (WhatsApp → Settings → Chats → Export Chat) and import into Signal (if they want to keep history)
3. Tell them to leave WhatsApp groups and delete their WhatsApp account (not just uninstall — deleting the account removes their data from Meta's servers)
4. For iMessage users: guide them to disable iMessage in Settings → Messages and inform contacts to use Signal

### Step 6: Advanced Option — Molly (Android)
If the user is on Android and wants hardening beyond Signal's defaults, recommend **Molly** (F-Droid). It's a hardened Signal fork with:
- Database encryption (separate passphrase from the PIN)
- Tor routing support
- RAM wiping on lock
- Automatic screen lock on app switch
- Available as Molly-FOSS (no Google services) or Molly-Standard (with Google FCM push)

## Decision Points

The onboarding already knows the user's threat model. Use that:
- **Basic privacy (tracking/ad-targeting):** Standard Signal is sufficient
- **High threat (govt-surveillance, data-breach):** Recommend Molly (Android) with Tor routing, registration lock, disappearing messages set to 1 week, and always relay calls

Ask the user: "Who do you talk to most?" If most of their contacts are on WhatsApp, the migration will require coordination. Suggest they start with their closest contacts and expand gradually.

## Pitfalls

- Signal is only as secure as the people you talk to. If your contact's phone is compromised, your messages to them are exposed. You cannot control other people's security.
- WhatsApp's cloud backups are unencrypted by default. Even if the user switches to Signal, their old WhatsApp messages may still be stored unencrypted on Google Drive or iCloud. Guide them to either delete the backup or replace it with an E2EE backup (WhatsApp now supports E2EE backups — enable it before deleting).
- Signal requires a phone number. For users who need anonymity beyond a phone number, recommend SimpleX Chat or Briar (both are phone-number-free). SimpleX has no user identifiers at all — it uses pairwise addresses.
- Telegram is not E2EE by default. Only "Secret Chats" are encrypted, and they are device-specific (no multi-device sync). Most Telegram users use cloud chats, which are not encrypted. Do not recommend Telegram as a privacy tool.
- If the user's phone is seized or stolen, disappearing messages (if enabled) will have already deleted old messages. If they need this protection, set disappearing messages to 1 week or less.

## Sources

1. rollingstone.com/politics/politics-features/whatsapp-imessage-facebook-apple-fbi-privacy-1261816/ — Rolling Stone: FBI "Lawful Access" document obtained via FOIA reveals WhatsApp delivers metadata to law enforcement every 15 minutes via pen register — unique among major messaging apps
2. theguardian.com/technology/2026/jan/31/us-authorities-reportedly-investigate-claims-that-meta-can-read-encrypted-whatsapp-messages — The Guardian: US Commerce Department investigation into whistleblower claims that Meta employees and contractors could access WhatsApp message content — investigation was abruptly shut down
3. eff.org/deeplinks/2025/09/what-whatsapps-advanced-chat-privacy-really-does — EFF: Meta AI on WhatsApp processes messages outside E2EE — data usable for AI training and ad targeting; WhatsApp metadata collection creates "serious concerns" as ads and AI features expand

## Guides

1. privacyguides.org/en/real-time-communication/ — PrivacyGuides: real-time communication recommendations — Signal, Molly, SimpleX Chat, Briar; criteria: open-source clients, E2EE by default, forward secrecy, independent audit; does not recommend Telegram or WhatsApp
2. signal.org/docs/ — Signal: official documentation — Sealed Sender, private groups, usernames, security model
3. eylenburg.github.io/im_comparison.htm — Eylenburg: instant messenger comparison table — 12 messengers with encryption, federation, metadata, and privacy feature analysis
4. molly.im — Molly: hardened Signal client for Android — database encryption, Tor routing, RAM wiping
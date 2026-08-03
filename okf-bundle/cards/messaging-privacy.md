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
related:
  - "cards/phone-degoogling.md"
  - "cards/privacy-browser.md"
  - "cards/google-privacy-settings.md"
  - "cards/digital-minimalism.md"
---

## Why

Your messaging app knows who you talk to, when, how often, and from where. That metadata — not the message content — is what surveillance is built on. As former NSA Director Michael Hayden put it: "We kill people based on metadata."

**WhatsApp** uses the Signal Protocol for content encryption, but everything around it is exposed. An FBI document obtained by Rolling Stone revealed WhatsApp delivers metadata to law enforcement in near-real-time — unique among major messaging apps. Cloud backups (on by default) store full message content unencrypted on Google Drive or iCloud, accessible with a warrant to Google or Apple. Meta AI chats aren't E2EE and feed ad targeting across Facebook and Instagram.

**iMessage** encrypts in transit, but Apple retains who-you-messaged logs for 25 days and holds iCloud Backup encryption keys — full message history available with a warrant.

**SMS** has no encryption. Carriers see everything and sell metadata to data brokers without warrants.

**Signal** collects almost nothing. No content, no contact lists, no metadata beyond your phone number and last connection. Sealed Sender encrypts sender identity. Open source, audited, non-profit. When served with a warrant, Signal has almost nothing to hand over.

## Steps

### General

**Signal** (signal.org) — the only recommendation for most people. Free, open source, non-profit. E2E encryption for messages, voice, and video. Available on Android (Play Store or F-Droid via Signal-Android build), iOS (App Store), and Desktop (linked to phone). Set up a username and hide your phone number in Settings → Privacy → Phone Number. Enable Sealed Sender for all messages (Settings → Privacy → Advanced). Enable disappearing messages by default for sensitive conversations.

**Migrating your contacts:** Install Signal, let it sync your contacts, then invite key people. Signal lets you message anyone who has Signal — you don't need to convince everyone at once.

### Android

**Signal** (signal.org) — the standard recommendation. Install from Play Store or F-Droid. Set up a username in Settings → Privacy → Phone Number to hide your number from contacts. Enable Sealed Sender for all messages (Settings → Privacy → Advanced).

For extra hardening, **Molly** (molly.im) is a drop-in replacement for Signal on Android with additional security features: local database encryption with a passphrase, RAM wiping, Tor routing, and automatic locking. Uses the same Signal network — your contacts don't need to switch. Recommended if your threat model includes targeted attacks or device seizure.

### iOS

Signal on iOS is the standard. No Molly equivalent on iOS — use the official Signal app. Go to Settings → Privacy → Sealed Sender → turn on "All" to encrypt sender metadata for everyone, not just contacts.

### Desktop

Signal Desktop (signal.org/download) links to your phone as a secondary device. Messages are stored locally in an encrypted SQLite database. Desktop does not independently connect to the Signal server — it mirrors conversations from your phone. For maximum security, disable "Link and sync" on desktop and only use it for active conversations.

## Going Further

**Telegram is not a private messenger**
Telegram does not use end-to-end encryption by default. Regular chats are client-to-server encrypted — Telegram can read them, and has handed over data to authorities. "Secret chats" with E2EE must be manually enabled per conversation, don't sync across devices, and aren't available in group chats. Telegram collects phone numbers, contact lists, IP addresses, and usage data. If you need Telegram for a community, treat it as a public forum, not a private channel.

**Cloud backups are the weakest link**
Even with Signal, if your phone backs up to Google Drive or iCloud, metadata about your Signal usage (timestamps, contacts, message previews in notifications) may be accessible to law enforcement through a warrant to Google or Apple. Disable cloud backup of messaging data, or encrypt your device backup locally.

**When Signal isn't enough**
Signal requires a phone number to register. If your threat model requires anonymity (no phone number at all), consider **SimpleX Chat** (no identifiers whatsoever — no phone numbers, no usernames, contacts via QR code or invite link) or **Briar** (peer-to-peer over Tor, no central server). Both are recommended by PrivacyGuides. For group chat replacing Slack/Discord, **Matrix with Element** offers E2EE chat rooms on a federated network.

**Notification databases**
Even deleted Signal messages can survive in your phone's notification database. A 404 Media investigation showed the FBI extracting deleted Signal messages from an iPhone's notification log. Set Signal notifications to show "Message" only (no content preview) in Signal Settings → Notifications.

## Sources

1. rollingstone.com/politics/politics-features/whatsapp-imessage-facebook-apple-fbi-privacy-1261816/ (Rolling Stone: FBI "Lawful Access" document obtained via FOIA reveals WhatsApp delivers metadata to law enforcement every 15 minutes via pen register — unique among major messaging apps — while iMessage lookup logs and iCloud backups expose who you message and full message content)
2. theguardian.com/technology/2026/jan/31/us-authorities-reportedly-investigate-claims-that-meta-can-read-encrypted-whatsapp-messages (The Guardian: US Commerce Department investigation into whistleblower claims that Meta employees and contractors could access WhatsApp message content — investigation was abruptly shut down; Meta denies the allegations)
3. eff.org/deeplinks/2025/09/what-whatsapps-advanced-chat-privacy-really-does (Electronic Frontier Foundation: Meta AI on WhatsApp processes messages outside E2EE — data usable for AI training and ad targeting; WhatsApp metadata collection creates "serious concerns" as ads and AI features expand)

## Guides

1. privacyguides.org/en/real-time-communication/ (PrivacyGuides: real-time communication recommendations — Signal, Molly, SimpleX Chat, Briar; criteria: open-source clients, E2EE by default, forward secrecy, independent audit; does not recommend Telegram or WhatsApp)
2. signal.org/docs/ (Signal: official documentation — Sealed Sender, private groups, usernames, security model)
3. eylenburg.github.io/im_comparison.htm (Eylenburg: instant messenger comparison table — 12 messengers with encryption, federation, metadata, and privacy feature analysis)
4. molly.im (Molly: hardened Signal client for Android — database encryption, Tor routing, RAM wiping)

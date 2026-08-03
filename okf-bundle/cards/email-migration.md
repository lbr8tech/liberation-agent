---
type: "lbr8 Protocol Card"
title: "Private Email"
description: "Move from Gmail or Outlook to an encrypted email provider that never scans or profits from your messages."
tags:
  - "phase-2"
  - "identity"
  - "intermediate"
  - "p2"
  - "big-tech-surveillance"
  - "tracking"
  - "data-breach"
related:
  - "cards/email-aliasing.md"
---

## Context for the Agent

This card is for users who want to move away from Gmail, Outlook, or other surveillance-based email providers to an encrypted alternative. Use it when the user expresses concern about email scanning, ad targeting, or data mining of their inbox.

## Why This Matters

Your email inbox is a map of your life — every account, contact, purchase, and conversation. Google was caught scanning student emails for ad targeting [1][2], fined €325M by France for inserting ads disguised as emails [3], and faces a class action for secretly enabling Gemini AI to read all Gmail content [4]. The new Outlook transmits IMAP/SMTP credentials to Microsoft cloud servers and shares data with 801 third parties [5][6]. A technical analysis found that Outlook acts as a MITM between your device and your email provider — Microsoft servers log into your email, not your local client [7].

## Coaching Flow

### Step 1: Choose a provider
The user's device type is known from onboarding. Guide them to the best fit:
- **Proton Mail** (free tier available): Swiss jurisdiction, PGP-based encryption, Bridge for desktop clients on paid plans. Best for users who want desktop email client access.
- **Tuta** (free tier available): German jurisdiction, post-quantum encryption, native desktop apps, available on F-Droid, encrypted subject lines. For de-Googled Android phones, Tuta is the better choice — it bypasses Google Play Services entirely.

Both offer E2E encryption by default. Share the [Eylenburg comparison](https://eylenburg.github.io/cloud_comparison.htm) [4] for users who want to see 42 providers analyzed across encryption, jurisdiction, and features.

### Step 2: Create the new account
Walk the user through signing up at the chosen provider's website. Both have free tiers that include enough storage for personal use. Remind them to use a strong, unique password (stored in their password manager).

### Step 3: Forward mail from the old account (temporary)
Guide the user to set up forwarding from their old Gmail/Outlook account to the new private email. This is temporary — they should update accounts gradually. Explain:
- Gmail: Settings → Forwarding and POP/IMAP → Add a forwarding address
- Outlook: Settings → Mail → Forwarding
- Once forwarding is set up, they can still access the old account for a transition period

### Step 4: Update accounts gradually
This is the most important step — and the one that takes time. Guide the user to:
1. Use their password manager to identify which accounts use the old email
2. Start with the most important accounts first: banking, utilities, government services, work accounts
3. Update each one to the new private email address
4. Move to secondary accounts over time: shopping, newsletters, social media
5. Keep the old account active (with forwarding) for at least 3-6 months to catch stragglers

### Step 5: When to delete the old account
Only delete the old account after:
- All important accounts have been migrated
- The forwarding period has been running for at least 3 months with no missed emails
- The user has downloaded any data they want to keep (Google Takeout for Gmail)

## Decision Points

Ask the user: **Which email provider are you migrating from?** Gmail vs Outlook vs other determines the forwarding setup. Also ask: **Do you need desktop email client access?** If yes, recommend Proton Mail with Bridge (paid plan). If they only use webmail and mobile, Tuta's free tier may be sufficient.

## Pitfalls

- Warn the user that migration takes time — they should not delete their old account until they're confident everything is migrated.
- Warn that some services (especially older ones) may not accept email aliases or encrypted email addresses — Proton and Tuta both work with standard SMTP.
- Remind the user that email encryption (E2EE) only works between users of the same provider or when both sides use PGP. Most emails sent to Gmail/Outlook addresses will be in-transit encrypted but readable by the recipient's provider.
- Warn that forwarding from Gmail/Outlook creates a copy of all messages on the old server, so it doesn't delete the data — it just gives time to migrate.
- Suggest using a password manager to track which accounts have been updated to the new email.

## Sources

1. [CNIL: Google fined €325M for displaying ads as emails in Gmail without consent, 2025](https://cnil.fr/en/cookies-and-advertisements-inserted-between-emails-google-fined-325-million-euros-cnil)
2. [EFF: FTC complaint against Google for Education for scanning student emails and building advertising profiles](https://eff.org/files/2015/12/01/ftccomplaint-googleforeducation.pdf)
3. [EPIC: Google admits to data-mining student emails in court filings](https://archive.epic.org/2014/03/google-admits-to-data-mining-s.html)
4. [Thele v. Google: class action over Gemini AI scanning Gmail/Chat/Meet without consent, Oct 2025](https://classaction.org/media/thele-v-google-complaint_2.pdf)
5. [Proton: new Outlook shares data with 801 third parties, transmits IMAP/SMTP credentials to Microsoft cloud](https://proton.me/blog/outlook-is-microsofts-new-data-collection-service)
6. [Schneier: new Outlook conducts extensive surveillance, shares data with advertisers](https://schneier.com/blog/archives/2024/04/surveillance-by-the-new-microsoft-outlook-app.html)
7. [Meister Security: technical analysis of new Outlook MITM architecture](https://blog.meister-security.de/new-outlook-the-end-of-email-privacy/)
8. [ZDNET: Google denies but class action alleges Gemini AI scanning of Gmail](https://zdnet.com/article/google-denies-analyzing-your-emails-for-ai-training-heres-what-happened/)

## Guides

1. [Proton Mail — official website](https://proton.me) — E2E encrypted email, Swiss jurisdiction, free tier available
2. [Tuta — official website](https://tuta.com) — E2E encrypted email, German jurisdiction, post-quantum, F-Droid, free tier available
3. [PrivacyGuides: encrypted email recommendations](https://privacyguides.org/en/email/) — Proton Mail, Tuta, Mailbox.org
4. [Eylenburg: cloud, sync & email services comparison](https://eylenburg.github.io/cloud_comparison.htm) — 42 providers with encryption, jurisdiction, and feature analysis
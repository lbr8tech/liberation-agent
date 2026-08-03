---
type: "lbr8 Protocol Card"
title: "Email Aliasing"
description: "Generate unique forwarding addresses for every service so a data breach or leak never exposes your real inbox."
tags:
  - "phase-2"
  - "identity"
  - "intermediate"
  - "p2"
  - "tracking"
  - "data-breach"
  - "ad-targeting"
prerequisites:
  - "cards/email-migration.md"
related:
  - "cards/email-migration.md"
  - "cards/password-manager.md"
---

## Context for the Agent

This card is for users who want to compartmentalize their email identity so a data breach or spam leak never exposes their real inbox. Prerequisite: the user should have migrated to a privacy-first email provider first (see email-migration card). Use this after that migration is complete.

## Why This Matters

Your email address is a universal identifier. Data brokers use it as the primary key to merge your activity across hundreds of services — shopping, social media, finance, health — into a single profile. Hashing doesn't stop this because the same hash is generated from the same email on every service, making cross-service correlation trivial. Email aliasing gives every service a unique forwarding address. If one alias gets spammed or appears in a breach, you burn it — your real address is never exposed. This prevents cross-service correlation, stops spam at the source, and makes it trivially detectable which service sold or leaked your data.

## Coaching Flow

### Step 1: Confirm the user has a private email provider
Check that the user has completed the email-migration card. If they haven't, recommend they do that first. Email aliasing forwards to your real inbox — if that inbox is Gmail or Outlook, Google and Microsoft still see the forwarded content.

### Step 2: Choose an aliasing service
Present the two main options:
- **SimpleLogin** (Proton-owned): 10 aliases free, $30/yr premium for unlimited + custom domains. Browser extension generates aliases in-place on signup forms. Supports anonymous replies. Tight integration with Proton Mail.
- **Addy.io** (open source): More generous free tier (shared-domain aliases). $1/mo Lite removes bandwidth cap + custom domain. PGP encryption on all tiers including free. Catch-all on custom domain.

Both offer mobile apps (Android, iOS) and browser extensions (Firefox, Chrome, Brave). Both support PGP encryption of forwarded mail.

### Step 3: Set up the service
Walk the user through:
1. Sign up for SimpleLogin or Addy.io
2. Install the browser extension
3. Configure it to forward to their new private email address
4. Enable PGP encryption if the provider supports it (recommended for sensitive aliases)

### Step 4: Start using aliases for every new signup
Guide the user on the practice:
- Use the browser extension to generate a new alias on every signup form
- The alias is automatically created and forwarded to their real inbox
- They never enter their real email address on any website

### Step 5: Organize by risk category
Suggest the user organize aliases by risk level:
- **High trust (banking, government):** Use a dedicated alias per service, with PGP encryption enabled
- **Medium trust (shopping, social media):** One alias per service, standard forwarding
- **Low trust (newsletters, free trials, one-time signups):** One alias per service, can be deleted immediately if spammed

### Step 6: For advanced users — custom domain
If the user owns a domain, walk them through setting up a catch-all alias on their custom domain. This lets them use `service@theirdomain.com` for every service — if they ever want to switch providers, they just update the catch-all forwarding rule, not every account.

## Decision Points

Ask the user: **Do you use Proton Mail?** If yes, SimpleLogin is the natural choice (Proton-owned, tight integration). If they use Tuta or another provider, either SimpleLogin or Addy.io works. **Do you own a domain?** If yes, custom domain aliasing is a powerful option — recommend Addy.io's catch-all feature.

## Pitfalls

- Warn the user not to use aliases for services that need to send them verification codes via SMS — aliasing only covers email.
- Warn that some services reject alias domains (especially free shared domains). If this happens, use a custom domain alias instead.
- Remind the user to keep a spreadsheet or note of which alias goes with which service — this is what makes breach detection possible.
- Warn that deleting an alias means losing access to that service's account unless they've updated their email first.
- If the user is on SimpleLogin's free tier (10 aliases), warn them to use them strategically — save them for the most important services.

## Sources

1. privacyguides.org/en/email-aliasing/ — PrivacyGuides: Email Aliasing guide — Comprehensive recommendations for email aliasing services
2. securemailguide.com/posts/email-aliases-privacy/ — Secure Mail Guide: Email aliases and privacy — Technical overview of how aliasing protects against correlation
3. thenewoil.org/en/guides/moderately-important/email-aliasing/ — The New Oil: Email aliasing guide — Practical guide for implementing email aliasing

## Guides

1. simplelogin.io — SimpleLogin — official website — Proton-owned aliasing service, 10 aliases free, browser extension
2. addy.io — Addy.io — official website — Open source aliasing service, generous free tier, PGP on all tiers
3. privacyguides.org/en/email-aliasing/ — PrivacyGuides: Email Aliasing — Service recommendations and setup guide
---
type: "lbr8 Protocol Card"
title: "Digital Footprint Cleanup"
description: "Find and remove personal information from search results, social media, and cached pages."
tags:
  - "phase-2"
  - "identity"
  - "intermediate"
  - "p2"
  - "data-breach"
  - "tracking"
  - "account-takeover"
  - "stalking"
related:
  - "cards/data-broker-opt-out.md"
  - "cards/email-aliasing.md"
  - "cards/loyalty-program-audit.md"
---

## Context for the Agent

This card is for users who want to find and clean up their public-facing digital presence — old accounts, exposed personal info, stale social media, and cached pages. Use it when the user is concerned about what shows up when someone searches their name.

## Why This Matters

Your digital footprint is what shows up when someone searches your name — old social media posts, forum comments, cached web pages, and personal info aggregated across the web. This is the first thing prospective employers, dates, and stalkers check. The EFF's Opt Out October campaign recommends regular self-searching as a baseline privacy practice, because data brokers and advertisers continuously scrape public posts to build profiles [1]. The goal isn't to delete everything — it's intentional curation: keep what serves you, remove what creates risk [2].

## Coaching Flow

### Step 1: Search for yourself
Walk the user through the first step of any digital footprint cleanup:
1. Search their name in Google, DuckDuckGo, and Bing
2. Search in private/incognito mode so results aren't personalized
3. Note down everything that shows up: social media profiles, forum posts, directory listings, news articles, mentions on other sites
4. Also search their phone number, email addresses, and usernames separately

### Step 2: Categorize what you find
Guide the user to sort what they find into three buckets:
- **Keep public:** Professional work — personal website, GitHub repos, published writing, conference talks, LinkedIn profile (with role, education, and professional email only — no home address, phone, or security clearance level)
- **Make private or remove:** Personal details that don't serve a professional purpose — home address, phone number, birthdate, location-tagged photos, old social media with personal info
- **Delete entirely:** Old accounts on services they no longer use, forum posts with identifying info, cached pages that expose personal data

### Step 3: Delete old accounts
Guide the user to **Just Delete Me** [3] — a directory of direct account deletion links organized by difficulty, covering 1,455+ sites. Walk through:
1. Identify all accounts from the search results
2. Visit each service's deletion page
3. Delete accounts that aren't needed
4. For accounts that must be kept (banking, essential services), update the profile to the minimum necessary info

### Step 4: Remove personal info from Google search results
Guide the user to **Google's "Results about you"** tool [4] at myactivity.google.com/results-about-you. This lets them:
- Request removal of personal info (phone, address, email) from Google search results
- Set up proactive monitoring so Google alerts them if new personal info appears

### Step 5: Check for data breaches
Guide the user to **Have I Been Pwned** [5] — enter their email address and phone number to check if they appear in known data breaches. If they do, change passwords on affected accounts and enable 2FA.

### Step 6: Check for username exposure
Guide the user to **WhatsMyName** [6] — it checks where their username exists across 700+ sites. This is useful for finding old accounts they've forgotten about.

### Step 7: Clean up social media
Walk through social media privacy settings:
- Set posts to "friends only" or "private" as appropriate
- Remove location tags from photos
- Remove identifying info from bio/about sections
- Delete old posts that reveal too much
- For sites they want to keep but separate from their real identity, consider creating a pseudonym account

## Decision Points

Ask the user: **What's your primary concern about your digital footprint?** If it's about what employers see, focus on LinkedIn cleanup and Google search removal. If it's about stalker/harassment risk, focus on removing address and phone from all platforms. If it's about data breach exposure, start with Have I Been Pwned.

## Pitfalls

- Warn the user that deletion is not always permanent — cached pages and archives (Wayback Machine) may still have copies.
- Warn that some services make deletion intentionally difficult (Just Delete Me categorizes these by difficulty level).
- Remind the user that they can't delete everything — government records, news articles, and court records are public by law.
- Warn against deleting accounts they still need — make a list of essential services first.
- Remind the user to check for connected accounts before deleting (e.g., "Sign in with Google" or "Sign in with Facebook").
- Suggest using a password manager to track which accounts have been deleted vs. kept.

## Sources

1. eff.org/deeplinks/2025/09/opt-out-october-daily-tips-protect-your-privacy-and-security — EFF: Opt Out October — daily privacy tips including searching for yourself, deleting old accounts, and removing personal info from search engines
2. eff.org/wp/behind-the-one-way-mirror — EFF: Behind the One-Way Mirror — Deep dive into corporate surveillance technology, identifiers, tracking networks, and how profiles are built from mundane data points
3. ssd.eff.org/module/protecting-yourself-social-networks — EFF Surveillance Self-Defense: Protecting Yourself on Social Networks — Privacy settings, data collection by social platforms, keeping identities separate
4. privacyguides.org/articles/2025/06/10/stay-safe-but-stay-connected/ — PrivacyGuides: Stay Safe, but Stay Connected — How to participate online while minimizing traces, pseudonyms, identity separation, metadata removal

## Guides

1. ssd.eff.org/module/how-to-manage-your-digital-footprint — EFF SSD: How to Manage Your Digital Footprint — Comprehensive guide covering self-searching, account deletion, social media cleanup
2. myactivity.google.com/results-about-you — Google: Results about you — Request removal of personal info from search results, proactive monitoring
3. justdeleteme.xyz — Just Delete Me — Directory of direct account deletion links organized by difficulty, 1,455+ sites
4. haveibeenpwned.com — Have I Been Pwned — Check if your email or phone appears in known data breaches
5. whatsmyname.app — WhatsMyName — Check where your username exists across 700+ sites
6. privacyguides.org/en/basics/account-deletion/ — PrivacyGuides: Account Deletion — Tips for finding and deleting old accounts, GDPR erasure rights
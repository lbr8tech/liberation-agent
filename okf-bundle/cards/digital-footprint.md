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

## Why

Your digital footprint is what shows up when someone searches your name — old social media posts, forum comments, cached web pages, and personal info aggregated across the web. This is the first thing prospective employers, dates, and stalkers check. EFF's Opt Out October campaign recommends regular self-searching as a baseline privacy practice, because data brokers and advertisers continuously scrape public posts to build profiles.

The goal isn't to delete everything — it's intentional curation. Keep the professional presence you've built (a personal website, a GitHub portfolio, a LinkedIn profile), remove what creates risk (home address, phone number, location-tagged photos), and separate identities that shouldn't be linked. EFF frames this as data minimization: "focus on specific pieces of information, where they are, and what you can do about them."

## Steps

### General

**What to keep public (intentional sharing)**
Professional work you're proud of: a personal website, GitHub repos, a Codeforces profile, published writing, conference talks. A LinkedIn profile with your role, education, and a professional email — but not your home address, phone number, or security clearance level. The question to ask for each piece of content: does this serve a clear purpose? If yes, keep it. If not, remove it.

**What to make private or remove (risk reduction)**
Personal details that don't serve a professional purpose: home address, phone number, birthdate, family members' names. Old posts with location data, photos taken outside your home, political rants from a decade ago. Make personal social accounts private. View your profiles in an incognito window to see what a stranger sees.

**What to separate (identity compartmentalization)**
EFF recommends keeping different account identities separate — professional, personal, and pseudonymous. Use different usernames, emails, and photos for each. A profile photo that appears on both your LinkedIn and your dating profile links those identities. To check where your usernames overlap across 700+ sites, use WhatsMyName — but see the caveat in Going Further first.

**Step 1: Search for yourself**
Google your name plus variations (nicknames, maiden names, your name + city). Note what comes up on the first 3 pages. Check Bing and DuckDuckGo too — results differ between engines.

**Step 2: Remove personal info from Google results**
Use Google's "Results about you" tool (myactivity.google.com/results-about-you) to request removal of results showing your phone number, home address, email, or government ID numbers. Google will monitor and alert you if new results appear. This removes the result from search — the source page still exists. Contact the website owner to remove it at the source.

**Step 3: Clean up social media**
Audit every social account: review privacy settings, make accounts private where possible, delete old posts with location data or personal details. Check what's publicly visible by viewing your profile in an incognito window. EFF has a dedicated guide on social network privacy settings (see sources).

**Step 4: Find and delete old accounts**
Search your email for "welcome", "verify", "confirm" — these surface forgotten sign-ups. Check haveibeenpwned.com for breach exposure. Use justdeleteme.xyz for direct account deletion links organized by difficulty. Prioritize accounts with your real name, address, or phone number.

## Going Further

**Check where your username exists**
WhatsMyName (whatsmyname.app) checks 700+ websites for a given username. The underlying dataset is open source (github.com/WebBreacher/WhatsMyName, 2,500+★, maintained since 2015). Run your common usernames through it to find accounts you've forgotten about or impersonation attempts.

**Privacy caveat:** The web version is a client-server hybrid — the server queries each site on your behalf, so it sees your IP address and the username you're searching. The project claims no logging, and the open-source code shows no logging mechanism, but you're still handing a third-party server your username plus your IP. Bellingcat also flags tracking cookies on the web version. For maximum privacy, run it locally: clone the GitHub repo and use a CLI wrapper like Sherlock, or use the web version in a browser with tracking protection enabled (Firefox Strict mode) and a VPN.

**Remove cached content**
Even after you delete a page, copies may survive in search engine caches and the Internet Archive (archive.org). For the Archive, email info@archive.org with the specific URL and time period you want excluded. For Google's cache, use the "Remove outdated content" tool in Google Search Console.

**Overwrite before deleting**
Some sites retain your data even after account deletion. Before deleting, overwrite your profile info with fake data — change your name, address, and email to dummy values, then delete. There's no guarantee this works (backups may hold the original), but it increases the chance your real info is purged.

**GDPR right to erasure**
EEA residents can demand data deletion under GDPR Article 17. Read the service's privacy policy for the process — some require filling out forms, emailing a data protection officer, or proving EEA residence. If the service refuses, contact your national Data Protection Authority.

## Sources

1. eff.org/deeplinks/2025/09/opt-out-october-daily-tips-protect-your-privacy-and-security (EFF: Opt Out October — daily privacy tips including searching for yourself, deleting old accounts, and removing personal info from search engines)
2. ssd.eff.org/module/protecting-yourself-social-networks (EFF Surveillance Self-Defense: Protecting Yourself on Social Networks — privacy settings, data collection by social platforms, keeping identities separate)
3. privacyguides.org/articles/2025/06/10/stay-safe-but-stay-connected/ (PrivacyGuides: Stay Safe, but Stay Connected — how to participate online while minimizing traces, pseudonyms, identity separation, metadata removal)

## Guides

1. ssd.eff.org/module/how-to-manage-your-digital-footprint (EFF SSD: How to Manage Your Digital Footprint — comprehensive guide covering self-searching, account deletion, social media cleanup)
2. myactivity.google.com/results-about-you (Google: Results about you — request removal of personal info from search results, proactive monitoring)
3. justdeleteme.xyz (Just Delete Me: directory of direct account deletion links organized by difficulty — 1,455★)
4. haveibeenpwned.com (Have I Been Pwned: check if your email or phone appears in known data breaches)
5. whatsmyname.app (WhatsMyName: check where your username exists across 700+ sites — 2,556★)
6. privacyguides.org/en/basics/account-deletion/ (PrivacyGuides: Account Deletion — tips for finding and deleting old accounts, GDPR erasure rights)

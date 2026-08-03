---
type: "lbr8 Protocol Card"
title: "Data Broker Opt-Out"
description: "Remove your personal data from data broker databases and people-search sites. Free options first."
tags:
  - "phase-2"
  - "identity"
  - "basic"
  - "p2"
  - "data-breach"
  - "tracking"
  - "ad-targeting"
  - "stalking"
related:
  - "cards/digital-footprint.md"
  - "cards/credit-freeze.md"
  - "cards/loyalty-program-audit.md"
---

## Context for the Agent

This card is for users who want to remove their personal information from data broker databases and people-search sites. Use it when the user expresses concern about their personal data being sold, or after completing the digital footprint audit.

## Why This Matters

Data brokers collect, package, and sell your personal information — name, address, phone, relatives, location history — to anyone willing to pay, including advertisers, insurers, law enforcement, and stalkers. The EFF identified 750 registered data brokers operating across US state registries, and found that 43% of California-registered brokers ignore legally-mandated access requests entirely [1][2]. No service can permanently delete you — brokers continually re-scrape public records, so removal is ongoing maintenance, not a one-time fix [3].

## Coaching Flow

### Step 1: Check if the user is a California resident
If the user is a **California resident**, start with **California DROP** (Delete Request and Opt-Out Platform) — the free government-backed deletion platform launched January 2026 under the Delete Act [4]. One request forces all registered data brokers to delete your data. This is the closest thing to a one-click opt-out and costs nothing.

### Step 2: Manual opt-outs (everyone)
For everyone else (or as a supplement to DROP), guide the user to the **Big Ass Data Broker Opt-Out List** (BADBOOL) [6]. This is a community-maintained directory of direct opt-out links for every major broker, organized by priority. It's free, actively maintained, and reaches the same sites a paid service would.

Walk the user through:
1. Start with the highest-priority brokers (people-search sites like Spokeo, Whitepages, BeenVerified, Intelius, MyLife)
2. Each broker's opt-out page is linked directly in BADBOOL
3. Set a recurring reminder to re-check every 3-6 months since brokers repopulate from public records

### Step 3: Optional automation (EasyOptOuts)
If the user finds manual opt-out too time-consuming, recommend **EasyOptOuts** — the PrivacyGuides-recommended paid service at ~$20/year [5]. It's affordable and covers the same ground as the manual approach. But start with free first — most users can cover the major brokers manually in under an hour.

### Step 4: Also cover telemarketing and credit opt-outs
If the user is getting spam calls or credit offers, guide them to the Griffin Boyce data broker opt-out list [7] which covers telemarketing, direct mail, and credit offer opt-outs.

## Decision Points

Ask the user: **Are you a California resident?** If yes, use DROP as the primary method. Otherwise, BADBOOL manual opt-outs are the way to go. If they're short on time, offer EasyOptOuts as a paid alternative.

## Pitfalls

- Warn the user that this is **ongoing maintenance**, not a one-time fix. Brokers continuously re-scrape public records. Set a 3-6 month reminder to re-check.
- Warn that DROP only works for California residents — don't confuse it with a universal solution.
- Warn that some broker opt-out pages are intentionally hard to find or require email verification. The BADBOOL list includes specific instructions for each.
- Remind the user that opting out doesn't delete government records (voter registration, property records) — those are public by law and can only be restricted, not removed.

## Sources

1. eff.org/deeplinks/2025/06/why-are-hundreds-data-brokers-not-registering-states — EFF: 750 data brokers identified across state registries, hundreds failing to register — Analysis with Privacy Rights Clearinghouse
2. eff.org/deeplinks/2025/08/data-brokers-are-ignoring-privacy-law-we-deserve-better — EFF: 43% of California data brokers ignore legally-mandated access requests — UC Irvine research
3. eff.org/wp/behind-the-one-way-mirror — EFF: Behind the One-Way Mirror — Deep dive into corporate surveillance technology, data brokers, real-time bidding, and how trackers link data to people

## Guides

1. privacyguides.org/en/data-broker-removals/ — PrivacyGuides: Data Removal Services — Manual opt-out links, EasyOptOuts recommendation, vetting criteria
2. github.com/yaelwrites/Big-Ass-Data-Broker-Opt-Out-List — BADBOOL: Big Ass Data Broker Opt-Out List — Community-maintained directory of direct opt-out links for every major data broker, free, organized by priority
3. github.com/glamrock/data-brokers — Griffin Boyce: data broker opt-out list — Telemarketing, direct mail, and credit offer opt-outs
4. oag.ca.gov/privacy/drop — California DROP: free government-backed deletion request platform
5. privacyrights.org/data-broker-registry — Privacy Rights Clearinghouse: data broker registry — Searchable data broker registry across all state registries
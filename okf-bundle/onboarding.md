---
type: lbr8 Onboarding Protocol
title: "Liberation Agent Onboarding Quiz"
description: "Questions the agent asks to assess the user's threat model, platform, budget, and goals. Maps answers to card selections. The agent curates the card list — the user does not pre-select cards."
tags: [onboarding, lbr8, protocol]
---

# Liberation Agent Onboarding Quiz

Ask these questions conversationally — not as a form. One at a time, in a natural flow. The goal is to build a personalized checklist of cards from this bundle that match the user's situation.

The user downloaded the complete bundle — they did not pre-select cards. It is your job to understand their situation and curate the right cards in the right order. This quiz is your curation tool.

Skip any question the user has already answered unprompted. If they seem impatient, use the fast path (questions 1-3 only) and fill in the rest as you go.

## Questions

### 1. What devices do you use day-to-day?

**Why:** Determines which platform instructions to show. Most cards have Android, iOS, and desktop variants.

**Ask:** "What devices do you use? Android phone, iPhone, Windows, Mac, Linux?"

**Map:**
- Android → tag `android`, include cards with Android steps
- iOS → tag `ios`, include cards with iOS steps
- Windows/Mac/Linux → tag `desktop`, include cards with desktop steps

### 2. What's your budget for privacy tools?

**Why:** Some cards recommend paid services (VPN, email aliasing, data broker removal). Calibrates recommendations.

**Ask:** "Are you looking for free solutions only, or are you open to paid services? If paid, what's your annual budget?"

**Map:**
- Free only → de-prioritize cards where the best option is paid (data-broker-opt-out, vpn-basics). Lead with free alternatives.
- Under $50/yr → include vpn-basics, email-aliasing. Note costs.
- Under $200/yr → include all paid-service cards. Note costs.
- Whatever it takes → include all cards. Still lead with free first per editorial voice.

### 3. What are your goals?

**Why:** The core question. Determines which card sets to include.

**Ask:** "What are you trying to achieve? For example: stop being tracked online, protect your identity, take control of your phone, communicate privately, self-host your services?"

**Map answers to card categories:**
- "Stop tracking" / "ads" / "Google" → browser-search, quick-wins, identity-accounts
- "Protect my identity" / "data brokers" / "people finding me" → identity-accounts, data-broker-opt-out, digital-footprint
- "Private messaging" / "secure calls" → communication
- "Take control of my phone" / "degoogling" / "bloatware" → device-liberation, quick-wins
- "Home network" / "router" / "IoT" → home-network
- "Self-host" / "my own server" / "own my data" → self-hosting-101 (or self-hosting-advanced if they already self-host basics)
- "AI" / "local LLM" / "my own assistant" → personal-ai
- "Everything" / "all of it" → include all card sets
- Unsure → include quick-wins and identity-accounts as a starting point

### 4. How much time can you invest right now?

**Why:** Determines which phases to prioritize. Phase 0 cards take 5 minutes. Phase 4+ takes a weekend.

**Ask:** "How much time do you have to spend on this today? A few minutes, a few hours, a weekend?"

**Map:**
- A few minutes → Phase 0 cards only (notification-audit, google-privacy-settings, permissions-audit, etc.)
- A few hours → Phase 0-2 cards (adds app installs, account setup, email migration)
- A weekend → Phase 0-4 cards (adds home network, first self-hosting)
- Ongoing → All phases. Build the full roadmap.

### 5. Do you have a server or spare hardware?

**Why:** Determines whether self-hosting cards are actionable or aspirational.

**Ask:** "Do you have a server, NAS, Raspberry Pi, or spare computer you could run services on?"

**Map:**
- Yes → include self-hosting-101, self-hosting-advanced, data-media
- No → exclude self-hosting cards. Mention them as future options if the user gets hardware later.
- Maybe / not sure → include self-hosting-101 but flag that it requires hardware. Mention Raspberry Pi as a low-cost entry point.

## Building the Checklist

After gathering answers:

1. **Collect matching cards** from the bundle based on the mappings above
2. **Sort by phase** (0 first, 6 last)
3. **Cap the first pass at 5-8 cards** — don't overwhelm
4. **Present as a numbered list:** "Here's your starting checklist. We'll go through these one at a time."
5. **Start with the lowest-phase card**

If the quiz produced fewer than 5 cards, that's fine. Quality over quantity.

## Fast Path

If the user seems impatient or just wants to get started:

1. Ask only: "What devices do you use, and what's your main privacy concern?"
2. Pick 3-5 cards from phase 0-2 that match
3. Start immediately with the first card

You can always adjust the checklist later as you learn more about their situation.

## What Not to Do

- Don't ask all 5 questions before starting. Ask 1-3, build a starter checklist, and refine as you go.
- Don't include more than 8 cards in the first pass. Overwhelm kills momentum.
- Don't skip the disclaimer (see SKILL.md) before starting onboarding.
- Don't ask about threat models directly. Most users don't know what a threat model is. Infer it from their goals.
- Don't let the user pre-select cards. The whole point is that you curate based on their situation. If they ask "which cards should I pick?", say "tell me about your setup and goals and I'll figure that out for you."

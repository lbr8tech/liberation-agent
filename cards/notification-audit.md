---
type: "lbr8 Protocol Card"
title: "Notification Audit & Reduction"
description: "Go through every app and disable all notifications except direct messages."
tags:
  - "phase-0"
  - "devices"
  - "basic"
  - "p0"
  - "digital-minimalism"
  - "ad-targeting"
---

## Context for the Agent

This card is about reducing notification noise across all apps. Use it when the user wants to regain control of their focus and stop being pulled into apps by interruptive alerts.

## Why This Matters

Notifications are designed to keep you addicted and distracted, not to inform you. Every ping is a dopamine loop that fractures your attention — and apps have no incentive to limit themselves. Tristan Harris calls this a "race to the bottom of the brain stem" [1]. The fix is simple: allow only direct messages from real people, and silence everything else.

## Coaching Flow

### Step 1: Define what stays and what goes
Tell the user the rule: only direct, person-to-person messages from real people get through. Everything else — marketing, news, social likes, recommendations, game invites, delivery updates — gets turned off. Ask them to name the messaging apps they consider essential (Signal, SMS, WhatsApp, etc.) and note that social apps (Instagram, Facebook, TikTok, X) do not count as messaging for this purpose.

### Step 2: Walk through the settings per platform
- **Android**: Guide them to Settings → Notifications → App notifications. Show them how to toggle off everything except their core messaging apps. For Android 8.0+ (Oreo), mention that they can go deeper: tap an app, then use notification channels to disable only "Marketing" or "Promotional" types while keeping "Direct messages" — this is especially useful for apps like Amazon or eBay where you want order confirmations but not deal alerts.
- **iOS**: Guide them to Settings → Notifications → [app name]. Tell them to toggle off "Allow Notifications" for every app except their messaging essentials. Note that iOS does not offer per-category notification channels like Android, so it's all-or-nothing per app.

### Step 3: Handle the hard cases
Walk through apps that are tricky:
- **Email clients**: Allow notifications only for VIP/senders they actually want to hear from immediately. Most email apps support per-account or per-folder notification rules.
- **Calendar/reminder apps**: These are legitimate — keep them on if they need them.
- **System apps**: Phone calls, alarms, and calendar alerts are fine. System updates and "tips" can be turned off.

### Step 4: Review and commit
Ask them to spend 10 minutes going through every single app on their phone. Open the notification settings list and scroll from top to bottom — no skipping. Tell them not to worry about missing something important; they can always re-enable a specific app's notifications later.

## Decision Points

No onboarding-level questions required — the agent already knows the user's platform. The only fork is if the user mentions a specific app category they're unsure about (e.g., "what about my banking app?"). For banking, suggest keeping only transaction alerts and turning off marketing/promotions.

## Pitfalls

- **"I'll miss something important"** — Reassure the user that critical alerts (alarms, calls, calendar) are separate from app notifications. They can always toggle a specific app back on.
- **Notification channels on Android** — Many users don't know about per-app channels. Point this out for Android users; it's the best feature for selectively keeping useful notifications while killing noise.
- **Social media direct messages** — If the user keeps Instagram DMs on, remind them that Instagram still sends non-DM notifications (suggestions, "X is live") unless they use notification channels to keep only DMs.
- **iOS limits** — Warn iOS users that they can't finely filter within an app like Android can. For apps like Instagram, they'll have to choose between all notifications or none.

## Sources

1. digitalwellbeing.org/googles-internal-digital-wellbeing-presentation-transcript-and-slides (Tristan Harris: A Call to Minimize Distraction and Respect Users' Attention)

## Guides

1. developer.android.com/develop/ui/compose/notifications/channels (Android Developer Docs: Notification Channels)
2. support.apple.com/en-us/108781 (Apple Support: Use notifications on iPhone)
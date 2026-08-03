---
type: "lbr8 Protocol Card"
title: "Agent-Mediated Reflection"
description: "Complete a nightly AI-guided survey that surfaces patterns and connects your thoughts and reflections across days."
tags:
  - "phase-5"
  - "agent"
  - "advanced"
  - "p5"
  - "big-tech-surveillance"
  - "agency-loss"
prerequisites:
  - "cards/personal-ai.md"
  - "cards/note-taking.md"
related:
  - "cards/agent-planning.md"
  - "cards/agent-routines.md"
  - "cards/attention-audit.md"
draft: true
---
> ⚠️ **This card is a work in progress.** It has not been reviewed for accuracy or completeness. Use at your own risk — verify any recommendations against primary sources before acting on them.


## Steps

### General

Your AI agent conducts a structured evening survey and processes your responses into an interlinked thought wiki.
- Every night at a scheduled time, the agent asks 5 questions via Telegram: (1) recap of the day, (2) mood/reflections, (3) gratitude, (4) long-term goals check-in, (5) thought capture (anything on your mind).
- Responses are saved to a git-tracked, interlinked wiki (Substrate/thought-wiki). The agent processes raw responses into structured pages — identifying themes, cross-referencing with past entries, tracking how your thinking evolves over time.
- The agent tracks thought progression across sessions — it can surface patterns ("you've mentioned X three times this week" or "you felt differently about Y last month").
- Trade-off: Requires a running agent + Telegram. The data is deeply personal — it stays on your infrastructure, never sent to a third party. The agent is a guide, not a therapist — it asks questions and reflects, but does not diagnose.
- Why this is different from a journaling app: The agent reads your entries, connects them to past reflections, and surfaces patterns you wouldn't see yourself. It's a thinking partner, not a blank page.

## Self-Hosted

Hermes Agent nightly-survey skill — 5-question evening survey via Telegram, saved to Substrate

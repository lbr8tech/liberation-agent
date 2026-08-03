---
type: "lbr8 Protocol Card"
title: "Agent-Mediated Planning"
description: "Have your AI agent draft a structured daily plan from your calendar and tasks, then track your follow-through."
tags:
  - "phase-5"
  - "agent"
  - "advanced"
  - "p5"
  - "agency-loss"
  - "attention-fragmentation"
prerequisites:
  - "cards/personal-ai.md"
  - "cards/calendar-contacts.md"
  - "cards/task-management.md"
related:
  - "cards/agent-routines.md"
  - "cards/agent-reflection.md"
  - "cards/attention-audit.md"
---

## Steps

### General

Your AI agent reviews tomorrow's landscape and drafts a structured day plan for your approval.
- Evening: Agent reviews calendar (Baikal/CalDAV), task backlog (Vikunja), carryover from today, and any scheduled events. Drafts a structured plan with time blocks, priorities, and estimated durations. Delivered via Telegram for review before sleep.
- Morning: Agent confirms or adjusts the plan based on any overnight changes, starts execution tracking.
- The plan is a living document — the agent tracks compliance throughout the day and surfaces drift ("you planned to work on X at 2pm but you're watching YouTube instead").
- Trade-off: Requires a running agent (Hermes Level 2+), calendar and task integrations. The agent mediates but does not decide — you approve the plan, it holds you accountable.
- Why this is different from a reminder app: The agent understands context, can reprioritize when things change, and tracks whether you actually followed through — not just whether you dismissed the notification.

## Self-Hosted

Hermes Agent daily-planning skill — evening review + morning confirmation cycle

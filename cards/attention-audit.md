---
type: "lbr8 Protocol Card"
title: "Attention Self-Audit & Review"
description: "Cross-reference DNS logs and application activity data to detect attention patterns, variable reward loops, and drift."
tags:
  - "phase-5"
  - "agent"
  - "advanced"
  - "p5"
  - "attention-fragmentation"
  - "variable-reward-loops"
  - "agency-loss"
prerequisites:
  - "cards/personal-ai.md"
  - "cards/dns-blocking.md"
  - "cards/timed-dns-blocking.md"
related:
  - "cards/agent-planning.md"
  - "cards/agent-reflection.md"
draft: true
---
> ⚠️ **This card is a work in progress.** It has not been reviewed for accuracy or completeness. Use at your own risk — verify any recommendations against primary sources before acting on them.


## Steps

### General

Your AI agent cross-references application usage and DNS queries to detect attention patterns and variable reward loops.
- ActivityWatch: Open-source, self-hosted activity tracker. Runs on each device (laptop, phone). Records which app/window is in focus, idle/active state, and browser tab focus. No data leaves the device.
- AdGuard DNS logs: Your self-hosted DNS blocker logs every DNS query from every device on your network.
- The agent cross-references these two data sources to detect patterns: "You checked Reddit 12 times today, averaging 2 minutes per visit — that's a variable reward loop" or "You opened YouTube during your planned work block."
- Daily report delivered to a dedicated Telegram thread. The agent identifies specific loops, quantifies time cost, and suggests targeted DNS blocks (see timed-dns-blocking card).
- Trade-off: Requires ActivityWatch on each device + self-hosted AdGuard + a running agent. The data is surveillance of yourself, by yourself — the point is to make the invisible visible, then act on it.
- Why this is different from screen time: The agent doesn't just show you a number — it interprets the pattern, names the loop, connects it to your planned schedule, and can take action (block the service) with your approval.

## Self-Hosted

Hermes Agent activity-agent skill — ActivityWatch + AdGuard DNS cross-referencing

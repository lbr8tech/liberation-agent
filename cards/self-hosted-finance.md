---
type: "lbr8 Protocol Card"
title: "Self-Hosted Finance Management"
description: "Self-host Firefly III to track budgets, expenses, and investments without sending your financial data to third parties."
tags:
  - "phase-4"
  - "data"
  - "intermediate"
  - "p4"
  - "big-tech-surveillance"
  - "data-breach"
prerequisites:
  - "cards/file-sync.md"
  - "cards/backup-strategy.md"
related:
  - "cards/personal-ai.md"
draft: true
---
> ⚠️ **This card is a work in progress.** It has not been reviewed for accuracy or completeness. Use at your own risk — verify any recommendations against primary sources before acting on them.


## Steps

### General

Self-hosted personal finance manager with automatic transaction import.
- Firefly III: PHP/Laravel app, Docker deployment. Tracks accounts, budgets, categories, rules engine for auto-categorization. Supports double-entry bookkeeping. Full API.
- SimpleFIN: Bridges bank accounts to Firefly III via OFX/CSV import. No bank credentials stored by third parties — you run the bridge yourself.
- Agent integration: Hermes finance-agent skill provides natural language queries ("How much did I spend on food last month?"), weekly summaries, and automated reconciliation via the Firefly III API.
- Trade-off: Requires a running server and initial bank feed configuration. Data stays on your infrastructure — no third-party sees your spending patterns.
- Note: Firefly III does not connect to banks directly. SimpleFIN or manual CSV/OFX import is required for automatic transaction sync.

## Self-Hosted

Firefly III (self-hosted budgeting + expense tracking) + SimpleFIN (bank transaction import)

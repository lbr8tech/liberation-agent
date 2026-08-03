---
type: "lbr8 Protocol Card"
title: "Self-Hosted Meal & Recipe Planning"
description: "Self-host Mealie to manage recipes, plan meals, and generate shopping lists from your own pantry inventory."
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

Self-hosted recipe manager with meal planning, shopping lists, and pantry tracking.
- Mealie: Python/Docker, web UI. Import recipes from any URL with a single click (scrape and parse automatically). Meal planning calendar, shopping list generation, pantry inventory with on-hand flags.
- Agent integration: Hermes food-agent skill provides natural language queries ("What can I make with what I have?"), meal suggestions based on pantry contents, automated shopping list generation, and neighborhood restaurant guidance.
- API: Full REST API for recipes, meal plans, shopping lists — agent can read, create, and modify entries programmatically.
- Trade-off: Requires a running server. Recipe scraping may need manual fixes for some sites. No integration with online grocery ordering (by design — that would send your data to a third party).

## Self-Hosted

Mealie (self-hosted recipe manager + meal planning)

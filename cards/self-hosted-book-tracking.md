---
type: "lbr8 Protocol Card"
title: "Self-Hosted Book Tracking"
description: "Self-host BookWyrm to track your reading and reviews with ActivityPub federation, outside Goodreads or Amazon."
tags:
  - "phase-4"
  - "data"
  - "intermediate"
  - "p4"
  - "big-tech-surveillance"
  - "tracking"
  - "data-breach"
prerequisites:
  - "cards/file-sync.md"
  - "cards/backup-strategy.md"
related:
  - "cards/personal-ai.md"
---

## Steps

### General

Self-hosted book tracking with reading lists, reviews, and ActivityPub federation.
- BookWyrm: Python/Django, Docker. Import from Goodreads/StoryGraph CSV. Track reading status (to-read, reading, finished), rate and review books, organize into shelves/lists.
- Federation: BookWyrm speaks ActivityPub — your reviews and reading activity can be shared with other BookWyrm instances (or kept private). You control what's shared.
- Agent integration: Hermes books-agent skill provides natural language queries ("What did I think of X?", "What's on my to-read shelf?"), reading recommendations based on history, and bulk import/export.
- API: REST API for programmatic access to your library.
- Trade-off: Smaller community than Goodreads. Book metadata from OpenLibrary (free, community-maintained) — less complete than Amazon for some books. Federation is optional — runs fully standalone.

## Self-Hosted

BookWyrm (federated, self-hosted book tracking)

---
type: "lbr8 Protocol Card"
title: "Self-Hosted Code Repository"
description: "Self-host Forgejo for private code repositories with issue tracking and CI/CD outside of GitHub."
tags:
  - "phase-4"
  - "data"
  - "intermediate"
  - "p4"
  - "big-tech-surveillance"
  - "data-breach"
  - "vendor-lockin"
prerequisites:
  - "cards/file-sync.md"
  - "cards/backup-strategy.md"
related:
  - "cards/personal-ai.md"
---

## Steps

### General

Self-hosted git repository hosting with web UI, issue tracking, and CI/CD.
- Forgejo: Go binary, single Docker container, very low resource footprint. Web UI for browsing code, managing issues, pull requests, and wiki. Built-in CI/CD via Forgejo Actions (GitHub Actions-compatible).
- Agent integration: Hermes forgejo-workflow skill provides repo creation via API, remote management, and commit verification — all programmatically through the agent.
- API: Full REST API compatible with Gitea — works with existing tooling (helm, tea CLI, etc.).
- Migration: `git remote add` your existing repos and push. Import from GitHub via API or mirroring.
- Trade-off: No built-in advanced features like GitHub's Codespaces or GitLab's built-in registry. You handle TLS, backups, and access control. But for private repos and personal projects, it's more than sufficient.
- Note: Forgejo is a hard fork of Gitea by the original community after Gitea's corporate acquisition. Use Forgejo, not Gitea, for new deployments.

## Self-Hosted

Forgejo (lightweight, self-hosted git hosting)

Alternatives: Gitea (Forgejo is a hard fork of Gitea — Forgejo is community-governed)

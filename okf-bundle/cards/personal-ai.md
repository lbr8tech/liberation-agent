---
type: "lbr8 Protocol Card"
title: "Private AI"
description: "Use a privacy-preserving AI provider, self-hosted agent, or fully local model instead of data-harvesting cloud AI."
tags:
  - "phase-2"
  - "media"
  - "intermediate"
  - "p2"
  - "big-tech-surveillance"
  - "tracking"
  - "data-breach"
related:
  - "cards/mesh-vpn.md"
  - "cards/dns-blocking.md"
---

## Steps

### General

Three levels of privacy — choose based on your threat model:

**Level 1 — Privacy-first cloud AI (5 min, no setup)**
Switch to a provider that doesn't log, train, or share your data.
- Proton Lumo: Zero-access encryption (even Proton can't read your chats), no logs, no training, EU jurisdiction (not subject to US surveillance orders). Open source. $0 (free tier) or $30/mo (Plus).
- Brave Leo: Built into Brave browser, no account needed, anonymous. Good for quick queries but no memory/persistence.
- Trade-off: Your data still leaves your device (encrypted, but it leaves). You trust the provider's encryption claims.

**Level 2 — Self-hosted agent + private cloud inference (1-2h setup)**
Run your own agent (Hermes) that orchestrates calls to a private inference provider — your data is never stored by the provider, and the agent layer (memory, tools, history) is entirely under your control.
- Hermes Agent (self-hosted) + Synthetic ($30/mo or pay-per-token): OpenAI-compatible API, open-source models (Qwen, GLM, Kimi, Nemotron), never stores prompts/completions, GDPR-compliant. Synthetic is generous — $30/mo flat includes all always-on models, 3x Claude Pro rate limits, no per-token billing on subscription. Or pay-per-token ($0.10–$1.40/M input, $0.10–$4.40/M output).
- Alternatively, route through a TEE-protected gateway (NEAR AI, RedPill, ZeroK Cloud) for cryptographic attestation that your data was never seen — even the operator can't read it. These run open-weight models inside Intel TDX / NVIDIA confidential computing enclaves with hardware-signed proofs.
- For maximum cloud privacy: OpenAI/Anthropic/Google all offer Zero Data Retention (ZDR) on enterprise plans — no logs retained beyond inference. But ZDR requires an enterprise agreement (not self-serve) and still trusts the provider's infrastructure.
- Trade-off: Data leaves your device for inference, but is not stored. Agent memory/history stays on your server. You trust the inference provider's privacy policy, not their encryption (unless using TEE).

**Level 3 — Fully local inference (2-4h setup, requires hardware)**
Run models on your own hardware. Data never leaves the machine. No provider trust required.
- Ollama (CLI, easy model management) or LM Studio (GUI, model browser).
- Hermes Agent + local model (e.g., Qwen 3.6 27B via llama.cpp) — full agent capability with zero network dependency.
- Hardware requirements: 8GB+ RAM for 7B models, 32GB+ for 27B, 64GB+ for 70B. A used GPU (RTX 3060 12GB ~$200) runs 7-13B models well. CPU-only works but is slow.
- Trade-off: No data leaves your machine — maximum sovereignty. But you need the hardware, models are smaller/less capable than frontier cloud models, and you handle your own security (a misconfigured local server is worse than a hardened cloud provider).

**Decision tree:**
- Non-technical, want privacy now → Level 1 (Proton Lumo)
- Technical, want agent capability + memory + privacy → Level 2 (Hermes + Synthetic)
- Technical, want maximum sovereignty, have hardware → Level 3 (Ollama/llama.cpp)
- Adversarial threat model (government targeting) → Level 3 only — no cloud provider is safe against legal compulsion

## Self-Hosted

Hermes Agent + Synthetic (self-hosted orchestration + private cloud inference)

Alternatives: Ollama or llama.cpp (fully local inference), LM Studio (GUI for local models)

## Cloud

Proton Lumo (zero-access encrypted, no logs, no training, EU jurisdiction)

Alternatives: Brave Leo (built into Brave browser, no login required)

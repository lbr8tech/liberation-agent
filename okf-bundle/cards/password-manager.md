---
type: "lbr8 Protocol Card"
title: "Password Manager"
description: "Use Bitwarden to generate, store, and autofill strong passwords and TOTP codes across every device."
tags:
  - "phase-1"
  - "identity"
  - "intermediate"
  - "p1"
  - "data-breach"
  - "account-takeover"
---

## Why

If you reuse a password or variations of one, a single breach cascades to every account sharing that password. A password manager breaks the cascade: every account gets a unique, randomly generated password that you never need to remember. The only password you memorize is the master password that encrypts your vault. Even if a service you use gets breached, the stolen password works nowhere else. Cloudflare's 2024 analysis found 41% of successful logins involve leaked credentials, and Verizon's 2025 DBIR found stolen credentials were the entry point in 22% of all breaches — the problem is not theoretical.

## Steps

### General

Install a password manager on every device — browser extension, mobile app, and desktop. Generate a unique 20+ character password for every account. The only password you memorize is your master password — never reuse it anywhere else. Choose Cloud or Self-Hosted below based on where you want your encrypted vault to live.

## Self-Hosted

<strong>Vaultwarden</strong> (AGPL-3.0, 64,026★) — recommended for experts and technical folks only. Rust reimplementation of the Bitwarden server. Runs on anything from a Raspberry Pi to a VPS. Your encrypted vault never touches a third-party server. Use official Bitwarden clients to connect — the experience is identical to cloud Bitwarden. You are responsible for uptime, backups, TLS certificates, and security updates. If your server goes down, you lose access to every password.

Alternatives: KeePassXC (GPL, 27,859★) — fully offline, no server at all. Stores everything in a single encrypted .kdbx file on your machine. No cloud, no account, no company. Sync the file yourself via Syncthing or USB. Mobile: KeePassDX on Android (F-Droid), Strongbox on iOS. Browser: KeePassXC-Browser extension. The most private option — no server to breach, no subscription to cancel. Trade-off: more manual setup and no built-in sync.

## Cloud

<strong>Bitwarden</strong> (GPL, open source, 13,109★) — recommended for most users. The default choice for ~90% of people. Free tier is genuinely unlimited: unlimited passwords, unlimited devices, unlimited sync. Browser extensions for Firefox, Chrome, Brave, Edge, Safari. Mobile apps with biometric unlock. Audited by Cure53 and ETH Zurich. 8 years without a server breach. Self-hosting a password manager is difficult to do well — if your server goes down, you lose access to every account. Unless you have reliable uptime and a backup strategy, the cloud option is the right call.

Alternatives: Proton Pass (clients open source, Swiss jurisdiction, built-in email aliases — but server is closed and free tier has limits)

**Privacy note:** Your encrypted vault is stored on Bitwarden's servers. Zero-knowledge architecture means they cannot read your passwords, but the server is not under your control.

## Going Further

<strong>Emergency Access</strong>
Bitwarden lets you designate trusted contacts who can request access to your vault in an emergency. If you don't respond within a wait period you choose (e.g. 7 days), they automatically gain access — no shared passwords needed. Set this up under Settings → Emergency Access and add a trusted friend or family member.

<strong>Layer 2: Passkeys</strong>
A passkey replaces the password entirely with a cryptographic key pair. The private key never leaves your device, the public key stored on the server is useless to an attacker, and the credential is cryptographically bound to the website it was created for — phishing becomes structurally impossible. The UK's National Cyber Security Centre recommends passkeys wherever services support them, and NIST SP 800-63B classifies them as phishing-resistant (AAL2). Google reports 99.9% lower compromise rates for passkey accounts vs passwords. Enable passkeys wherever a service offers them (Google, GitHub, Amazon, Microsoft, Apple, most major banks). Bitwarden can store and sync passkeys alongside passwords, so no separate app is needed.

<strong>Layer 3: TOTP (Authenticator App)</strong>
For accounts without passkey support, use a TOTP app to generate 6-digit codes. <strong>Bitwarden Authenticator</strong> (included in the $10/year premium tier) stores TOTP codes in the same vault as your passwords — one app, one unlock. Scan the QR code each service provides under Security → 2FA → Authenticator App. Store backup recovery codes in your vault too. Prefer a separate authenticator app like <strong>Aegis</strong> (Android, F-Droid, 12,658★) only if you want TOTP codes isolated from your password vault — the separation means a compromised master password doesn't also expose your 2FA codes.

<strong>SMS-based 2FA</strong>
SMS 2FA is weaker than passkeys and TOTP — SMS is unencrypted, routed through third-party intermediaries with no security oversight, and vulnerable to SIM swapping. In January 2024, SIM swapping of a single SEC employee's phone number let attackers post from the official @SECGov Twitter account. UK SIM swap fraud rose 1,055% in 2024. That said, SMS 2FA is still better than no 2FA at all — use it if a service offers nothing else, but migrate to passkeys or TOTP the moment they become available.

## Sources

1. blog.cloudflare.com/password-reuse-rampant-half-user-logins-compromised (Cloudflare: 41% of successful human logins involve leaked credentials across 30M websites)
2. verizon.com/business/resources/articles/credential-stuffing-attacks-2025-dbir-research (Verizon 2025 DBIR: stolen credentials = initial access vector in 22% of breaches, only 49% of user passwords are distinct)
3. ncsc.gov.uk/blogs/passkeys-are-more-secure-than-traditional-ways-to-log-in (NCSC: Passkeys are more secure than traditional ways to log in — phishing-resistant by design)
4. arstechnica.com/security/2024/10/how-alleged-sim-swap-and-hacked-x-account-drove-up-price-of-bitcoin-by-1k/ (Ars Technica: SIM swap of SEC account — how SMS 2FA was defeated to hack @SECGov)

## Guides

1. ssd.eff.org/module/creating-strong-passwords (EFF Surveillance Self-Defense: creating strong passwords, using password managers, 2FA, and security questions — the complete guide)
2. github.com/bitwarden/clients (Bitwarden: open-source password manager, audited by Cure53 and ETH Zurich)
3. github.com/dani-garcia/vaultwarden (Vaultwarden: self-hosted Bitwarden-compatible server in Rust)
4. github.com/keepassxreboot/keepassxc (KeePassXC: fully offline, local password manager)
5. github.com/beemdevelopment/Aegis (Aegis: open-source encrypted TOTP authenticator for Android, for users wanting 2FA isolated from password vault)

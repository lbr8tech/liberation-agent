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

## Context for the Agent

This card helps the user set up a password manager to generate and store unique, strong passwords for every account. Use it when the user is ready to stop reusing passwords and wants to protect against credential-stuffing attacks and data breaches.

## Why This Matters

If you reuse a password, a single breach cascades to every account sharing that password. Cloudflare's 2024 analysis found 41% of successful logins involve leaked credentials, and Verizon's 2025 DBIR found stolen credentials were the entry point in 22% of all breaches — only 49% of user passwords are distinct [1][2]. A password manager breaks the cascade: every account gets a unique, randomly generated password you never need to remember. The only password you memorize is the master password that encrypts your vault. Even if a service you use gets breached, the stolen password works nowhere else. Passkeys (supported by Bitwarden) are phishing-resistant by design and eliminate the password entirely for compatible services [3].

## Coaching Flow

### Step 1: Choose Cloud or Self-Hosted
Ask the user: "Do you want your encrypted vault stored on Bitwarden's servers (cloud, no maintenance) or on your own server (self-hosted, full control)?" Most users should choose cloud Bitwarden — it's audited, encrypted end-to-end (not even Bitwarden can read your vault), and requires zero maintenance. For technical users who want to self-host, recommend Vaultwarden (described below). If the user wants no server at all, recommend KeePassXC.

### Step 2: Install Bitwarden on Every Device
Guide the user to install Bitwarden everywhere:
- **Browser extension:** Chrome, Firefox, Brave, Edge — it autofills passwords on login pages
- **Mobile app:** iOS/Android app from F-Droid or Aurora Store (or official app store)
- **Desktop app:** from bitwarden.com or package manager
Walk them through creating an account with a strong email and master password. Emphasize: the master password must be strong, unique, and memorable — write it down on paper and store it somewhere safe. There is no password reset. If you lose it, your vault is gone forever.

### Step 3: Generate and Replace Passwords
Guide the user to start generating new passwords for every account. Walk them through:
1. Use Bitwarden's built-in password generator (20+ characters, uppercase + lowercase + digits + symbols)
2. For each existing account, log in, go to settings, change password, and let Bitwarden generate and save the new one
3. Prioritize high-value accounts first: email, banking, social media, cloud storage, domain registrar
4. Do not rush — this is a gradual process. One or two accounts per day is fine.

### Step 4: Set Up Two-Factor Authentication (TOTP)
Ask the user if they want their TOTP (time-based one-time passwords) in the same vault or separate. If they want convenience, Bitwarden Premium ($10/year) stores TOTP codes alongside passwords and auto-fills them. If they want defense-in-depth (an attacker who compromises the vault cannot access 2FA codes), recommend installing **Aegis** (Android) or using a separate authenticator app. Explain that SMS 2FA is vulnerable to SIM swapping — the 2024 SEC Twitter hack was a SIM swap that defeated SMS 2FA [4].

### Step 5: Enable Passkeys
If the user's accounts support passkeys (Apple, Google, Microsoft, GitHub, PayPal), guide them to enable passkeys in the Bitwarden vault. Passkeys are phishing-resistant by design — they cannot be stolen by a fake login page. They replace passwords entirely for supported services.

### Step 6: Self-Hosted Option (Vaultwarden — Technical Users Only)
If the user chose self-hosted, guide them through:
1. Deploy Vaultwarden on a server they control (Raspberry Pi, VPS, or home server) — official Docker image available
2. Set up TLS (Let's Encrypt) and a domain name
3. Use official Bitwarden clients to connect — the experience is identical to cloud Bitwarden
4. Warn them: they are responsible for uptime, backups, TLS certificates, and security updates. If their server goes down, they lose access to every password.

### Step 7: Fully Offline Option (KeePassXC)
If the user wants no server at all, recommend KeePassXC. It stores everything in a single encrypted .kdbx file on their machine. They sync the file manually (Syncthing, USB, Nextcloud). No cloud, no server, no network. Trade-off: no autofill on mobile, no seamless sync, and they are responsible for backup discipline.

## Decision Points

The onboarding already knows the user's skill level. Use that to determine the recommendation:
- **Beginner:** Cloud Bitwarden, TOTP in Bitwarden
- **Intermediate:** Cloud Bitwarden, TOTP in Aegis (separate)
- **Advanced:** Self-hosted Vaultwarden or KeePassXC, TOTP in Aegis

Ask the user: "Do you want convenience (everything in one place) or defense-in-depth (separate 2FA app)?" If they are concerned about a single point of failure, recommend separating TOTP into Aegis.

## Pitfalls

- The master password is the single point of failure. There is no password reset. Write it down on paper and store it in a safe place (safety deposit box, fireproof safe). Do not store it in a cloud document, a notes app, or a photo.
- Browser-based password managers (Chrome's built-in, Firefox Lockwise) are not encrypted the same way and are tied to your browser profile. If someone gains access to your Google account, they have all your passwords. Always use a dedicated password manager.
- SMS 2FA is vulnerable to SIM swapping. If the user is using SMS 2FA, prioritize moving them to TOTP as soon as possible.
- Cloud Bitwarden is encrypted end-to-end, but some users may still be uncomfortable with any cloud dependency. Respect that and offer the self-hosted or offline option.
- Do not try to migrate every password in one sitting. Coach the user to do a few accounts per day — it's a marathon, not a sprint.

## Sources

1. blog.cloudflare.com/password-reuse-rampant-half-user-logins-compromised — Cloudflare: 41% of successful human logins involve leaked credentials across 30M websites
2. verizon.com/business/resources/articles/credential-stuffing-attacks-2025-dbir-research — Verizon 2025 DBIR: stolen credentials = initial access vector in 22% of breaches, only 49% of user passwords are distinct
3. ncsc.gov.uk/blogs/passkeys-are-more-secure-than-traditional-ways-to-log-in — NCSC: Passkeys are more secure than traditional ways to log in — phishing-resistant by design
4. arstechnica.com/security/2024/10/how-alleged-sim-swap-and-hacked-x-account-drove-up-price-of-bitcoin-by-1k/ — Ars Technica: SIM swap of SEC account — how SMS 2FA was defeated to hack @SECGov

## Guides

1. ssd.eff.org/module/creating-strong-passwords — EFF Surveillance Self-Defense: creating strong passwords, using password managers, 2FA, and security questions — the complete guide
2. github.com/bitwarden/clients — Bitwarden: open-source password manager, audited by Cure53 and ETH Zurich
3. github.com/dani-garcia/vaultwarden — Vaultwarden: self-hosted Bitwarden-compatible server in Rust
4. github.com/keepassxreboot/keepassxc — KeePassXC: fully offline, local password manager
5. github.com/beemdevelopment/Aegis — Aegis: open-source encrypted TOTP authenticator for Android, for users wanting 2FA isolated from password vault
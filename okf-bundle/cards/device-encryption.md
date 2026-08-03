---
type: "lbr8 Protocol Card"
title: "Device Encryption Verification"
description: "Verify encryption is enabled on every device and strengthen your PIN or passphrase against brute-force attacks."
tags:
  - "phase-0"
  - "devices"
  - "basic"
  - "p0"
  - "data-breach"
  - "physical-theft"
  - "govt-surveillance"
related:
  - "cards/password-manager.md"
  - "cards/digital-vault.md"
---

## Context for the Agent

This card is about verifying that device encryption is enabled and strengthening the passphrase that protects the encryption key. Use it when the user wants to ensure their data is protected if their device is stolen or seized.

## Why This Matters

If someone steals or seizes your phone, encryption is the only thing standing between them and your data. But encryption is only as strong as the PIN protecting the encryption key — a 4-digit PIN has only 10,000 combinations. While rate limiting slows on-device guessing, law enforcement tools like Cellebrite and GrayKey exploit vulnerabilities to bypass rate limiting on some devices [1][2]. A longer PIN or alphanumeric passcode significantly increases resistance. For maximum protection, power off your device before border crossings or protests — a powered-off phone is in BFU (Before First Unlock) state, where encryption keys are not in memory. Android 17 further slashes PIN guess attempts from 1,800 to just 20 [3].

## Coaching Flow

### Step 1: Check encryption status
Based on the user's platform, guide them to verify encryption is enabled:
- **Android**: Guide them to Settings → Security & privacy → More security & privacy → Encryption & credentials. Phones have encrypted by default since Android 6.0 (2015), but it's worth verifying.
- **iOS**: Tell them iPhones encrypt by default since iOS 4 (2010) — all data on the flash storage is always encrypted. Data Protection assigns per-file encryption classes based on when the app needs access. Verify at Settings → Face ID & Passcode (or Touch ID & Passcode).
- **Desktop (Windows)**: Guide them to check BitLocker status in Settings → Privacy & Security → Device encryption. If they have Windows 11 Home, only "Device Encryption" is available (weaker). Pro/Enterprise users can use full BitLocker. Warn them: if BitLocker is auto-enabled with a Microsoft account, the recovery key is uploaded to Microsoft's servers. Tell them to store the recovery key locally (USB drive, printed copy) and remove it from their Microsoft account.
- **Desktop (macOS)**: Guide them to System Settings → Privacy & Security → FileVault. Turn it on and store the recovery key locally — NOT in iCloud.
- **Desktop (Linux)**: Tell them LUKS2 is typically set up at install time. It uses the Argon2id KDF, which is the strongest available. If they didn't set it up during installation, they'll need to reinstall.

### Step 2: Strengthen the PIN/passcode
Tell the user to change their screen lock to something stronger:
- **Android**: Guide them to Settings → Security & privacy → Screen lock. A 4-digit PIN has only 10,000 combinations. Recommend at least 8 digits, preferably an alphanumeric passcode. Mention that Android 17 now limits PIN guess attempts to just 20 before the device wipes [3].
- **iOS**: Guide them to Settings → Face ID & Passcode → Change Passcode. Recommend at least 6 digits, preferably alphanumeric. The Secure Enclave enforces escalating delays and wipes after 10 failed attempts.

### Step 3: Explain BFU vs. AFU
Tell the user about the two states of a locked phone:
- **BFU (Before First Unlock)**: The phone was powered off or just restarted. Encryption keys are not in memory. This is the most secure state — forensic tools get the least data.
- **AFU (After First Unlock)**: The phone has been unlocked at least once since boot. Keys are in memory. Forensic tools can extract significantly more data.
- **Practical advice**: If the user is traveling or crossing a border, power off the phone completely. Don't just lock it. If they're in a high-risk situation (protest, arrest), power off before anyone approaches.

### Step 4: Check backup encryption
Cloud backups can bypass device encryption. Guide the user to check:
- **Android**: Google Drive backups may be encrypted with the device PIN or Google account password. Check in Settings → Google → Backup → Backup by Google One.
- **iOS**: iCloud backups can be end-to-end encrypted if Advanced Data Protection is enabled (Settings → Apple ID → iCloud → Advanced Data Protection). Without it, Apple holds the encryption key.

## Decision Points

- **Desktop vs. phone**: The agent knows the user's device type from onboarding. If they have a desktop/laptop, guide them through the desktop-specific steps. Encryption is on by default for phones but NOT for desktops — this is a key distinction.
- **Cloud backup concern**: If the user mentions they care about cloud backup privacy, guide them to the "Digital Vault" card.

## Pitfalls

- **"I have a 4-digit PIN, that's fine"** — It's not. 10,000 combinations is trivially brute-forceable if rate limiting is bypassed. A 6-digit code has 1 million combinations; an 8-digit alphanumeric has quadrillions.
- **BitLocker recovery key in Microsoft account** — Many users don't know this is the default. If someone gains access to their Microsoft account, they get the recovery key too. Store it locally.
- **Cloud backups bypass device encryption** — Even if the phone is encrypted, a cloud backup held by Google or Apple is only as secure as the account password and the provider's encryption practices.
- **Linux LUKS2 is not retroactive** — If the user didn't set up disk encryption at install time, they cannot easily add it later without reinstalling.
- **VeraCrypt for plausible deniability** — If the user needs hidden volumes (you can deny the volume exists), VeraCrypt supports this. LUKS does not.
- **Power off ≠ airplane mode** — Airplane mode stops network communication but the device is still in AFU state. Encryption keys remain in memory. For border crossings, power off completely.

## Sources

1. 404media.co/leaked-docs-show-what-phones-cellebrite-can-and-cant-unlock/ (404 Media: Leaked Cellebrite docs showing which phones can and cannot be unlocked)
2. theverge.com/2024/11/19/24300731/a-major-forensics-tool-is-only-getting-partial-data-from-recent-phones (The Verge: GrayKey forensics tool only getting partial data from recent phones)
3. androidauthority.com/android-17-pin-password-protection-3683166/ (Android Authority: Android 17 slashes PIN guess attempts from 1,800 to just 20)

## Guides

1. ssd.eff.org/module/what-should-i-know-about-encryption (EFF SSD: What should I know about encryption)
2. privacyguides.org/en/encryption/ (PrivacyGuides: Encryption)
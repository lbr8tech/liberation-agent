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

## Why

If someone steals or seizes your phone, the encryption is the only thing standing between them and your data. But encryption is only as strong as the PIN protecting the encryption key — a 4-digit PIN has only 10,000 combinations. While rate limiting slows on-device guessing, law enforcement tools like Cellebrite and GrayKey exploit vulnerabilities to bypass rate limiting on some devices. A longer PIN or alphanumeric passcode significantly increases resistance. For maximum protection, power off your device before border crossings or protests — a powered-off phone is in BFU (Before First Unlock) state, where encryption keys are not in memory.

## Steps

### General

Encryption is on by default on phones, but verify it and strengthen the PIN. The encryption is only as strong as the passphrase protecting the key.

Key points:
- A locked phone is weaker than a powered-off phone (After First Unlock state retains keys in memory)
- For travel/border crossings: power off, don't just lock
- Cloud backups may be unencrypted or encrypted with a provider-held key — check backup encryption settings

### Android

Phones encrypt by default since Android 6.0 (2015). Verify: Settings → Security & privacy → More security & privacy → Encryption & credentials. Set PIN to at least 8 digits, or use an alphanumeric passcode: Settings → Security & privacy → Screen lock. A 4-digit PIN has only 10,000 combinations; while rate limiting slows guessing, forensic tools can bypass it on some devices.

### iOS

iPhones encrypt by default since iOS 4 (2010) — all data on the flash storage is always encrypted. Data Protection assigns per-file encryption classes based on when the app needs access. Verify: Settings → Face ID & Passcode (or Touch ID & Passcode on older devices). Set passcode to at least 6 digits, preferably alphanumeric. The Secure Enclave enforces escalating delays and wipes after 10 failed attempts.

### Desktop

Desktops and laptops do not encrypt by default — you must enable it manually:

- Windows: BitLocker (Pro/Enterprise). On Windows 11, may be auto-enabled with Microsoft account — check if recovery key is uploaded to Microsoft and move it offline. Home edition: "Device Encryption" only.
- macOS: FileVault 2. Enable in System Settings → Privacy & Security. Store recovery key locally, NOT in iCloud.
- Linux: LUKS2 at install time. Harder to add after the fact.

## Sources

1. 404media.co/leaked-docs-show-what-phones-cellebrite-can-and-cant-unlock/ (404 Media: Leaked Cellebrite docs showing which phones can and cannot be unlocked)
2. theverge.com/2024/11/19/24300731/a-major-forensics-tool-is-only-getting-partial-data-from-recent-phones (The Verge: GrayKey forensics tool only getting partial data from recent phones)
3. androidauthority.com/android-17-pin-password-protection-3683166/ (Android Authority: Android 17 slashes PIN guess attempts from 1,800 to just 20)

## Guides

1. ssd.eff.org/module/what-should-i-know-about-encryption (EFF SSD: What should I know about encryption)
2. privacyguides.org/en/encryption/ (PrivacyGuides: Encryption)

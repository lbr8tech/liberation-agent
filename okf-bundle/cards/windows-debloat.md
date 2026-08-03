---
type: "lbr8 Protocol Card"
title: "Windows Debloat & Teardown"
description: "Remove pre-installed bloatware, disable telemetry, kill AI features, and declutter Windows 10/11 with a single script."
tags:
  - "phase-0"
  - "devices"
  - "basic"
  - "p0"
  - "big-tech-surveillance"
  - "tracking"
  - "ad-targeting"
related:
  - "cards/google-privacy-settings.md"
  - "cards/browser-hardening.md"
  - "cards/device-encryption.md"
  - "cards/linux-desktop.md"
---

## Why

Windows is the only operating system that ships with ads on the lock screen, Candy Crush pre-installed, and a search bar that sends your local queries to Bing. Microsoft redesigned its OS around AI — Copilot, Recall, Click to Do — features that screenshot everything you do and process it locally or in the cloud. The original Recall stored screenshots in an unencrypted SQLite database that any malware could read; security researchers called it a "disaster." Even with AI features off, Windows sends diagnostic data to Microsoft: browsing history, app usage, device configuration — used for "tailored experiences," Microsoft's word for targeted ads. In July 2026, an unsealed FBI complaint revealed that every Windows installation has a Global Device Identifier (GDID) — a persistent, server-assigned ID that travels with the OS installation itself, not the network connection. The FBI used it to track a suspect across VPNs, proxy servers, and four countries. A VPN hides your IP; the GDID stitches your sessions together regardless. There is no opt-out. Even a debloated Windows installation reports this identifier to Microsoft. For maximum privacy, the only real answer is Linux.

## Steps

### Desktop

Win11Debloat — a free, open-source PowerShell script (MIT license, 52k+ stars) that removes bloatware and disables telemetry in one run. Works on both Windows 10 and 11.

Quick method (PowerShell):
<pre><code>& ([scriptblock]::Create((irm "https://debloat.raphi.re/")))</code></pre>
Or download from github.com/Raphire/Win11Debloat and run Run.bat as admin.

What it does:
- Removes pre-installed apps (Xbox, Candy Crush, weather, etc.)
- Disables telemetry, diagnostic data, activity history, app-launch tracking, targeted ads
- Removes Microsoft Copilot, Windows Recall, and Click to Do
- Disables AI features in Edge, Paint, and Notepad
- Disables Bing web search and Copilot in Start menu search
- Disables lock screen tips, suggestions, and ads
- Restores Windows 10-style context menu
- Enables dark mode, disables transparency/animations
- Shows file extensions and hidden files
- Disables Find My Device location tracking
- Disables Delivery Optimization (P2P update sharing)

All changes are revertible — removed apps can be reinstalled from the Microsoft Store. Export/import your settings to apply the same config across machines.

Review the script options before running — it presents an interactive menu where you choose what to disable.

This script reduces telemetry and removes AI features, but it cannot remove the GDID or stop all diagnostic data. Windows still reports a persistent device identifier to Microsoft regardless of how many settings you disable. For maximum privacy, migrate to Linux.

## Sources

1. pcmag.com/news/a-hackers-arrest-reveals-microsoft-can-track-users-via-a-windows-device-id (PCMag: Hacker's arrest reveals Microsoft can track users via Windows Global Device ID — FBI used GDID to track suspect across VPNs and 4 countries)
2. ghacks.net/2026/07/12/microsoft-confirms-windows-gdid-device-identifier-that-cannot-be-disabled-documented-in-fbi-case-filing/ (gHacks: Microsoft confirms Windows GDID device identifier that cannot be disabled)
3. theverge.com/2024/6/3/24170305/microsoft-windows-recall-ai-screenshots-security-privacy-issues (The Verge: Windows AI feature that screenshots everything labeled a security disaster — Recall stored screenshots in unencrypted database)
4. arstechnica.com/gadgets/2024/09/microsoft-details-security-privacy-overhaul-for-windows-recall-ahead-of-relaunch/ (Ars Technica: Microsoft details security overhaul for Windows Recall after plain-text database discovery)

## Guides

1. github.com/Raphire/Win11Debloat (Win11Debloat: open-source PowerShell script to remove bloatware and disable telemetry)

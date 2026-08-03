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

## Context for the Agent

This card is about debloating and reducing telemetry in Windows 10/11. Use it when the user is on Windows and wants to remove pre-installed bloatware, disable AI features, and reduce Microsoft's data collection.

## Why This Matters

Windows is the only operating system that ships with ads on the lock screen, Candy Crush pre-installed, and a search bar that sends your local queries to Bing. Microsoft redesigned its OS around AI — Copilot, Recall, Click to Do — features that screenshot everything you do and process it locally or in the cloud. The original Recall stored screenshots in an unencrypted SQLite database that any malware could read; security researchers called it a "disaster" [3][4]. Even with AI features off, Windows sends diagnostic data to Microsoft: browsing history, app usage, device configuration — used for "tailored experiences," Microsoft's word for targeted ads. In July 2026, an unsealed FBI complaint revealed that every Windows installation has a Global Device Identifier (GDID) — a persistent, server-assigned ID that travels with the OS installation itself, not the network connection [1][2]. The FBI used it to track a suspect across VPNs, proxy servers, and four countries. There is no opt-out. Even a debloated Windows installation reports this identifier to Microsoft. For maximum privacy, the only real answer is Linux.

## Coaching Flow

### Step 1: Explain the GDID limitation
Before the user invests time, be upfront: debloating reduces telemetry and removes AI features, but it cannot remove the GDID or stop all diagnostic data. Windows still reports a persistent device identifier to Microsoft regardless of how many settings you disable. This card is about harm reduction. If the user wants maximum privacy, the "Linux Desktop" card is the real answer.

### Step 2: Download and run Win11Debloat
Guide the user to use Win11Debloat — a free, open-source PowerShell script (MIT license, 52k+ stars) that works on both Windows 10 and 11. Two methods:

**Quick method (recommended)**: Open PowerShell as Administrator (right-click Start → Windows PowerShell (Admin) or Terminal (Admin)) and run:
```
& ([scriptblock]::Create((irm "https://debloat.raphi.re/")))
```

**Manual method**: Download from github.com/Raphire/Win11Debloat and run Run.bat as Administrator.

### Step 3: Walk through the interactive menu
Tell the user the script will present an interactive menu. They should review each option before running. Key things to select:
- **Remove pre-installed apps**: Removes Xbox, Candy Crush, Weather, News, and other bloatware
- **Disable telemetry**: Disables diagnostic data collection, activity history, app-launch tracking, and targeted ads
- **Remove Microsoft Copilot**: Disables the AI assistant
- **Remove Windows Recall**: Disables the screenshot-everything AI feature
- **Remove Click to Do**: Disables the AI-powered screen analysis
- **Disable AI features in Edge, Paint, and Notepad**: Stops AI suggestions and generation
- **Disable Bing web search and Copilot in Start menu**: Prevents Start menu search from sending queries to Bing
- **Disable lock screen tips, suggestions, and ads**: Removes Windows tips and sponsored content
- **Restore Windows 10-style context menu**: If they prefer the classic right-click menu
- **Enable dark mode, disable transparency/animations**: Performance and visual preferences
- **Show file extensions and hidden files**: Good security practice
- **Disable Find My Device**: Stops location tracking
- **Disable Delivery Optimization**: Stops P2P update sharing (which uses your bandwidth)

### Step 4: Export settings for future use
Tell the user to export their configuration after the script runs. This lets them apply the same settings to other machines or re-apply after a Windows update.

### Step 5: Post-debloat steps
After the script runs, guide the user to:
- **Check Edge settings**: Open Edge → Settings → Privacy, search, and services. Turn off "Save and fill basic info," "Save and fill payment info," "Improve your web experience," "Help improve Microsoft products." Turn on "Strict" tracking prevention. Turn off "Copilot" in the sidebar.
- **Check Start menu**: Right-click any pinned bloatware and select "Unpin from Start."
- **Check taskbar**: Right-click the taskbar → Taskbar settings. Turn off "Widgets," "Chat," "Task View," and "News and interests."
- **Restart**: Reboot to ensure all changes take effect.

### Step 6: Verify the changes
Tell the user to open Settings → Privacy & security → Diagnostics & feedback. The diagnostic data setting should now be at "Required" or "Basic" (not "Full"). Open the Start menu and confirm Copilot is gone. Open the installed apps list and confirm bloatware is removed.

## Decision Points

The agent knows the user's platform from onboarding. If they're on Windows 11 Home, note that some features (like BitLocker) are not available. If they're on Windows 10, the process is similar but some options (like Copilot) may not appear.

If the user is not comfortable running PowerShell scripts, suggest the manual approach: download the ZIP from GitHub, extract it, and run Run.bat as Administrator. The script is fully open source with 52k+ stars on GitHub.

## Pitfalls

- **GDID cannot be removed** — This is the most important limitation. A debloated Windows still reports a persistent device identifier to Microsoft. No script, registry tweak, or group policy can remove it.
- **Windows Update restores removed apps** — Major Windows updates (feature updates, not patches) may reinstall bloatware. Re-run Win11Debloat after feature updates.
- **Copilot and Recall may return** — Microsoft has been aggressive about re-enabling AI features through updates. Check after each monthly update.
- **Some apps can't be removed** — Core Windows components are protected. Win11Debloat will not attempt to remove them. If the user tries to manually remove something like Microsoft Edge, it may break Windows functionality.
- **Offline account is better** — Suggest the user switch to a local account (not a Microsoft account) in Settings → Accounts → Your info → "Sign in with a local account instead." This removes the Microsoft account link and reduces cloud sync.
- **Linux is the real answer** — If the user expresses frustration with Windows's inability to fully stop phoning home, guide them to the "Linux Desktop" card.

## Sources

1. pcmag.com/news/a-hackers-arrest-reveals-microsoft-can-track-users-via-a-windows-device-id (PCMag: Hacker's arrest reveals Microsoft can track users via Windows Global Device ID — FBI used GDID to track suspect across VPNs and 4 countries)
2. ghacks.net/2026/07/12/microsoft-confirms-windows-gdid-device-identifier-that-cannot-be-disabled-documented-in-fbi-case-filing/ (gHacks: Microsoft confirms Windows GDID device identifier that cannot be disabled)
3. theverge.com/2024/6/3/24170305/microsoft-windows-recall-ai-screenshots-security-privacy-issues (The Verge: Windows AI feature that screenshots everything labeled a security disaster — Recall stored screenshots in unencrypted database)
4. arstechnica.com/gadgets/2024/09/microsoft-details-security-privacy-overhaul-for-windows-recall-ahead-of-relaunch/ (Ars Technica: Microsoft details security overhaul for Windows Recall after plain-text database discovery)

## Guides

1. github.com/Raphire/Win11Debloat (Win11Debloat: open-source PowerShell script to remove bloatware and disable telemetry)
---
type: "lbr8 Protocol Card"
title: "Wearable Device Data Privacy"
description: "Prevent your fitness tracker or smartwatch from sending biometric data to vendor clouds by replacing their app, going wired-only, or choosing open hardware."
tags:
  - "phase-5"
  - "devices"
  - "advanced"
  - "p5"
  - "big-tech-surveillance"
  - "tracking"
  - "data-breach"
  - "vendor-lockin"
related:
  - "cards/fitness-tracking.md"
  - "cards/smart-device-audit.md"
  - "cards/permissions-audit.md"
draft: true
---
> ⚠️ **This card is a work in progress.** It has not been reviewed for accuracy or completeness. Use at your own risk — verify any recommendations against primary sources before acting on them.


## Steps

### Android

Gadgetbridge (F-Droid, FOSS) replaces the vendor app entirely — no account, no cloud, no network permission. Data stays on your phone. Supports many Mi Band, Amazfit, Huawei, and some Garmin models. Some devices require one-time pairing with the official app to extract an auth key, then you uninstall the vendor app. For fully open hardware: PineTime or Bangle.js 2 (pair natively with Gadgetbridge, no vendor app ever). Trade-off: open hardware is not yet viable for fitness-focused use — a 2025 peer-reviewed validation study (n=47, PMC12074211) found Bangle.js 2 heart rate agreement drops from "strong" to "good" during activity, underreporting max HR (178 BPM vs 195 reference). PineTime HR is unreliable during movement. Open hardware also lacks gym/workout tracking and has no iOS companion app for data sync.

### iOS

Apple Watch with Apple Health offers genuine E2EE — Apple cannot read your health data, and it is not used for advertising. This is the strongest default privacy among mainstream wearables. However: (1) E2EE ends the moment you connect third-party apps like Strava, (2) you are locked into the Apple ecosystem, (3) Apple Watch is expensive. If you stay within Apple Health only (no third-party sharing, iCloud sync disabled), your data is architecturally protected. No Gadgetbridge equivalent exists on iOS.

### Desktop

If your wearable supports USB file transfer (some Garmin, Polar, Coros models), disable Bluetooth and cloud sync entirely. Connect the device to your computer via USB cable only, and use desktop software like Golden Cheetah or Garmin Express (offline mode) to import data. This is the slowest but most private approach for mainstream hardware — no wireless data leaves the device.

## Sources

1. eff.org/deeplinks/2026/07/most-smart-watches-rings-and-bands-lack-basic-transparency-reports-and-key-privacy (EFF wearable privacy investigation, July 2026)
2. classaction.org/media/lomeli-v-whoop-inc.pdf (Lomeli v. Whoop class action, N.D. Cal., 2025)
3. classactionu.org/mass-arbitrations/current-claims/oura-ring/ (Oura mass arbitration claims)
4. gadgetbridge.org (Gadgetbridge — FOSS, cloudless Android companion app)
5. codeberg.org/Freeyourgadget/Gadgetbridge (source code, supported device list)
6. mozillafoundation.org/en/privacynotincluded/ (Mozilla Privacy Not Included — wearable reviews)
7. doi.org/10.1038/s41746-025-01757-1 (Nature: Privacy in consumer wearable technologies, 2025)
8. cybernews.com/news/samsung-health-ai-training-delete-user-data (Samsung Health AI consent, July 2026)
9. ghostvault.live/blog/fitness-tracker-selling-health-data (Fitness tracker data selling overview)
10. closednetwork.io/runna-garmin-apple-health-which-one-actually-doesnt-sell-your-data/ (Wearable privacy policy comparison)
11. cnet.com/tech/services-and-software/facebook-receives-personal-info-like-your-heart-rate-from-popular-apps/ (CNET: Facebook receives biometric data from fitness apps via SDKs, Feb 2019)
12. pmc.ncbi.nlm.nih.gov/articles/PMC12074211/ (Validation of Bangle.js 2 for step counting and heart rate monitoring, 2025)

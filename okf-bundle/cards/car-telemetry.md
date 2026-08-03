---
type: "lbr8 Protocol Card"
title: "Car Telemetry Disabling"
description: "Modern cars are always-on surveillance devices. Disable telemetry via software opt-out, or physically remove the modem for a true air gap."
tags:
  - "phase-3"
  - "devices"
  - "intermediate"
  - "p3"
  - "tracking"
  - "big-tech-surveillance"
  - "data-breach"
related:
  - "cards/smart-tv-blocking.md"
  - "cards/network-segmentation.md"
---

## Steps

### General

Modern cars are computers on wheels with always-on cellular modems (DCM/TCU), GPS, inward and outward cameras, microphones, and hundreds of sensors. They continuously transmit location, speed, acceleration, braking events, fuel levels, and driving behavior data to manufacturer servers. This data is sold to data brokers like LexisNexis and Verisk, who sell it to insurance companies — often without the driver's knowledge. A 2025 Subaru vulnerability allowed anyone to remotely unlock cars and access real-time GPS location history. Tesla employees were caught sharing customer camera footage in 2023. In 2024, GM was penalized by the FTC for selling driving data to insurers without consent. Consumer Reports found nearly every automaker sells or shares driver behavior data.

**Level 1 — Software Opt-Out (15-30 min, no tools):**
The minimum step. Disable connected services and data sharing through your car's infotainment system and mobile app. Trade-off: you lose remote start, cloud navigation, SOS/emergency calling, and over-the-air updates.

1. **Check what your car collects**: Enter your VIN at privacy4cars.com/vehicle-privacy-report — see what data your make/model collects and who it shares with
2. **Infotainment settings**: Navigate to Settings → Privacy/Data Sharing. Disable: data sharing, location sharing, viewing data collection (ACR), diagnostics/usage data, personalized ads, driver scoring/feedback programs
3. **Mobile app**: Open your manufacturer's app (Toyota app, FordPass, MyBMW, etc.) → Settings → disable all data sharing, location tracking, and connected services. Cancel connected services subscriptions
4. **Call the manufacturer**: Request "complete data collection opt-out" in writing. Key numbers:
   - GM/OnStar: 1-800-800-2813 — say "Cancel all connected services for privacy reasons"
   - Toyota: Press SOS button in car, or call Customer Care
   - BMW: 1-855-BMW-PRIV — also request embedded SIM card disabling
   - Mercedes: 1-800-367-6372 or me-connect.usa@cac.mercedes-benz.com
   - Ford, Honda, Hyundai/Kia, Subaru: Call customer service, request opt-out + written confirmation
5. **File data deletion requests**: Under state privacy laws (CA, CO, and 15+ other states), submit "Right to Opt Out" and "Right to Delete" requests through the manufacturer's privacy portal
6. **Opt out of insurance data brokers**: Request your file from LexisNexis (consumer.risk.lexisnexis.com) and Verisk, then submit opt-out and deletion requests. Look for the "Telematics" section in your LexisNexis report — if it contains driving data, your car manufacturer has been sharing it
7. **Verify**: After 45-90 days, re-request your data to confirm deletion. Check that the car's infotainment shows no data connection.

Important: Software opt-outs are often unreliable. The New York Times and EFF reported that even after opting out, some cars continue transmitting data. Some manufacturers re-enable data sharing after firmware updates. Treat software opt-out as a necessary but insufficient step. DNS-level blocking (AdGuard Home, Pi-hole) won't help either — cars transmit via their own cellular modem, not your home Wi-Fi.

**Level 2 — Physical Modem Removal (2-4 hours, requires basic tools):**
The only reliable method. Physically remove the Data Communication Module (DCM) / Telematics Control Unit (TCU) so the car has no cellular connection. Also disconnect the GPS antenna so the car cannot confuse CarPlay with stale GPS data.

Best documented for Toyota (RAV4, Camry, Corolla) thanks to detailed community guides. Varies significantly by manufacturer — some integrate the modem deeply into the vehicle bus, making removal impractical.

General approach (Toyota-specific guides available at rav4world.com):
1. Disconnect the negative battery terminal
2. Remove dashboard trim around the shifter and infotainment screen
3. Locate the DCM (usually behind the infotainment screen or under the dash)
4. Remove the mounting bolts (typically 8mm or 10mm)
5. Disconnect all cables from the DCM
6. Install a DCM bypass kit (preserves in-cabin microphone for phone calls via CarPlay)
7. Disconnect the GPS antenna from the head unit (single-wire connector, identify by process of elimination)
8. Reassemble everything

Critical Bluetooth caveat: Even with the modem removed, if you connect your phone via Bluetooth, the car may use your phone as an internet connection and resume transmitting data. Use a USB cable for CarPlay/Android Auto instead. Alternatively, use a Bluetooth-to-USB adapter — the car thinks it has a wired connection and won't tether through your phone.

Trade-offs: You lose SOS/emergency calling, remote start, cloud navigation, over-the-air updates, and connected services. CarPlay/Android Auto still work via USB (navigation uses your phone's GPS). Dealer software updates require a visit. Magnuson-Moss Warranty Act protects you — manufacturer cannot deny warranty claims for unrelated systems due to DCM removal. Some cars may throw error codes or disable certain features (sport mode, etc.) when the modem is removed — research your specific model first.

When to consider Level 3: Your car is always-on and phone-home regardless of settings. You want a true air gap. You're comfortable with basic automotive DIY (or willing to pay a shop).

Resources for specific models: Toyota/RAV4 has the best community documentation. Other brands vary — search "[your car] DCM removal" or "[your car] telematics disable" for model-specific guides.

## Sources

1. arkadiyt.com/2026/05/13/removing-the-modem-and-gps-from-my-rav4/ (Detailed DCM+GPS removal guide for 2024 RAV4 Hybrid)
2. youtube.com/watch?v=2vq7Xfn5D4Y (The Drive: How to Stop Your Car From Sharing Your Data)
3. consumerreports.org/electronics/personal-information/how-to-stop-your-car-from-collecting-sharing-driving-data-a1233378612/
4. eff.org/deeplinks/2024/03/how-figure-out-what-your-car-knows-about-you-and-opt-out-sharing-when-you-can
5. apnews.com/article/auto-car-privacy-3674ce59c9b30f2861d29178a31e6ab7
6. theautopian.com/heres-how-to-stop-your-car-from-sharing-your-data/
7. rav4world.com/threads/how-to-fully-disable-telemetry-and-have-an-air-gapped-car.343029/
8. privacy4cars.com/vehicle-privacy-report
9. ftc.gov/reports (GM Smart Driver penalty, 2024)
10. mashable.com/article/privacy-please-what-data-do-modern-cars-collect (Mashable: Your car knows too much about you)

## Prerequisites

No prerequisites — this card is self-contained.

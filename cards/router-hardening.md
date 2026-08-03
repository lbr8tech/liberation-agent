---
type: "lbr8 Protocol Card"
title: "Router Hardening"
description: "Secure your router by changing the admin password, disabling WPS and UPnP, and enabling automatic firmware updates."
tags:
  - "phase-3"
  - "network"
  - "intermediate"
  - "p3"
  - "tracking"
  - "malware"
  - "big-tech-surveillance"
related:
  - "cards/router-dns.md"
  - "cards/network-segmentation.md"
  - "cards/router-firmware.md"
draft: true
---
> ⚠️ **This card is a work in progress.** It has not been reviewed for accuracy or completeness. Use at your own risk — verify any recommendations against primary sources before acting on them.


## Steps

### General

The firewall (NAT + SPI) is already ON by default in almost every consumer router — you do NOT need to buy a new router. The real work is closing other security holes:

1. Change admin password (default passwords are publicly known)
2. Disable WPS (PIN-based, crackable in minutes with Reaver)
3. Disable UPnP (lets malware auto-open ports; manually forward if needed)
4. Disable remote admin (router admin page should not be reachable from internet)
5. Set Wi-Fi encryption to WPA3-Personal, or WPA2-AES (never WEP/WPA/WPA2-TKIP)
6. Enable firmware auto-update if available, else check monthly
7. Audit and remove unknown port forwards
8. Rename SSID to something neutral (no name, router model, or ISP)
9. Enable guest network for visitors (client isolation on)
10. Enable IPv6 firewall if your ISP provides IPv6

**Verify (5 min):** After hardening, confirm your ports are actually stealthed from the internet. Run GRC ShieldsUP! (grc.com/shieldsup) — click "Proceed," then "All Service Ports." It probes your public-facing ports from their server. You want every port to show **STEALTH** (not just "closed"). If any show OPEN, you have a misconfigured port forward or UPnP rule letting traffic through. Also check dnsleaktest.com (Extended Test) to confirm your DNS queries aren't still going to your ISP.

## Sources

1. plainlysec.com/home-wifi-router-security-complete-hardening-guide/
2. tp-link.com user guides
3. kb.netgear.com/224
4. expressvpn.com/blog/what-is-spi-firewall/

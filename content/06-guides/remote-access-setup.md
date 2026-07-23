---
title: "Guide: Setting Up Secure Remote Access"
date: 2026-07-22
---
## Overview
Checking on the pool automation or an ecobee zone while away from home means Home Assistant needs to be reachable from outside the house.

### The Options
1. **Port forwarding directly to Home Assistant**: The simplest to set up, but also the one ruled out first. Making Home Assistant's web interface open directly to the internet means every vulnerability in Home Assistant (or any add-on) becomes remotely exploitable.
2. **A managed remote-access service**: Trades setup effort for a subscription.
3. **A self-hosted VPN (WireGuard)**: More setup, but no open inbound ports and no third-party relay needed.
### The Approach
1. **WireGuard runs as its own container** in the [[../01-infrastructure/docker-container-stack|Docker stack]], on the same [[../01-infrastructure/server-hardware|EliteDesk hardware]].
2. **Only the WireGuard port is forwarded** on the router — Home Assistant itself is never directly exposed.
3. **My phone and laptop run a WireGuard client**, and connecting to the VPN makes the [[../02-platforms/home-assistant-core|Home Assistant]] reachable as if I were on the home network.  This including local-only integrations like [[../04-integrations/wiz-connected|WiZ]] and [[../04-integrations/lutron-caseta|Lutron Caseta]] that don't work at all over the open internet.
### Trade-offs
- If home internet is down, remote access is down too.
- Firmware/software updates to the VPN container are on me, not a vendor, to keep current.

### Related Reading
- [[../01-infrastructure/network-segmentation|Network Segmentation]]
- [[../01-infrastructure/docker-container-stack|Docker Container Stack]]


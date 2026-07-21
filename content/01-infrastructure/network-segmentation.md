---
title: Network Segmentation
date: 2026-07-20
---
## Overview
IoT devices are some of the least trustworthy endpoint on a network.  They often have cheap firmware and rarely get security updates.
### High-Level Approach
1. **A dedicated IoT VLAN**, separate from the VLAN my personal devices use.
2. **The [[../01-infrastructure/server-hardware|Home Assistant server]] bridges both VLANs** intentionally, since it needs to talk to IoT devices for control and to my phone for the companion app.
3. **Outbound internet access is limited** for the IoT VLAN and only allowed when a device has a cloud dependency.
### Why the Bridge
Several integrations depend on local network discovery rather than the cloud:
- WiZ bulbs use **UDP broadcast** on the local subnet to be discovered by Home Assistant.
- The Lutron Caseta bridge talks to Home Assistant over a local API on the same network.
Segmentation only works if it doesn't break these discovery mechanisms. 
### Trade-offs I've Accepted
- More router/firewall complexity than a single flat network, but I am a Network Engineer at heart so what do you expect.
- Extra troubleshooting overhead any time a new device won't discover.
### Related Reading
- [[server-hardware|Home Server Hardware]]
- [[../04-integrations/wiz-connected|WiZ Connected Lighting]]

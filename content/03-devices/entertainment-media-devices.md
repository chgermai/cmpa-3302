---
title: Entertainment & Media Devices
date: 2026-07-21
---
## Overview
A handful of entertainment devices are integrated into Home Assistant, mostly so they can be included in scenes and automations rather than needing their own separate remotes.
### Device Inventory
- **Denon AVR Network Receiver**: 1 device, controlling audio for the Game Room and backyard.
- **Samsung Smart TV**: 2 devices, exposed as media players.
### Why Bring These Into Home Assistant
On their own, a receiver and a couple of TVs don't need home automation. What makes it worthwhile is combining them with everything else:
- The Game Room's [[wiz-bulbs-fixtures|WiZ lighting scenes]] (Movie/TV, Pool Table, Rest) can be triggered alongside turning on the TV and receiver, so "movie night" is a single action instead of three.  This is still a work in progress and isn't working quite right.
- Volume and input state can be checked from the same dashboard as the room's lighting and climate, rather than needing a separate app.
### Reliability
Both the [[../04-integrations/denon-avr-integration|Denon]] and [[../04-integrations/samsung-smart-tv-integration|Samsung]] integrations depend on the devices being reachable on the local network. Smart TVs tend to go into a deep sleep where they stop responding to network commands until manually woken .

### Related Reading
- [[../04-integrations/denon-avr-integration|Denon AVR Integration]]
- [[../04-integrations/samsung-smart-tv-integration|Samsung Smart TV Integration]]
- [[wiz-bulbs-fixtures|WiZ Bulbs & Fixtures]]

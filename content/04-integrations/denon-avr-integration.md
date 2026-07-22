---
title: Denon AVR Integration
date: 2026-07-21
---
## Overview
A single Denon AVR network receiver handles audio for the game room and backyear.  It connects to Home Assistant over the local network using Denon's Network Receiver protocol.
### Setup
Home Assistant discovers Denon network receivers automatically once they're on the same subnet as the [[../01-infrastructure/server-hardware|Home Assistant server]] — no manual IP configuration is typically required as long as network discovery traffic isn't being blocked (see [[../01-infrastructure/network-segmentation|Network Segmentation]]).
### What It Exposes
- Power on/off
- Volume level and mute
- Input source selection
- Currently playing source info, where supported
### Use in Scenes
Paired with the [[samsung-smart-tv-integration|Samsung Smart TV integration]] and the [[../03-devices/wiz-bulbs-fixtures|Game Room lighting scenes]], the receiver becomes part of a single "Movie/TV" action rather than a separate step with its own remote.

### Related Reading
- [[../03-devices/entertainment-media-devices|Entertainment & Media Devices]]
- [[samsung-smart-tv-integration|Samsung Smart TV Integration]]

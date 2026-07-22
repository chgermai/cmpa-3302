---
title: Samsung Smart TV Integration
date: 2026-07-21
---
## Overview
Two Samsung Smart TVs are integrated with [[../02-platforms/home-assistant-core|Home Assistant]] as `media_player` entities, connecting over the local network rather than through a cloud service.
### Setup
Home Assistant discovers Samsung TVs on the local network and pairs with them using Samsung's SmartThings-compatible local API. The first time you turn an automation loose on the TV, it typically prompts an on-screen "Allow access?" confirmation that has to be accepted once from the TV's own remote.
### What It Exposes
- Power state (on/off)
- Volume and mute control
- Input source switching
- App launch, for a limited set of supported apps
### Use in Scenes
Combined with the [[../03-devices/wiz-bulbs-fixtures|Game Room WiZ lighting scenes]], the TV can be brought into a single "Movie/TV" action alongside dimming the lights, rather than needing the Samsung remote and the lighting app separately.
### Related Reading
- [[../03-devices/entertainment-media-devices|Entertainment & Media Devices]]
- [[denon-avr-integration|Denon AVR Integration]]

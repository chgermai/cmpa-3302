---
title: WiZ Connected Lighting
date: 2026-07-21
---
![[wiz-logo-small.svg]]
## Overview
I moved to Wiz bulbs after some pain with the original Tuya bulbs I used. I found them easier to use and setup then Tuya and they were widely available in stores and online.  Home Assistant has the ability to natively discover and control WiZ bulbs on the local network. 
### Local Discovery
When you first configure a WiZ bulb you need to register it to their could service.  But once it is configured and online you can discover the bulb with Home Assistant (HA).  Both the bulbs and the HA server are on the same subnet so the discovery process is nearly automatic.  The main concern to to make sure you are not blocking UDP broadcasts. 
### Current Installation
I utilize WiZ bulbs in the following rooms
- Game Room
- Outdoor Lighting
- Living Room
#### Game Room Scenes
In the Game Room, I have multiple groupings to allow us to optimize the light by applying scenes.
- Movie/TV – Keep the light dimmed near the exit and bar area but the rest of the lights are off.
- Pool Table– Keep most of the lights in a relaxing hue but the ones over the pool table are 100% brights in full white.
- Rest – Keep on the light near the exist dimmed the rest of the lights are off.
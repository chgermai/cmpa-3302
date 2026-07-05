---
title: Generic IFTTT Integration
---
## Overview
IFTTT (If This Then That) is a catch-all integration for connecting services that don't have a native [[02-platforms/index|Home Assistant]] integration.  I also use it for devices I only need to touch occasionally and building a custom integration isn't worth the effort. It works on simple logic.  A trigger from one service ("this") fires an action in another service ("that").
### Why use it
Most of my core devices, including  [[wiz-connected|WiZ bulbs]] and [[04-integrations/lutron-caseta|Lutron Caseta]] light and fan controls communicate with Home Assistant directly through their own integrations. But a handful of devices only expose a webhook or an IFTTT applet rather than a full API. Rather than writing and maintaining custom code, IFTTT handles the basics.
### Applets Currently Running
- Severe weather alerts (from the [[04-integrations/weather-api|weather API integration]]) triggers a text message to my phone.
- A webhook fired from the [[node-red-pool-automation|pool automation flow]] send a message to my wife and I if the flow switch reports no water movement for more than five minutes.
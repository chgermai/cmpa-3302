---
title: Home Assistant Core
date: 2026-07-20
---
## Overview
Home Assistant is the central hub every device and integration ultimately reports to. It's an open-source application and every integration described in the [[../04-integrations/index|Integrations section]] plugs into it.
### A Bit of History
This installation has been through more than one life:
- It started as a Raspberry PI Container.
- I then migrated it to run as **Home Assistant OS**, directly on the [[../01-infrastructure/server-hardware|EliteDesk server]].
- The existing data files were just carried over creating a headache to unravel and troubleshoot.
- The last update before the rebuild was `core_2023.10.1`, meaning the instance sat untouched for over two years.
### What It Manages Today
- **Dashboards**: Room based views with each showing the relevant lights, sensors, and weather for that space.
- **Integrations**: Both cloud services ([[../04-integrations/ecobee-integration|ecobee]]) and local devices like ([[../04-integrations/wiz-connected|WiZ bulbs]]).
- **Automations**: The rules documented in the [[../05-automations/index|Automations section]].
### Why Home Assistant Specifically
1. **Local-first**: Integrations that support local control (WiZ, Lutron Caseta) keep working even without internet access.
2. **No vendor lock-in**: I'm not stuck inside a single manufacturer's app ecosystem.
3. **Community Support**: Most devices I've bought over the years already have either a built-in or community-maintained integration through [[hacs-community-store|HACS]].
### Related Reading
- [[mosquitto-mqtt-broker|Mosquitto MQTT Broker]]
- [[node-red-overview|Node-RED Overview]]
- [[../01-infrastructure/docker-container-stack|Docker Container Stack]]

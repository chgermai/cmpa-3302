---
title: Docker Container Stack
date: 2026-07-20
---
## Overview
I started this project running [[02-platforms/home-assistant-core|Home Assistant]] on bare-metal (Supervised). After a few years I decided to rebuild it on Ubuntu Server with Docker for added flexibility.

### Why Move Off Supervised
The old Supervised install had accumulated a lot of baggage:
- The last known good backup was `core_2023.10.1`, which was two years old at the time of the rebuild.
- Several integrations were failing and support was mixed on the versions running.
- There was an even older backup in the history from an instance that had been carried over; including leftover config that no longer matched the hardware.

Rather than waste time debugging, a clean Docker-based rebuild let me start from a known-good state while keeping the same physical hardware.
### The Stack Today
Everything now runs as containers on Ubuntu Server:
1. **Home Assistant Core**: the automation hub itself
2. **Mosquitto**: the [[mosquitto-mqtt-broker|local MQTT broker]] used primarily for pool sensor data
3. **Node-RED**: for flows that don't belong in native Home Assistant automations, like the [[../04-integrations/node-red-pool-automation|pool automation]]
### Advantages Over Supervised
- **Isolation**: each service has its own container, so an update to one doesn't risk breaking another.
- **Portability**: the whole stack is defined in compose files, so moving to new hardware in the future is a simpler process.
- **Explicit backups**: rather than relying on the built-in backup tooling, each container's data volume is backed up on a schedule.
### Related Reading
- [[../06-guides/rebuilding-home-assistant|Rebuilding Home Assistant]]
- [[network-segmentation|Network Segmentation]]

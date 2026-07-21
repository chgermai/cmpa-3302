---
title: Home Server Hardware
date: 2026-07-20
---
## Overview
Everything in this knowledge base runs on one physical box sitting in a closet.  I repurposed a small business desktop that would otherwise have been thrown away.
### The Hardware
- **Model:** HP EliteDesk 800 G2 Mini
- **CPU:** Intel Core i5-6500T @ 2.5GHz
- **RAM:** 8GB DDR4
- **Storage:** 240GB SSD
### Why a Mini Desktop Instead of a Raspberry Pi
1. **CPU**: A Core i5, comfortably runs [[02-platforms/home-assistant-core|Home Assistant]], a database, and several containers at once without the bottlenecks on a Pi-based setup.
2. **Hard Drive**: The biggest source of corrupted Home Assistant installs is SD card wear on Raspberry Pi builds. A SSD avoids that failure mode entirely.
3. **Cheap**: I had access to a used desktop and it was small enough to easily fit in my closet.
### Placement and Power
It's small enough to tuck into a closet near the network rack, runs quiet enough that nobody notices it, and its power use is low enough that I don't think about the cost.
### Related Reading
- [[docker-container-stack|Docker Container Stack]]
- [[network-segmentation|Network Segmentation]]
- [[../06-guides/rebuilding-home-assistant|Rebuilding Home Assistant]]

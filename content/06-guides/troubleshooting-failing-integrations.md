---
title: "Guide: Troubleshooting Failing Integrations"
date: 2026-07-21
---
## Overview
Before the [[rebuilding-home-assistant|rebuild]], four things on the old instance were stuck an not working: Bluetooth, [[../02-platforms/hacs-community-store|HACS]], WiZ, and WLED. This guide walks through how I fixed each one.
### Is It Actually Broken?
The first find, the Game Room's WiZ light was showing "Failed setup, will retry" in the integrations list, yet it was still live and controllable from the Overview dashboard. 
### Bluetooth
**Symptom**: "Failed setup, will retry," 1 device.
**Likely cause:** Bluetooth adapters are sensitive to driver and kernel version mismatches, and this instance's underlying OS hadn't been updated in years.
**Resolution path**: Rebuilding on a current Ubuntu Server image (see [[rebuilding-home-assistant|the rebuild guide]]) resolved this by starting from current drivers rather than patching an old kernel.
### HACS
**Symptom**: "Failed to set up," offering only "Reconfigure."
**Likely cause**: HACS depends on GitHub's API and its own backend service, both of which are upgraded independently of Home Assistant releases. The age of the install effectively guaranteed that it had fallen out of compatibility.
**Resolution path**: Full reinstall against the current Home Assistant release, rather than trying to coax the existing configuration back to life.
### WiZ
**Symptom**: "Failed setup, will retry," 8 devices 
**Likely cause**: Local UDP discovery is sensitive to network conditions; see [[../01-infrastructure/network-segmentation|Network Segmentation]] for how VLAN rules can interfere with broadcast discovery.
**Resolution path**: Confirmed the network wasn't blocking UDP broadcast, then let the integration retry after the rebuild.
### WLED
**Symptom**: "Failed setup, will retry," 1 device.
**Likely cause**: Similar to WiZ; a local-network device integration that had likely lost its DHCP lease or IP address over the long gap without anyone verifying it.
**Resolution path:** Reconfigured fresh post-rebuild rather than assuming the original configuration was still accurate.
### The  Pattern
Every one of these traced back to the same root cause: a system that went untouched for years while the devices, network, and external services around it kept changing. None of them were unfixable, they just needed attention rather than continuing to "retry" silently in the background.
### Related Reading
- [[rebuilding-home-assistant|Rebuilding Home Assistant]]
- [[../02-platforms/hacs-community-store|HACS]]
- [[../01-infrastructure/network-segmentation|Network Segmentation]]


---
title: Vacation Mode Automation
date: 2026-07-21
---
## Overview
A single "Vacation Mode" switch in Home Assistant changes the behavior of several automations at once, rather than requiring me to manually reconfigure each area before a trip.
### What Changes When It's Active
1. **Exterior lighting**: The [[exterior-lighting-schedule|sunset-relative schedule]] swaps to a randomized preset pattern from the Playlist selector instead of a fixed scene, so the house doesn't look obviously unattended from the street.
2. **Climate zones**: Every ecobee zone drops to an away setpoint via the [[../04-integrations/ecobee-integration|ecobee integration]].
3. **Notifications**:  The [[mobile-notifications-automation|mobile notification]] thresholds tighten, since there's no one physically present to notice an issue before it becomes serious.
### Why a Single Toggle Instead of Manual Changes
Before this existed, prepping the house for a trip meant remembering to adjust the thermostats, the exterior lighting preset, and the notification settings separately — and un-remembering to revert all of it on return. Consolidating it into one switch removed the chance of forgetting a step in either direction.
### Related Reading
- [[exterior-lighting-schedule|Exterior Lighting Schedule]]
- [[mobile-notifications-automation|Mobile App Notifications]]


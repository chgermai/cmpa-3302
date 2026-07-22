---
title: Exterior Lighting Schedule
date: 2026-07-21
---
## Overview
The Exterior area's Porte-cochère and Walkway downlights, built on [[../03-devices/wiz-bulbs-fixtures|WiZ fixtures]], run on an automated schedule rather than needing to be switched on manually every evening.

### The Logic
1. **Sunset-relative trigger**: Home Assistant's sun entity fires the "turn on" trigger a set number of minutes before actual sunset, rather than a fixed clock time, so the lights stay in sync with the season instead of turning on too early in summer or too late in winter.
2. **Playlist and preset selection**: The Exterior dashboard's Playlist and Preset selectors let me pick a lighting pattern (steady white, a warmer scene, etc.) that the automation applies at trigger time.
3. **Late-night dimming**: After a set late hour, brightness steps down rather than switching off outright, balancing visibility for anyone arriving home late against not lighting up the whole front of the house all night.
4. **Sunrise-relative shutoff**: Lights turn off relative to sunrise the same way they turn on relative to sunset.
### Manual Override
The Playlist and Preset selectors on the Exterior dashboard double as a manual override, allowing a user to select a different preset mid-evening (for a party, for example) overrides the automated pattern until the next scheduled trigger resets it.
### Related Reading
- [[../03-devices/wiz-bulbs-fixtures|WiZ Bulbs & Fixtures]]
- [[vacation-mode-automation|Vacation Mode Automation]]


---
title: WiZ Bulbs & Fixtures
date: 2026-07-21
---
## Overview
This page covers the physical WiZ lighting hardware installed around the house. For how Home Assistant talks to these bulbs, see the [[../04-integrations/wiz-connected|WiZ Connected integration page]] — this page is about the fixtures themselves and where they're deployed.
### Fixture Inventory
| Area                     | Fixture                | Notes                  |
| ------------------------ | ---------------------- | ---------------------- |
| Exterior — Porte-cochère | Downlights             | 3 lights               |
| Exterior — Walkway       | Downlights             | 4 lights               |
| Game Room                | WiZ RGBW Tunable light | Back exterior entrance |
| Game Room                | Downlights             | 12 lights              |
### Why I Moved to WiZ
I originally ran Tuya bulbs in several of these same locations. WiZ bulbs replaced them because:
1. Setup was noticeably simpler.
2. They were more widely available in stores and online, so replacing a failed bulb doesn't mean waiting on a specific supplier.
3. Home Assistant's local discovery works cleanly with them, unlike some of my remaining Tuya devices, which stay on the [[../04-integrations/tuya-cloud-integration|Tuya Cloud integration]].
### Physical Considerations
- Exterior fixtures need to tolerate outdoor temperature swings and moisture — I stuck to fixtures explicitly rated for exterior/damp locations rather than repurposing indoor bulbs outside.
- All fixtures are on the same local subnet as the [[../01-infrastructure/server-hardware|Home Assistant server]], which is what makes UDP-broadcast discovery reliable; see [[../01-infrastructure/network-segmentation|Network Segmentation]] for why.
### Related Reading
- [[../04-integrations/wiz-connected|WiZ Connected Lighting Integration]]
- [[../05-automations/exterior-lighting-schedule|Exterior Lighting Schedule]]


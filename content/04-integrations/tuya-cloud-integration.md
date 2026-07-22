---
title: Tuya Cloud Integration
date: 2026-07-21
---
## Overview
Not every Tuya device in the house has been replaced. While I moved the bulbs over to [[../04-integrations/wiz-connected|WiZ]] after some setup pain, a handful of Tuya smart switches are still in service and connect through Home Assistant's Tuya Cloud integration.
### Why This One Stayed Cloud-Based
Unlike WiZ or Lutron Caseta, there's no practical local-only path for these particular Tuya switches — they depend on Tuya's cloud service to relay commands, which means:
- An internet outage means these specific switches lose remote/automation control until connectivity returns (though they still work as ordinary manual switches).
- Setup requires linking a Tuya IoT developer account rather than simple local discovery.
### Setup
1. Create a Tuya IoT Platform developer account and register a cloud project.
2. Link the Tuya Smart Life app account used to originally set up the switches to that cloud project.
3. Authorize Home Assistant against the Tuya Cloud integration using the resulting API credentials.
### Related Reading
- [[../03-devices/wiz-bulbs-fixtures|WiZ Bulbs & Fixtures]]
- [[lutron-caseta|Lutron Caseta Integration]]


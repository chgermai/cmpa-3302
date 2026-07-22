---
title: Mobile App Notifications
date: 2026-07-21
---
## Overview
Three devices are registered through Home Assistant's Mobile App integration, which is what turns automation logic from "something happened" into "someone actually finds out about it."
### What Triggers a Notification
- **Pool safety alert**: The [[../04-integrations/node-red-pool-automation|Node-RED pool automation]]'s flow switch check fires a push notification (in addition to the [[../04-integrations/generic-ifttt|IFTTT text message]]) if the cleaner pump runs without detected water movement for more than five minutes.
- **Severe weather**: Tied to the same forecast data used by the [[../04-integrations/weather-api|weather API integration]], so a hard freeze warning reaches a phone, not just an automation log.
- **Device unavailable**: If a key device (an ecobee thermostat, the Lutron Caseta bridge) drops off Home Assistant's radar for more than a few minutes, a notification goes out rather than the issue silently persisting until someone happens to check the dashboard.
### Why Notifications, Not Just Automations
An automation that silently adjusts something is fine for routine tasks like lighting. But for anything safety-related — freeze protection, the pool's water flow — I want a human in the loop who can override the automation if the situation is unusual enough that the automated response isn't the right call.
### Related Reading
- [[../04-integrations/generic-ifttt|Generic IFTTT Integration]]
- [[../04-integrations/weather-api|OpenWeatherMap API Integration]]


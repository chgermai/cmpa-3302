---
title: Node-RED Overview
date: 2026-07-20
---
## Overview
Node-RED is a flow-based programming tool.  It allows you to connect nodes representing triggers, logic, and actions on a UI instead of writing code. I run it as its own container in the [[../01-infrastructure/docker-container-stack|Docker stack]].
### Why is it Needed
Home Assistant's built-in automations are great for simple trigger-condition-action (if/then) logic. But once logic needs to use multiple data sources, make stateful decisions, or branch based on more than a couple of conditions, this visual flow becomes easier to read and update.
### Where Node-RED is Used
Right now, the only use of Node-RED is the [[../04-integrations/node-red-pool-automation|pool automation]], which:
- Reads pool temperature over [[mosquitto-mqtt-broker|MQTT]]
- Reads forecast data from the [[../04-integrations/weather-api|OpenWeatherMap integration]]
- Adjusts pump runtime based on both
### A Deliberate Boundary
I've been careful to keep Node-RED use cases limited to where the complexity is needed. Most of the house's day-to-day automations stay in native Home Assistant automations, which are easier to review. Node-RED is reserved for the pool, where the decision logic is needed.
### Related Reading
- [[mosquitto-mqtt-broker|Mosquitto MQTT Broker]]
- [[../04-integrations/node-red-pool-automation|Node-RED Pool Automation Integration]]

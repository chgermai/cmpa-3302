---
title: Mosquitto MQTT Broker
date: 2026-07-20
---
## Overview
Not every sensor talks directly to Home Assistant's built-in integrations. The pool automation, in particular, depends on a local MQTT broker to move data between the pool's [[node-red-overview|Node-RED flow]] and Home Assistant.
### Why MQTT 
MQTT is a lightweight publish/subscribe messaging protocol built for this.  Lots of small, frequent sensor updates (temperature, flow status) that need to reach multiple subscribers without each sensor needing to know who's listening.
### What Runs Through It
- **Pool temperature sensor**: Read by the [[../04-integrations/node-red-pool-automation|Node-RED pool automation]] flow to decide whether the freeze-protection logic tied to the [[../04-integrations/weather-api|weather API integration]] needs to kick in.
- **Flow switch status**: Feeds the low-water alert that fires if the cleaner pump runs the primary pump.
### Running It in Docker
Mosquitto runs as its own container in the [[../01-infrastructure/docker-container-stack|Docker stack]], with its data volume backed up on the same schedule as the rest of the stack.
### Related Reading
- [[node-red-overview|Node-RED Overview]]
- [[../04-integrations/node-red-pool-automation|Node-RED Pool Automation Integration]]

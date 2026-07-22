---
title: ecobee Integration
date: 2026-07-21
---
## Overview
Home Assistant's ecobee integration connects to the four [[../03-devices/ecobee-thermostats|ecobee thermostats]] in the house through ecobee's cloud API.
### Setup
1. Register an application through ecobee's developer portal to get an API key.
2. Authorize Home Assistant against your ecobee account.  This is a one-time OAuth-style handshake.
3. Home Assistant then automatically discovers every thermostat and paired remote sensor tied to that account.

Once configured, each thermostat shows up as a `climate` entity, and any paired remote sensors appear as their own temperature/occupancy entities.
### What It Exposes
- Current and target temperature per zone
- HVAC mode (heat, cool, auto, off)
- Humidity readings
- Remote sensor occupancy, where paired sensors are installed
### Reliability
This is a cloud integration, not a local one — but it's the one exception in this house where that hasn't caused problems. Throughout ecobee kept working without falling into the "failed setup, will retry" state that affected several other integrations.
### Related Reading
- [[../03-devices/ecobee-thermostats|ecobee Thermostats]]


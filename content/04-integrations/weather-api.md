---
title: OpenWeatherMap API Integration
---
## Overview
Many of the automation I run depend on the conditions outside the house and weather is an important factor to consider.  The pool automations are probably the most critical aspect.  I integrated a free OpenWeatherMap into [[02-platforms/index|Home Assistant]] so automations can be based on conditions like temperature, wind, and forecasted rain.
### Setup
Home Assistant has a built-in integration for OpenWeatherMap that just requires adding an API key and a defining the latitude/longitude of your current location. Once configured, the integration provides several sensors:
1. Current temperature
2. "Feels like" temperature
3. Forecast (clear, rain, snow, etc.)
4. Wind speed and humidity
### Use Cases
#### Avoiding Frozen Water in Pool Plumbing
The most critical use case for this integration is in the winter months.  Since we do not close the pool for the winter it is important we prevent water from freezing in the system.  If the forecast predicts a cold night (below freezing) we can keep the pool running overnight or until the temperature sensor rises about freezing.  This lives in a flow inside [[node-red-pool-automation|Node-RED]], which pulls both the weather forecast and the pool temperature sensor data coming in over MQTT.
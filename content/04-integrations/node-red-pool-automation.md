---
title: Node-RED Pool Automation Integration
date: 2026-07-21
---
## Overview
The pool is the one automation systems in the house that isn't controlled through Home Assistant.  The whole system runs as a dedicated Node-RED flow. Node-RED is a flow-based programming tool the works well at gather inputs and making logical decisions. 
### Why Node-RED
Running the pump and heater on a simple schedule is ineffective.  I need to pool to operate based on real conditions.  In summer months when chlorine evaporates faster I need to run the pool 18 hours a day.  However, in the winter, I can run the pool only 8 hours in a day.  I am also able to control the cleaner pump and additional features based on what else is running.  Making sure that I don’t run the booster pump for the cleaner of the main pump is not running. 

> A pool system that relies on a simple timer doesn't know it's warmer than yesterday.  Node-RED is able top gather all the inputs and adjusts the schedule accordingly.
### Functions Controlled
The pool automation handles the following functions:
- Runs the pump based on daily schedule tied to temperature and date
- Runs the cleaner booster pump only when the main pump is running
- Runs the waterfall on a daily schedule to prevent dirt build-up
- Runs the heater only when in spa mode.
#### Flow Diagram
![Diagram showing the different sensors feeding into the Node-RED pool automation flow](pool-flow-diagram.jpg)

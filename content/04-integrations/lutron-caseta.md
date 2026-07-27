---
title: Lutron Caseta Integration
date: 2026-07-21
---
## Overview
I utilize the Lutron Caseta system to extend lighting and fan control to many different locations in my house.   The Caseta systems uses a bridge to establish communications to the various switches in the deployment. [[02-platforms/index|Home Assistant]] communicates directly to the Caseta bridge over the local network.
### Lutron Caseta Smart Bridge Pro
The original Lutron Smart Bridge works fine when using the Lutron app, but Home Assistant's local integration requires the Pro model.  This is because the Pro model exposes a local Telnet/SSH-style API. Once connected, Home Assistant discovers every switch and fan control tied to that bridge automatically, there is no manual entity configuration needed.
### My Setup
My Caseta setup covers two types of devices:
1. Light switches
	1. Dimmers for bedrooms
	2. On/Off for the patio and sunroom.
2. Fan speed controls in the bedrooms, patio, and sunroom.
### Why Local Connectivity Matters
Because the bridge and HA communicate locally, Caseta switches keep working even during an internet outage.  It is one of the reasons I decided to mix Caseta switches into my automation system.
### Manufacturer Installation Instructions 

![[caseta-advanced-instructions.pdf#page=1]]
*Downloaded on 2026-07-11 from https://assets.lutron.com/a/documents/0301710_caseta_advanced_instructions.pdf.*
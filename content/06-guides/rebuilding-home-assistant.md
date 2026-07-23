---
title: "Guide: Rebuilding Home Assistant From Scratch"
date: 2026-07-22
---
## Overview
This guide documents the  rebuild of the Home Assistant instance from a failing Supervised install to a Docker-based setup on the same hardware.
### Starting Point
Before touching anything, I completed an audit of the existing instance to make sure I captured everything.
- **Last backup before this project**: taken about three years earlier.
- **Failing integration**: Bluetooth, [[../02-platforms/hacs-community-store|HACS]], WiZ, and WLED were all showing "Failed setup, will retry."
- **Leftover config**: A Raspberry Pi Power Supply Checker integration that made no sense on the [[../01-infrastructure/server-hardware|EliteDesk hardware]].
### Take a Full Backup First
Before any destructive change, I took a complete backup and saved it to my laptop. This was meant as a reference if needed during the rebuild.
### Install Ubuntu Server and Docker
Rather than reinstalling Home Assistant OS, Supervised, I installed a base Ubuntu Server on the same hardware and set up Docker to run the [[../01-infrastructure/docker-container-stack|container stack]] — Home Assistant Core, Mosquitto, and Node-RED as separate containers.
### Setup Integrations One at a Time
Rather than restoring the old backup, I reconnected each integration as a fresh install, starting with the ones that had been reliable before (ecobee, Denon, Samsung) and leaving the previously-failing ones (WiZ, WLED, HACS) for a separate reconfiguration effort,  [[troubleshooting-failing-integrations|Troubleshooting Failing Integrations]].
### Rebuild Dashboards
Rather than importing the old dashboard configuration, I rebuilt the Exterior, Game Room, and Master Bedroom area dashboards from scratch.
### Related Reading
- [[../01-infrastructure/server-hardware|Home Server Hardware]]
- [[../01-infrastructure/docker-container-stack|Docker Container Stack]]
- [[troubleshooting-failing-integrations|Troubleshooting Failing Integrations]]

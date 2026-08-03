---
type: "lbr8 Protocol Card"
title: "Local-First Smart Home"
description: "Run all smart home automations locally with Home Assistant and Zigbee2MQTT — no cloud connection required."
tags:
  - "phase-5"
  - "devices"
  - "advanced"
  - "p5"
  - "big-tech-surveillance"
  - "tracking"
  - "infrastructure-dependency"
prerequisites:
  - "cards/smart-device-audit.md"
related:
  - "cards/smart-device-audit.md"
  - "cards/network-segmentation.md"
---

## Steps

### General

Install Home Assistant. Use Zigbee2MQTT for Zigbee devices (no vendor hub needed). All automations run locally — no cloud required. Add devices from your smart-device-audit that can work locally.

## Self-Hosted

Home Assistant (FOSS, runs on any server, supports thousands of devices)

Alternatives: openHAB (older, Java-based)

## Prerequisites

Audit your devices first — know what can work locally before setting up Home Assistant.

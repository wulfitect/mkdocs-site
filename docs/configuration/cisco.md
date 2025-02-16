# Cisco VXLAN-EVPN Configuration Guide

This guide provides a step-by-step configuration for setting up VXLAN-EVPN on Cisco platforms.

## Prerequisites

- Cisco Nexus 9000 Series switches (or similar)
- IOS-XE or NX-OS software with VXLAN/EVPN support
- Underlay network configured (OSPF or IS-IS)

## Step 1: Configure the Underlay Network

```
interface Ethernet1/1
  no shutdown
  ip address 10.0.0.1/31
!
router ospf 1
  network 10.0.0.0/31 area 0
!
```
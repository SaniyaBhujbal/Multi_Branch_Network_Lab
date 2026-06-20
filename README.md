# Multi-Branch CCNA Network Topology

## Project Overview

This project demonstrates a multi-branch enterprise-style network topology designed and configured in Cisco Packet Tracer using CCNA-level networking concepts. The topology includes VLAN segmentation, trunking, and EtherChannel implementation to simulate a scalable and organized headquarters network infrastructure.

The network was divided into multiple departments including Sales, Marketing, Production, and Admin. VLANs were created to logically separate departmental traffic and improve network organization and management.

To increase redundancy and bandwidth between switches, EtherChannel was configured using both PAgP and LACP protocols.

## Technologies Implemented

* VLAN Configuration
* Switchport Assignment
* Trunking
* EtherChannel
* PAgP
* LACP
* Cisco Switch Configuration
* Network Verification Commands

## VLAN Implementation

Department-based VLAN segmentation was implemented across multiple switches. Switch ports were manually assigned to VLANs according to departmental structure.

### Departments

* Sales
* Marketing
* Production
* Admin

## EtherChannel Implementation

### PAgP Configuration

Configured between:

* Switch0 ↔ Switch1
* Switch0 ↔ Switch2

Modes used:

* desirable
* auto

### LACP Configuration

Configured between:

* Switch0 ↔ Switch3
* Switch0 ↔ Switch4

Modes used:

* active
* passive

## Verification Commands

The following commands were used to verify successful configuration:

```bash
show vlan brief
show etherchannel summary
show interfaces trunk
```

## Troubleshooting Experience

During implementation, EtherChannel initially failed to form correctly because of incorrect physical interface connectivity between switches. The issue was identified and resolved by correcting the cable connections and ensuring proper interface consistency between bundled links.

After troubleshooting and reconfiguration, the EtherChannel links successfully formed and displayed operational bundled states (`P`) and Layer 2 status (`SU`) in the verification output.

## Learning Outcome

This project helped strengthen practical understanding of:

* VLAN segmentation
* Switch trunking
* EtherChannel protocols
* Physical and logical troubleshooting
* Multi-switch topology design
* Cisco CLI configuration and verification

## Author

Saniya Bhujbal

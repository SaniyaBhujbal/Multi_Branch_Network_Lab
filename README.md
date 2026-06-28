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


## Final Project Completion Summary

Today the entire multi-branch enterprise network topology was completed successfully after implementing and troubleshooting multiple CCNA networking technologies together in one integrated environment.

The project evolved from a basic VLAN and trunking setup into a complete enterprise-style network containing routing, redundancy, security, dynamic addressing, and protocol redistribution between branches.

### Final Technologies Successfully Implemented

* VLAN Segmentation
* VTP (VLAN Trunking Protocol)
* Trunk Configuration
* Inter-VLAN Routing (Router on a Stick)
* DHCP Configuration
* EtherChannel using:

  * PAgP (Proprietary Protocol)
  * LACP (Open Standard Protocol)
* PVST (Per VLAN Spanning Tree)
* Port Security
* RIP Version 2
* EIGRP
* Route Redistribution between RIP and EIGRP
* NAT Translation between Branch Networks
* Multi-Branch WAN Connectivity
* Redundant Switch Topology

---

## Major Troubleshooting Experience and Lessons Learned

### 1. EtherChannel Troubleshooting

Initially EtherChannel was not forming correctly because:

* physical interfaces between switches were mismatched
* incorrect switch ports were bundled
* some links were configured on only one side

After troubleshooting:

* PAgP was correctly configured in Branch Office 1
* LACP was correctly configured in Branch Office 2
* EtherChannel verification showed operational bundled states `(P)` and Layer 2 operational state `(SU)`

Key lesson:
EtherChannel requires:

* identical switchport configuration
* matching trunk settings
* matching speed/duplex
* correct negotiation modes on both sides

---

### 2. RIP and EIGRP Redistribution Confusion

One major confusion during implementation was understanding why routing tables showed `D` and `D EX` instead of `R` on Branch Office 1 routers.

This issue helped build understanding of route redistribution behavior.

Important realization:

* Branch Office 1 was correctly running RIP
* Branch Office 2 was correctly running EIGRP
* Router0 redistributed routes between both protocols
* Redistributed routes appear as:

  * `D` = EIGRP route
  * `D EX` = External EIGRP route

This clarified that routing tables display how routes are learned, not necessarily every protocol currently running on the router.

---

### 3. NAT Configuration Troubleshooting

NAT initially failed because:

* inside and outside interfaces were assigned incorrectly
* translation verification command was typed incorrectly

After correction:

* Branch Office 1 translated to `212.102.19.1`
* Branch Office 2 translated to `213.102.19.1`

Verification using:

successfully displayed static translations.

---

### 4. PVST and Redundancy Understanding

The project also improved understanding of:

* root bridge election
* spanning-tree forwarding states
* designated ports
* redundant topology behavior

PVST was verified successfully using:

---

## Real-World Networking Skills Improved

This project strengthened practical understanding of:

* Enterprise network hierarchy design
* Redundant topology planning
* Dynamic routing protocols
* Protocol redistribution
* Network troubleshooting methodology
* Cisco CLI confidence
* Verification and debugging commands
* Layer 2 and Layer 3 integration
* Network security implementation
* Realistic branch-office communication design

---

## Biggest Learning Outcome

The biggest lesson from this project was understanding that networking is not just configuration — it is troubleshooting, verification, protocol behavior analysis, and logical problem solving.

Many issues were not caused by syntax errors but by:

* topology design misunderstandings
* protocol interaction confusion
* incorrect interface roles
* negotiation mismatches
* misunderstanding routing behavior after redistribution

Solving these problems built deeper practical networking confidence beyond basic CCNA theory.


## Author

Saniya Bhujbal

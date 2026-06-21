# Router-on-a-Stick and DHCP Configuration

## Project Overview

This project demonstrates:

* VLAN configuration
* Trunking
* EtherChannel
* Router-on-a-Stick
* DHCP configuration
* Inter-VLAN communication

using Cisco Packet Tracer.

---

# Features Implemented

* VLAN 10, 20, 30, 40
* Trunk links between switches
* EtherChannel using PAgP and LACP
* Router-on-a-Stick configuration
* DHCP for automatic IP assignment
* Inter-VLAN routing

---

# Problem Faced

Initially, PCs were receiving:

```bash
169.254.x.x
```

instead of valid DHCP addresses.

Router subinterfaces were showing:

```bash
up/down
```

which indicated VLAN communication failure.

---

# Root Cause

Router-on-a-Stick was configured on the wrong physical interface.

The router was connected to:

```bash
FastEthernet0/1
```

but subinterfaces were mistakenly configured on:

```bash
FastEthernet0/0
```

Additionally, DHCP pools were missing.

---

# Solution

* Reconfigured subinterfaces on the correct router interface
* Configured trunking properly
* Created DHCP pools for all VLANs
* Verified communication using ping tests

---

# Verification

## DHCP Working

PCs successfully received:

* IP Address
* Default Gateway
* Subnet Mask

through DHCP.

## Inter-VLAN Communication

Successfully pinged devices across:

* VLAN 10
* VLAN 20
* VLAN 30
* VLAN 40

---

# Commands Used

```bash
show vlan brief
show interfaces trunk
show etherchannel summary
show ip interface brief
show ip dhcp binding
```

---

# Final Result

Successfully achieved:

* VLAN segmentation
* DHCP automation
* Router-on-a-Stick routing
* Inter-VLAN communication
* Enterprise network redundancy

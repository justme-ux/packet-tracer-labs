# RIP Dynamic Routing Between Two Networks

## Overview
Configured RIP (Routing Information Protocol) between two routers 
to enable automatic route advertisement and communication between 
two separate LAN networks in Cisco Packet Tracer.

## What I Built
- Connected two routers via a serial link (WAN connection)
- Assigned IP addresses to all interfaces (LAN + serial)
- Enabled RIP version 2 on both routers and advertised both networks
- Connected PCs to each router's LAN interface
- Verified full connectivity with ping from 192.168.1.2 to 192.168.2.2

## Network Layout
| Device   | Interface | IP Address      |
|----------|-----------|-----------------|
| Router 1 | Fa0/1     | 192.168.1.1     |
| Router 1 | Se0/1     | 192.168.3.1     |
| Router 2 | Se0/1     | 192.168.3.2     |
| Router 2 | Fa0/1     | 192.168.2.1     |

## Key Commands Used
router rip
version 2
network 192.168.1.0
network 192.168.3.0
no auto-summary

## Skills Demonstrated
- Dynamic routing protocol configuration (RIP v2)
- Interface IP addressing and serial link setup
- Route advertisement and routing table verification
- End-to-end connectivity testing across subnets

## Tools Used
- Cisco Packet Tracer

## Key Concept
Unlike static routing where you manually enter every route, RIP 
automatically shares routing tables between routers every 30 seconds. 
This means if a new network is added, routers learn about it 
automatically — no manual reconfiguration needed.

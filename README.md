# Multi-Network DHCP Relay Lab

## Overview
Designed a 4-router inter-network topology in Cisco Packet Tracer 
where a single centralized DHCP server automatically assigns IP 
addresses to hosts across all four separate networks using DHCP relay.

## What I Built
- Connected 4 routers, each representing a different network subnet
- Placed a DHCP server on Router 1's network (192.168.30.0)
- Configured DHCP relay (ip helper-address) on Routers 0,1, 2, and 3 
  so their connected PCs could receive IPs from the central server
- Verified end-to-end connectivity using ping between all networks

## Skills Demonstrated
- Inter-network routing configuration
- DHCP server setup and IP pool management  
- DHCP relay / ip helper-address configuration
- Subnetting across multiple networks
- Network troubleshooting and verification

## Tools Used
- Cisco Packet Tracer

## Key Concept
Without DHCP relay, a DHCP broadcast from a PC on Network 2 
would never reach the server on Network 1 — routers block 
broadcasts by default. The `ip helper-address` command converts 
the broadcast into a unicast packet forwarded to the DHCP server, 
making centralized IP management possible across multiple networks.

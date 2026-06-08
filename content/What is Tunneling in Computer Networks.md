---
title: What is Tunneling in Computer Networks
draft: false
tags:
  - Networking
---
## What is tunneling

Think of the tunneling as the warping packet inside another packet so it can travel across networks that normally could not carry it, often due to compatibility, routing, or security purposes.
The process is like down below : 

Original Data
     ↓
Inner Packet
     ↓
Outer Packet
     ↓
Internet
     ↓
Remove Outer Packet
     ↓
Original Packet


### Why we need Tunneling

- IPv6 traffic over an IPv4 network
- Private network traffic over the public internet
- Company traffic from home to office securely
- VPN connections
- Cloud networking
- Site-to-site connections


Ex: IPv6 Through an IPv4 Network

Computer A (IPv6)
       |
   IPv4 Internet
       |
Computer B (IPv6)

### Tunnel

It is path on which the packet travelled like ex laptop -> ISP -> VPN Server -> Google or 
Laptop ------- SSH Tunnel ------- Server.

[[NAT vs Tunneling in Networking]]





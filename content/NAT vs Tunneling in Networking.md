---
title: NAT vs Tunneling in Networking
draft: false
tags:
  - Networking
---
NAT it is use to convert private address to public address for accessing internet.

### Problem

let say there are two networks A ( 192.168.1.0/24 ) and B ( 192.168.2.0/24 ) when device from A ( 192.168.1.10 ) want to send data to the device in B ( 192.168.2.50 ) then the NAT does as follows:

    192.168.1.10
        ↓
    203.x.x.x
    
then the packet becomes:
Source: 203.x.x.x
Destination: 192.168.2.50

So the whole internet see 192.168.2.50 as the destination address but problem with that is we expose our private IP ( security ), also the router doesn't know where this private address is so packet get dropped.

"This is why we use tunneling in site to site communication ( one network to another )."

### How Tunneling solve the problem

First it encrypt the IP packet with previous share key the add new IP header and VPN header

So the new IP header consist of the public address A and public address B.
when it receives at B then the new IP header get dropped and the original get used so the packet looks like :
192.168.1.10
      ↓
192.168.2.50

### In Site-To-Site VPN

The process is as follows:

Mumbai Office
     |
VPN Router
     |
Internet
     |
VPN Router
     |
Pune Office


[[What is Tunneling in Computer Networks]]
# Wireshark Analysis — Day 1

## Date
 18 May 2026

## What I Did
- Captured live Wi-Fi traffic using Wireshark
- Applied tcp, dns,filters

## What I Found

### ARP Analysis
- Router IP: 192.168.0.1
- My IP: 192.168.0.102
- Router kept checking if my PC was alive on the network

### DNS Analysis
- Saw CNAME chain for bing.com going through Akamai CDN
- Multiple A records returned = load balancing

## Tools Used
- Wireshark 4.x
- Filters: tcp, dns,dns.qry.type == 1

## Key Learnings
- ARP maps IP addresses to MAC addresses on local network
- DNS CNAME records redirect to CDN servers for speed

# Wireshark Analysis — Day 1

## Date
May 2026

## What I Did
- Captured live Wi-Fi traffic using Wireshark
- Applied tcp, dns, icmp filters
- Analyzed a PCAP file with ICMP ping requests

## What I Found

### ICMP Analysis (icmpreq.pcapng)
- My IPv6: 2406:b400:28:44ba:c062:c65d:3d15:21dc
- Target: 2404:6800:4007:808::200e (Google)
- Sent 4 ping requests — all 4 replied (100% success)
- Sequence numbers: 661, 662, 663, 664

### ARP Analysis
- Router IP: 192.168.0.1
- My IP: 192.168.0.102
- Router kept checking if my PC was alive on the network

### DNS Analysis
- Saw CNAME chain for bing.com going through Akamai CDN
- Multiple A records returned = load balancing

## Tools Used
- Wireshark 4.x
- Filters: tcp, dns, icmp, dns.qry.type == 1

## Key Learnings
- ICMP is used for ping — type 8 = request, type 0 = reply
- ARP maps IP addresses to MAC addresses on local network
- DNS CNAME records redirect to CDN servers for speed
- Sequence numbers track which reply matches which request

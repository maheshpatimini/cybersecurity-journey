# Cybersecurity Commands Cheat Sheet

## Wireshark Filters
- tcp → show all TCP packets
- dns → show all DNS packets
- icmp → show all ping packets
- dns.qry.type == 1 → show only A record lookups
- ip.addr == X.X.X.X → show traffic for specific IP

## Key Port Numbers
- 21 = FTP
- 22 = SSH
- 23 = Telnet
- 25 = SMTP
- 53 = DNS
- 80 = HTTP
- 443 = HTTPS
- 3389 = RDP

## DNS Record Types
- A = returns IP address
- CNAME = returns alias name
- NS = returns name server
- MX = returns mail server

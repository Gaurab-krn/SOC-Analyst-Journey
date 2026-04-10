# Networking Protocols — Notes

## OSI Model (7 Layers)

| Layer | Name | Example Protocols |
|-------|------|------------------|
| 7 | Application | HTTP, FTP, DNS, SMTP |
| 6 | Presentation | SSL, TLS |
| 5 | Session | NetBIOS |
| 4 | Transport | TCP, UDP |
| 3 | Network | IP, ICMP, ARP |
| 2 | Data Link | Ethernet, MAC |
| 1 | Physical | Cables, Wi-Fi |

---

## TCP vs UDP

| Feature | TCP | UDP |
|---------|-----|-----|
| Connection | Connection oriented | Connectionless |
| Reliability | Reliable | Unreliable |
| Speed | Slower | Faster |
| Use case | Web, Email, FTP | Video, DNS, Gaming |

---

## Common Ports (Important for SOC)

| Port | Protocol | Service |
|------|----------|---------|
| 21 | TCP | FTP |
| 22 | TCP | SSH |
| 23 | TCP | Telnet |
| 25 | TCP | SMTP (Email) |
| 53 | UDP/TCP | DNS |
| 80 | TCP | HTTP |
| 443 | TCP | HTTPS |
| 3389 | TCP | RDP (Remote Desktop) |
| 445 | TCP | SMB |
| 8080 | TCP | HTTP Alternate |

---

## Important Protocols for SOC Analysts

### DNS (Domain Name System)
- Converts domain names to IP addresses
- Port 53
- Attackers use DNS tunneling to exfiltrate data

### HTTP vs HTTPS
- HTTP — unencrypted, port 80
- HTTPS — encrypted with TLS, port 443
- SOC analysts look for suspicious HTTP requests

### ICMP (Internet Control Message Protocol)
- Used by ping command
- Attackers use ICMP for reconnaissance

### ARP (Address Resolution Protocol)
- Maps IP address to MAC address
- ARP Spoofing is a common attack

---

## IP Address Basics
### Private IP Ranges
10.0.0.0 - 10.255.255.255
172.16.0.0 - 172.31.255.255
192.168.0.0 - 192.168.255.255
### Special IPs

127.0.0.1 = Localhost (your own machine)
0.0.0.0 = All interfaces
255.255.255.255 = Broadcast




### Private IP Ranges

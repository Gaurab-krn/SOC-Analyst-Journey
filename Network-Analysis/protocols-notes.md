# 🌐 Network Analysis & Protocol Deep Dives

### 📝 Overview
This notebook captures my hands-on analysis of core networking protocols using packet capture (PCAP) tools like Wireshark. Understanding these protocols at the byte level is fundamental to identifying anomalies, unauthorized traffic, and potential cyber attacks.

---

## 🛠️ Core Protocol Breakdown

| Protocol | Port | Layer (OSI) | Key Security Considerations |
| :--- | :--- | :--- | :--- |
| **DNS** | 53 (UDP/TCP) | Application | Watch for DNS Tunneling, massive data exfiltration, or sudden high volumes of NXDOMAIN responses. |
| **HTTP** | 80 (TCP) | Application | Unencrypted traffic. Ideal for extracting cleartext credentials or analyzing web shells/malware drops. |
| **HTTPS** | 443 (TCP) | Application | Encrypted traffic. Requires TLS fingerprinting (JA3) to identify malicious patterns without decryption. |
| **SSH** | 22 (TCP) | Application | Look for brute-force patterns (hundreds of connections from a single IP in seconds). |

---

## 🔍 Wireshark Threat Hunting Lab: Detecting DNS Tunneling

### 📌 Scenario
An internal host is suspected of using DNS traffic to sneak data past the firewall (Data Exfiltration via DNS Tunneling). 

### ⚙️ Wireshark Display Filters Used
To find abnormally large DNS queries, I utilized this filter:
```wireshark
dns.flags.response == 0 && frame.len > 100


📊 Observations & Findings
Anomaly Spotted: Found a massive volume of inbound TXT and AAAA record requests directed to a rogue external nameserver.

Malicious Behavior: The subdomains contained long, random, base64-encoded strings (e.g., bXlzdXBlcnNlY3JldGRhdGE...attacker.com), confirming data staging and exfiltration.

Mitigation: Recommended blocking the rogue destination IP at the perimeter firewall and implementing a maximum character limit on DNS query lengths.

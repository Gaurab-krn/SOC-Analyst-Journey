# 🌐 Network Security Analysis: Defending Against ARP Poisoning

### 📝 Protocol Foundations
Address Resolution Protocol (ARP) maps a dynamic Layer 3 IP address to a physical Layer 2 MAC address. Because standard ARP lacks built-in authentication, it is highly susceptible to spoofing tactics.

---

## 🚀 The Threat: Man-in-the-Middle (MitM) via ARP Spoofing
An adversary sends falsified ARP responses across the local network segment. This tricks the target host into routing all outward traffic directly through the attacker's machine.

### 🔍 How to Spot it in Wireshark
When analyzing a packet capture (`.pcap`), look for duplicate MAC addresses claiming different IP addresses:
```wireshark
arp.duplicate-address-detected


# 🌐 Network Security Analysis: Defending Against ARP Poisoning

### 📝 Protocol Foundations
Address Resolution Protocol (ARP) maps a dynamic Layer 3 IP address to a physical Layer 2 MAC address. Because standard ARP lacks built-in authentication, it is highly susceptible to spoofing tactics.

---

## 🚀 The Threat: Man-in-the-Middle (MitM) via ARP Spoofing
An adversary sends falsified ARP responses across the local network segment. This tricks the target host into routing all outward traffic directly through the attacker's machine.

### 🔍 How to Spot it in Wireshark
When analyzing a packet capture (`.pcap`), look for duplicate MAC addresses claiming different IP addresses:
```wireshark
arp.duplicate-address-detected

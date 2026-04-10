# What is a SOC (Security Operations Center)?

## Definition
A Security Operations Center (SOC) is a centralized team 
responsible for monitoring, detecting, analyzing, and responding 
to cybersecurity incidents within an organization.

---

## SOC Analyst Tiers

| Tier | Role | Responsibilities |
|------|------|-----------------|
| Tier 1 | Alert Analyst | Monitor alerts, triage incidents, escalate |
| Tier 2 | Incident Responder | Investigate escalated incidents |
| Tier 3 | Threat Hunter | Proactively hunt for threats |

---

## Key Responsibilities of a SOC Analyst

- Monitor SIEM alerts (like Splunk, QRadar, Microsoft Sentinel)
- Analyze logs from firewalls, endpoints, servers
- Identify false positives and true positives
- Escalate confirmed incidents
- Document findings and write reports
- Follow incident response playbooks

---

## Common Tools Used in SOC

| Tool | Purpose |
|------|---------|
| Splunk | SIEM - log analysis |
| Wireshark | Network packet analysis |
| Nmap | Network scanning |
| VirusTotal | Malware analysis |
| TheHive | Incident management |
| MISP | Threat intelligence |

---

## Incident Response Steps (IR Lifecycle)

1. **Preparation** — Have tools and playbooks ready
2. **Identification** — Detect and confirm the incident
3. **Containment** — Stop the spread of the attack
4. **Eradication** — Remove the threat completely
5. **Recovery** — Restore systems to normal
6. **Lessons Learned** — Document and improve

---

## Common Attack Types SOC Analysts Deal With

- **Phishing** — Fake emails to steal credentials
- **Brute Force** — Repeated login attempts
- **DDoS** — Overwhelming a server with traffic
- **Malware** — Viruses, ransomware, trojans
- **Insider Threat** — Attack from within the organization
- **Man in the Middle** — Intercepting communications

---

## Important Concepts

### IOC (Indicators of Compromise)
Evidence that a system has been compromised.
Examples: suspicious IP, malicious file hash, unusual domain

### TTPs (Tactics, Techniques and Procedures)
How attackers operate. SOC analysts use the 
**MITRE ATT&CK framework** to understand TTPs.

### False Positive vs True Positive
- **False Positive** — Alert triggered but no real threat
- **True Positive** — Alert triggered and real threat exists

---

*Notes updated as I continue learning SOC concepts*

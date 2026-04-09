---

## Useful SPL (Search Processing Language) Commands

| Command | Description |
|---------|-------------|
| `stats` | Calculate statistics |
| `table` | Display results in table format |
| `top` | Find most common values |
| `rare` | Find least common values |
| `sort` | Sort results |
| `dedup` | Remove duplicate results |
| `rex` | Extract fields using regex |
| `eval` | Create calculated fields |

---

## Common SOC Use Cases in Splunk

### Detect multiple failed logins (Brute Force)
index=* "failed login" | stats count by src_ip | where count > 5
### Detect login outside business hours
index=* "successful login" | eval hour=strftime(_time, "%H")
| where hour < 8 OR hour > 18
### Find large data transfers
index=* | stats sum(bytes) by src_ip | sort -sum(bytes)
---

*Notes updated as I continue learning Splunk*

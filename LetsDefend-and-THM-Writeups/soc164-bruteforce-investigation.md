# 🛡️ Let'sDefend Case Study: SOC164 - Brute Force Detection

### 🚨 Alert Details
* **Event ID:** SOC164
* **Rule Triggered:** Brute Force Attack Detected
* **Target Host:** Production-Server-01
* **Source IP:** `192.168.1.150` (Internal Testing Segment)

---

## 🔍 Investigation Workflow & Log Analysis

### 1. Parsing the SIEM Logs
Upon reviewing the incoming log streams inside the analyst console, I observed an aggressive authentication pattern:
- **Event Pattern:** 45 consecutive failed login attempts targeting the `Administrator` account within a 60-second window.
- **Log Event ID:** Windows Security Event ID `4625` (An account failed to log on).

### 2. Determining the Verdict
- **Analysis:** Looking closer at the source workstation name, it matched an authorized internal vulnerability scanner running a scheduled validation check. 
- **Verdict:** **False Positive** (Authorized security testing activity).

---

## 📝 Action Taken & Containment
1. Verified the activity against the internal security team's maintenance calendar.
2. Documented the source IP as an authorized scanner inside the case notes.
3. Closed the alert ticket cleanly with no further remediation required.

# Lab: Detecting Brute Force and Successful Logins in Splunk

### 🔍 Splunk Search Queries Used
```splunk
index=main EventCode=4625 OR EventCode=4624
| stats count BY EventCode, User, src_ip


Observations & Findings
Anomaly Spotted: Detected 15 failed login attempts (EventCode 4625) followed by a single successful login (EventCode 4624) for user Admin-Test within a 2-minute window.

Analysis: This pattern strongly indicates a successful brute-force attack rather than a user who simply forgot their password.

Action Taken: Marked as high priority. Investigated the source IP reputation and recommended temporary account lockout policies.

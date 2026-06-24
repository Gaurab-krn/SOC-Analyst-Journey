# 🛠️ Local Splunk Enterprise Installation & Log Ingestion

### 📝 Project Overview
To build a functional security monitoring environment, I installed and configured a standalone instance of **Splunk Enterprise** on my local machine. This setup serves as my personal sandbox for testing log ingestion, field extractions, and custom alert rules.

---

## ⚙️ Environment Configuration
* **OS:** Windows 10/11 (Host Machine)
* **SIEM Platform:** Splunk Enterprise (Latest Version)
* **Data Sources Ingested:** Windows Event Logs (Application, Security, System)

---

## 🔍 Step-by-Step Implementation

### 1. Installation & Initial Configuration
- Downloaded and deployed the Splunk Enterprise MSI installer.
- Configured secure local administrator credentials for web console access (`http://localhost:8000`).

### 2. Setting Up Windows Log Ingestion
- Navigated to **Settings > Data Inputs > Local Windows Event Logs**.
- Selected core operational logs vital for SOC analysis:
  * **Security** (Essential for tracking logons, privilege changes, and process creation)
  * **System** (Tracks system reboots, service failures)
  * **Application** (Tracks third-party application errors)

---

## 📊 Next Milestones
- [ ] Configure a Splunk Universal Forwarder to pull logs from a separate Linux virtual machine.
- [ ] Build a custom dashboard tracking failed authentication spikes.

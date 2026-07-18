# 🛡️ SOC Authentication Monitoring Dashboard

A Splunk Enterprise project focused on monitoring Windows authentication events, detecting brute-force attacks, generating alerts, and visualizing security data through an interactive SOC dashboard.

---

# 📌 Project Overview

This project demonstrates how a Security Operations Center (SOC) analyst can collect, analyze, detect, and visualize Windows authentication events using Splunk Enterprise.

Windows Security Event Logs were collected from a Windows 11 virtual machine using Splunk Universal Forwarder and analyzed with Splunk Search Processing Language (SPL).

---

# 🎯 Objectives

- Monitor Successful Windows Logins
- Monitor Failed Windows Logins
- Detect Brute Force Attacks
- Generate Security Alerts
- Build an Authentication Monitoring Dashboard
- Improve Windows Log Visibility

---

# 🏗️ Lab Architecture

```
Windows 11 Virtual Machine
        │
        ▼
Splunk Universal Forwarder
        │
        ▼
Splunk Enterprise
        │
        ▼
Search → Detection → Alert → Dashboard
```

---

# 🛠️ Tools Used

- Splunk Enterprise
- Splunk Universal Forwarder
- Windows 11
- VirtualBox
- Windows Security Event Logs
- SPL (Search Processing Language)

---

# 📊 Event IDs Used

| Event ID | Description |
|----------|-------------|
| 4624 | Successful Logon |
| 4625 | Failed Logon |
| 4672 | Special Privileges Assigned |
| 4688 | Process Creation |

---

# 🚨 Detection Logic

This project detects brute-force login attempts by:

- Excluding SYSTEM accounts
- Excluding Service Accounts
- Excluding Machine Accounts
- Detecting 5 or more failed login attempts within 1 minute

---

# 📈 Dashboard Panels

- Successful Logins
- Failed Logins
- Brute Force Attempts
- Login Activity Trend
- Top Target Users
- Top Source IP Addresses
- Recent Failed Logins

---

# 🎯 MITRE ATT&CK

| Technique | Name |
|-----------|------|
| T1110 | Brute Force |

---

# 📂 Repository Structure

```
SOC-Authentication-Monitoring-Dashboard
│
├── screenshots
├── dashboard_queries
├── report
└── README.md
```

---

# 📸 Screenshots

Screenshots are available in the **screenshots/** folder.

---

# 📝 SPL Queries

All queries used in this project are available in:

```
dashboard_queries/dashboard_queries.txt
```

---

# 💡 Skills Demonstrated

- Splunk SPL
- Log Analysis
- Authentication Monitoring
- Detection Engineering
- Brute Force Detection
- Alert Creation
- Dashboard Development
- Windows Security Event Analysis
- SOC Investigation

---

# ⚠️ Disclaimer

This project was performed in a controlled lab environment for educational and defensive cybersecurity purposes only.

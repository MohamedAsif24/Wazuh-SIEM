# Wazuh-SIEM
Implemented and configured Wazuh File Integrity Monitoring (FIM) on a Windows endpoint to monitor real-time file and registry changes. The setup detects suspicious activities such as file creation, modification, deletion, and Windows Registry changes for security monitoring and SOC analysis.


# 🛡️ Wazuh SIEM Monitoring & File Integrity Monitoring (FIM) Project

## 📌 Project Description

This project demonstrates the implementation of a Security Information and Event Management (SIEM) solution using Wazuh for endpoint monitoring, File Integrity Monitoring (FIM), registry monitoring, threat hunting, and vulnerability assessment on a Windows system.

The environment was configured using a Wazuh Manager and a Windows endpoint agent to monitor suspicious activities, detect file changes in real time, analyze security events, and visualize alerts through the Wazuh Dashboard.

The project focuses on practical SOC (Security Operations Center) monitoring concepts and endpoint security analysis.

---

# 🚀 Features Implemented

## ✅ File Integrity Monitoring (FIM)
Configured Wazuh Syscheck to monitor sensitive directories in real time.

Monitored Path:
```xml
<directories realtime="yes">C:\Users\temp\hacker</directories>
```

Detected:
- File creation
- File modification
- File deletion

Generated real-time alerts when files were added to the monitored directory.

---

## ✅ Windows Registry Monitoring
Configured Wazuh to monitor critical Windows Registry paths.

```xml
<windows_registry realtime="yes">
  HKEY_LOCAL_MACHINE\Security
</windows_registry>
```

The dashboard successfully displayed:
- Registry inventory
- Registry modifications
- Registry monitoring events

---

## ✅ Threat Hunting & Event Analysis
Used Wazuh Threat Hunting dashboard to investigate:
- Endpoint events
- File integrity alerts
- Security events
- MITRE ATT&CK mapped activities

Observed MITRE ATT&CK tactics:
- Defense Evasion
- Privilege Escalation
- Persistence
- Initial Access

---

## ✅ Security Configuration Assessment (SCA)
Performed CIS benchmark assessment on the Windows endpoint.

Policy Used:
```text
CIS Microsoft Windows 11 Enterprise Benchmark v3.0.0
```

Results included:
- Critical vulnerabilities
- High severity findings
- Medium severity findings
- Compliance assessment

This helped identify security misconfigurations in the Windows environment.

---

## ✅ Vulnerability Detection
Analyzed installed software packages and vulnerabilities detected by Wazuh.

Detected applications:
- MySQL Server
- Visual Studio Code
- Oracle VirtualBox
- VLC Media Player

---

# 🧪 Testing Performed

Created test files inside:

```text
C:\Users\temp\hacker
```

Files created:
- hello.txt
- this is a test file.txt

Wazuh successfully generated alerts with:
- Rule ID: 554
- Rule Group: syscheck

Alert Description:
```text
File added to the system
```

---

# 📊 Dashboard Analysis

## 🔹 Events Dashboard
The Events section displayed:
- Real-time file monitoring alerts
- Syscheck events
- File addition activities
- Event timestamps

---

## 🔹 Inventory Monitoring
The Inventory section displayed:
- File inventory
- Windows Registry inventory
- Registry key monitoring

---

## 🔹 Threat Hunting Dashboard
Threat hunting provided:
- MITRE ATT&CK mapping
- Tactics analysis
- Security event visibility
- Endpoint monitoring

---

## 🔹 Vulnerability Detection Dashboard
Displayed:
- Installed packages
- Severity levels
- CIS benchmark compliance
- Vulnerability counts

---

# 🖥️ Endpoint Information

| Field | Value |
|-------|-------|
| Agent Name | Windows-2026 |
| Agent ID | 001 |
| Status | Active |
| Operating System | Windows 11 Pro |
| Wazuh Version | v4.12.0 |

---

# 📂 Project Structure

```bash
wazuh-file-integrity-monitoring/
│
├── README.md
├── configs/
│   └── ossec.conf
│
└── screenshots/
    ├── dashboard.png
    ├── events.png
    ├── inventory.png
    └── vulnerability-detection.png
```

---

# 📷 Screenshots Included
- Wazuh Dashboard Overview
- File Integrity Monitoring Events
- Registry Monitoring
- Threat Hunting
- Vulnerability Detection
- Security Configuration Assessment

---

# 🎯 Learning Outcomes

Through this project, I learned:
- Wazuh architecture and deployment
- File Integrity Monitoring (FIM)
- Syscheck configuration
- Registry monitoring
- Threat hunting workflows
- SIEM event analysis
- Security Configuration Assessment (SCA)
- Vulnerability detection
- MITRE ATT&CK mapping

---

# 🔥 Future Improvements
- Active response integration
- Malware detection
- YARA rule integration
- Linux endpoint monitoring
- Dockerized Wazuh deployment
- Custom alert rules
- Email alert integration

---

# 📌 Conclusion
This project demonstrates practical implementation of Wazuh SIEM for endpoint monitoring, file integrity monitoring, threat hunting, and vulnerability assessment in a SOC environment. It provides hands-on experience in cybersecurity monitoring and real-time security event analysis.


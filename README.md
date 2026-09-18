# Wazuh EDR Home Lab

## Overview

This project documents the deployment and testing of an open-source
Endpoint Detection and Response (EDR) home lab using Wazuh.

The lab was designed to provide hands-on experience with endpoint
security monitoring, event collection, threat detection, file integrity
monitoring, authentication monitoring, vulnerability detection, and
security configuration assessment.

The environment consists of a Wazuh Manager running on Ubuntu and a
Windows 11 endpoint running the Wazuh Agent.

## Lab Objectives

- Deploy and configure a Wazuh security monitoring environment
- Connect a Windows 11 endpoint to the Wazuh Manager
- Monitor endpoint security events
- Detect file system changes using File Integrity Monitoring (FIM)
- Detect failed Windows authentication attempts
- Perform security configuration assessments
- Review endpoint vulnerabilities and security findings
- Gain practical experience with EDR and SIEM concepts

## Lab Environment

| System | Operating System | Purpose |
|---|---|---|
| Wazuh Manager | Ubuntu Linux | Central security monitoring and analysis |
| Wazuh Endpoint | Windows 11 | Monitored client endpoint |

## Technologies Used

- Wazuh
- Ubuntu Linux
- Windows 11
- VMware
- PowerShell
- Windows Event Logs
- CIS Security Benchmarks

## Security Tests Performed

### 1. File Integrity Monitoring
Configured Wazuh to monitor a Windows directory and detect file
creation, modification, and deletion events.

### 2. Failed Windows Logon Detection
Generated controlled failed authentication attempts and verified that
Wazuh detected Windows Event ID 4625.

### 3. Security Configuration Assessment
Used Wazuh Security Configuration Assessment (SCA) to evaluate the
Windows 11 endpoint against CIS security recommendations.

### 4. Vulnerability Detection
Reviewed vulnerabilities identified by Wazuh on the monitored endpoint
and examined their severity and remediation information.
## Key Skills Demonstrated

- Endpoint Detection and Response (EDR)
- Security Information and Event Management (SIEM)
- Windows endpoint monitoring
- File Integrity Monitoring (FIM)
- Windows Event Log analysis
- Failed authentication detection
- Security Configuration Assessment (SCA)
- CIS security benchmark analysis
- Vulnerability detection and remediation analysis
- PowerShell administration
- Security event investigation
- Endpoint security analysis
- Technical security documentation

---
## Project Documentation

Detailed documentation for each stage of the Wazuh EDR home lab is available below:

1. [Lab Architecture](docs/01-lab-architecture.md)
2. [Wazuh Manager Installation](docs/02-wazuh-manager-installation.md)
3. [Windows Agent Deployment](docs/03-windows-agent-deployment.md)
4. [File Integrity Monitoring](docs/04-file-integrity-monitoring.md)
5. [Failed Windows Logon Detection](docs/05-failed-logon-detection.md)
6. [Security Configuration Assessment](docs/06-security-configuration-assessment.md)
7. [Vulnerability Detection](docs/07-vulnerability-detection.md)
8. [Lessons Learned](docs/08-lessons-learned.md)

---

## Repository Structure

```text
wazuh-edr-homelab/
├── README.md
├── docs/
│   ├── 01-lab-architecture.md
│   ├── 02-wazuh-manager-installation.md
│   ├── 03-windows-agent-deployment.md
│   ├── 04-file-integrity-monitoring.md
│   ├── 05-failed-logon-detection.md
│   ├── 06-security-configuration-assessment.md
│   ├── 07-vulnerability-detection.md
│   └── 08-lessons-learned.md
└── screenshots/

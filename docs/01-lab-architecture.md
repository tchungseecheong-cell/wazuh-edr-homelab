# Wazuh EDR Home Lab Architecture

## Overview

This lab was designed to simulate a small endpoint security monitoring
environment using Wazuh.

The environment consists of a centralized Wazuh Manager running on
Ubuntu Linux and a Windows 11 endpoint running the Wazuh Agent.

The Windows endpoint sends security information to the Wazuh Manager,
where events can be analyzed and viewed through the Wazuh Dashboard.

## Lab Components

| Component | Operating System | Role |
|---|---|---|
| Wazuh Manager | Ubuntu Linux | Central security monitoring and analysis server |
| Wazuh Agent | Windows 11 | Monitored endpoint |
| Wazuh Dashboard | Ubuntu/Wazuh Server | Security event visualization and investigation |
| VMware | Virtualization Platform | Hosts the lab virtual machines |

## Lab Architecture

```text
+---------------------------+
|     Windows 11 Endpoint   |
|                           |
|       Wazuh Agent         |
+-------------+-------------+
              |
              | Security Events
              | Endpoint Telemetry
              |
              v
+---------------------------+
|      Wazuh Manager        |
|       Ubuntu Linux        |
|                           |
| - Event Collection        |
| - Security Analysis       |
| - Alert Generation        |
+-------------+-------------+
              |
              v
+---------------------------+
|      Wazuh Dashboard      |
|                           |
| - Security Alerts         |
| - Endpoint Monitoring     |
| - FIM Events              |
| - Authentication Events   |
| - Security Assessment     |
| - Vulnerability Findings  |
+---------------------------+

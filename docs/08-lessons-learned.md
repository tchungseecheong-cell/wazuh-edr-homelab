# Lessons Learned

## Overview

This Wazuh EDR home lab provided hands-on experience deploying, configuring, and testing an endpoint monitoring and security analysis platform.

The project demonstrated how endpoint telemetry can be collected and analyzed to identify security events, configuration weaknesses, and software vulnerabilities.

## Key Lessons Learned

### 1. Endpoint Visibility Is Important

Deploying the Wazuh Agent demonstrated how endpoint telemetry provides security analysts with visibility into activity occurring on monitored systems.

Without centralized monitoring, security events such as authentication failures and file modifications may be difficult to identify and investigate.

### 2. File Integrity Monitoring Can Detect Unexpected Changes

The File Integrity Monitoring exercise demonstrated how Wazuh can monitor selected directories and generate events when files are created, modified, or deleted.

This can help identify unauthorized or unexpected changes to important files.

### 3. Authentication Monitoring Supports Threat Detection

The failed logon detection exercise demonstrated how Windows authentication events can be collected and analyzed by Wazuh.

Repeated authentication failures may indicate user error, misconfigured credentials, or potentially malicious authentication activity that requires investigation.

### 4. Secure Configuration Is an Important Part of Endpoint Security

The Security Configuration Assessment demonstrated that installing security software alone does not guarantee that an endpoint is securely configured.

Comparing the Windows endpoint against the CIS benchmark helped identify security hardening opportunities and configuration weaknesses.

### 5. Vulnerability Management Complements Endpoint Monitoring

The Vulnerability Detection exercise demonstrated how software inventory information can be used to identify applications that may be affected by known vulnerabilities.

Vulnerability findings can help administrators prioritize patching, software upgrades, and removal of unnecessary vulnerable applications.

### 6. Security Tools Require Investigation and Context

One of the most important lessons from the project was that security alerts and assessment results require analysis.

An alert does not automatically mean that a system has been compromised. Analysts must review the event, understand the context, determine the potential risk, and decide whether remediation is required.

## Skills Developed

This project provided practical experience with:

- Wazuh Manager deployment
- Wazuh Agent deployment and configuration
- Windows endpoint monitoring
- File Integrity Monitoring (FIM)
- Windows authentication event monitoring
- Security Configuration Assessment (SCA)
- CIS security benchmarks
- Vulnerability Detection
- Syscollector
- PowerShell
- Security event investigation
- Endpoint security analysis
- Vulnerability and configuration remediation concepts
- Technical documentation
- GitHub project documentation

## Future Improvements

The lab could be expanded in the future by:

- Adding additional Windows and Linux endpoints
- Creating custom Wazuh detection rules
- Integrating threat intelligence sources
- Testing additional Windows security events
- Monitoring network-based security events
- Performing additional endpoint hardening
- Investigating vulnerability remediation in greater detail
- Integrating Wazuh with other security tools
- Building automated alerting and notification workflows

## Conclusion

This project provided practical experience with several core concepts used in endpoint security monitoring and security operations.

By deploying Wazuh and performing controlled security tests, the lab demonstrated how endpoint telemetry can be used to detect file changes, authentication failures, configuration weaknesses, and software vulnerabilities.

The project also reinforced the importance of combining security monitoring with investigation, vulnerability management, system hardening, and clear technical documentation.

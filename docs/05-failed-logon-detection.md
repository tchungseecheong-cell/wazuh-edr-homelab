# Failed Windows Logon Detection

## Overview

This stage of the Wazuh EDR home lab demonstrates the detection and investigation of failed Windows authentication attempts.

Windows records unsuccessful logon attempts in the Security event log. The Wazuh Agent can collect these security events and forward them to the Wazuh Manager for analysis and investigation.

This test demonstrates how endpoint authentication activity can be monitored using Wazuh.

## Objective

The objectives of this test were to:

- Generate controlled failed logon attempts on the Windows 11 endpoint
- Verify that Windows recorded the authentication failures
- Confirm that Wazuh detected the failed authentication activity
- Review the generated security event in the Wazuh Dashboard
- Demonstrate authentication monitoring using an EDR/SIEM platform

## Test Environment

| Component | Configuration |
|---|---|
| Endpoint | Windows 11 |
| Endpoint Agent | Wazuh Agent |
| Manager | Wazuh Manager |
| Manager OS | Ubuntu Linux |
| Log Source | Windows Security Event Log |
| Windows Event ID | 4625 |
| Test Type | Controlled failed authentication attempt |

## Test Methodology

Controlled failed authentication attempts were generated on the Windows 11 endpoint.

Windows records unsuccessful account logon attempts in the Security event log as Event ID `4625`.

The Wazuh Agent monitored the Windows security events and forwarded relevant event information to the Wazuh Manager for analysis.

The Wazuh Dashboard was then used to investigate the authentication activity.

## Expected Result

The Windows endpoint should record the failed authentication attempt and Wazuh should provide visibility into the corresponding security event.

The event should provide information that can assist with investigating unsuccessful authentication activity.

## Security Relevance

Monitoring failed authentication attempts can help identify suspicious account activity, including repeated password guessing, unauthorized access attempts, and other abnormal authentication behavior.

Security analysts can use authentication logs alongside other endpoint and network telemetry when investigating potential security incidents.

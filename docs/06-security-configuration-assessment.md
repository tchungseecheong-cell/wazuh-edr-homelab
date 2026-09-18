# Security Configuration Assessment (SCA)

## Overview

This stage of the Wazuh EDR home lab demonstrates the use of Wazuh Security Configuration Assessment (SCA) to evaluate the security configuration of the Windows 11 endpoint.

Wazuh SCA performs configuration checks against security policies and benchmarks, allowing potential configuration weaknesses and compliance issues to be identified.

## Objective

The objectives of this assessment were to:

- Review the Security Configuration Assessment results for the Windows 11 endpoint
- Evaluate the endpoint against the applicable CIS benchmark
- Identify passed and failed security configuration checks
- Investigate selected failed security checks
- Understand how configuration weaknesses can increase endpoint security risk
- Identify potential remediation actions

## Test Environment

| Component | Configuration |
|---|---|
| Endpoint | Windows 11 |
| Endpoint Agent | Wazuh Agent |
| Manager | Wazuh Manager |
| Manager OS | Ubuntu Linux |
| Assessment Feature | Security Configuration Assessment (SCA) |
| Security Benchmark | CIS Microsoft Windows 11 Enterprise Benchmark v1.0.0 |

## Assessment Methodology

The Wazuh Security Configuration Assessment module was used to evaluate the Windows 11 endpoint.

The assessment compared the endpoint configuration against security checks defined by the applicable CIS benchmark.

The results were reviewed through the Wazuh Dashboard to identify passed and failed configuration checks.

Selected failed checks were then investigated to better understand the associated security risk and potential remediation.

## Expected Result

The assessment should identify security configuration checks that pass or fail against the selected benchmark.

Failed checks can then be reviewed to determine whether configuration changes are required to improve the security posture of the endpoint.

## Security Relevance

Security Configuration Assessment helps identify insecure or non-compliant system configurations.

Configuration weaknesses can increase the attack surface of an endpoint and may make systems more susceptible to unauthorized access, privilege abuse, credential attacks, or other security threats.

Using established security benchmarks provides a structured approach for evaluating and improving endpoint security configurations.

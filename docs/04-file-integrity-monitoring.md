# File Integrity Monitoring (FIM)

## Overview

This stage of the Wazuh EDR home lab demonstrates File Integrity
Monitoring (FIM) on the Windows 11 endpoint.

Wazuh File Integrity Monitoring can detect changes to monitored files
and directories, providing visibility into file creation, modification,
and deletion activity.

## Objective

The objectives of this test were to:

- Configure a directory for file integrity monitoring
- Create a controlled test file
- Modify the test file
- Verify that Wazuh detected the file system changes
- Investigate the generated event in the Wazuh Dashboard

## Test Environment

| Component | Configuration |
|---|---|
| Endpoint | Windows 11 |
| Endpoint Agent | Wazuh Agent |
| Manager | Wazuh Manager |
| Manager OS | Ubuntu Linux |
| Monitoring Feature | File Integrity Monitoring |
| Test Directory | C:\Wazuh-FIM-Test |

## Test Methodology

A dedicated test directory was created on the Windows 11 endpoint.

The directory was added to the Wazuh Agent File Integrity Monitoring
configuration.

Controlled file operations were then performed to determine whether
Wazuh successfully detected changes within the monitored directory.

## Expected Result

Wazuh should generate file integrity monitoring events when files
inside the monitored directory are created, modified, or deleted.

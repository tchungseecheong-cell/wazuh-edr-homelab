# Wazuh Manager Installation

## Overview

The first stage of the Wazuh EDR home lab involved deploying the
Wazuh Manager on an Ubuntu Linux system.

The Wazuh Manager acts as the central security monitoring platform
for the lab. It receives security information from monitored
endpoints, analyzes events, generates alerts, and provides access
to security information through the Wazuh Dashboard.

## Environment

| Component | Configuration |
|---|---|
| Operating System | Ubuntu Linux |
| Security Platform | Wazuh |
| Role | Wazuh Manager / Security Monitoring Server |
| Endpoint | Windows 11 |
| Virtualization | VMware |

## Step 1 - Add the Wazuh GPG Key

The Wazuh repository signing key was added to the Ubuntu system.

The key allows the package manager to verify that Wazuh packages
are authentic and have not been modified.

The following command was used:

```bash
curl -s https://packages.wazuh.com/key/GPG-KEY-WAZUH | \
sudo gpg --dearmor -o /usr/share/keyrings/wazuh-archive-keyring.gpg
```

## Step 2 - Download the Wazuh Installation Script

The Wazuh installation script was downloaded from the official
Wazuh package repository.

```bash
curl -sO https://packages.wazuh.com/4.12/wazuh-install.sh
```

## Step 3 - Install Wazuh

The installation script was executed with administrative privileges.

```bash
sudo bash ./wazuh-install.sh -a -i
```

The installation process configured the required Wazuh components
and services.

After installation completed, administrator credentials were
generated for accessing the Wazuh Dashboard.

> Security Note: Administrator passwords and authentication
> credentials should never be stored in a public GitHub repository.

## Step 4 - Identify the Wazuh Server IP Address

The Ubuntu system's network configuration was checked using:

```bash
ip a
```

This identified the IP address assigned to the Wazuh Manager.

The address was then used by other systems in the lab to communicate
with the Wazuh server and to access the dashboard.

## Step 5 - Access the Wazuh Dashboard

The Wazuh Dashboard was accessed from a web browser using the IP
address of the Wazuh Manager.

```text
https://<WAZUH-MANAGER-IP>
```

The administrator credentials generated during installation were
used to authenticate to the dashboard.

## Installation Verification

Successful installation was verified by confirming that:

- The Wazuh installation completed successfully
- The Wazuh services were running
- The Wazuh Manager had network connectivity
- The Wazuh Dashboard was accessible through a web browser
- Administrator authentication to the dashboard was successful

At this stage, the Wazuh Manager was ready to receive security
information from monitored endpoints.

## Next Step

The next stage of the project involved installing the Wazuh Agent
on a Windows 11 endpoint and registering the endpoint with the
Wazuh Manager.

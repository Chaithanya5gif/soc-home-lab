## 🖥️ Lab Environment

**Virtualization Platform:** [VMware Workstation / VirtualBox / Proxmox]

| Component        | OS / Version              | Role                                      |
|-------------------|----------------------------|--------------------------------------------|
| Splunk Server     | [Ubuntu 22.04 / Windows]  | Log aggregation, saved searches, dashboards |
| Wazuh Server      | [Ubuntu 22.04]             | SIEM manager, agent management, alerting  |
| Endpoint (Agent)  | [Windows 10/11]           | Monitored host running Wazuh agent        |
| Attacker Machine  | [Kali Linux]               | Used to simulate brute-force / attack traffic |

**Network Setup:**
- All VMs deployed on an isolated internal/NAT network ([e.g., 192.168.X.0/24])
- Wazuh Manager: `[IP address]`
- Splunk Server: `[IP address]`
- Endpoints forward logs to Wazuh Manager via Wazuh Agent

**Resource Allocation:**
- [X] GB RAM / [X] vCPUs per VM (adjust based on your host machine)

**Reproduction Steps (high-level):**
1. Deploy Wazuh Manager and enroll agent(s) on endpoint VM(s)
2. Install and configure Splunk, forward relevant logs via [Splunk Universal Forwarder / syslog]
3. Simulate attack traffic from Kali (e.g., SSH brute-force via Hydra/Metasploit)
4. Validate detection in Wazuh dashboard and cross-reference with Splunk saved searches
5. Map triggered alerts to corresponding MITRE ATT&CK techniques

# SOC Home Lab

## Overview

This project demonstrates a basic SOC (Security Operations Center) Home Lab using Splunk and Wazuh.

## Tools Used

* Splunk Enterprise
* Wazuh SIEM
* Kali Linux
* Windows 11
* MITRE ATT&CK Framework

## Splunk Activities

* Daily Event Volume Analysis
* Brute Force Detection
* Saved Searches
* SOC Dashboard Creation

## Wazuh Activities

* Agent Deployment
* Threat Hunting
* Custom Rule Creation
* Custom Alert Generation

## MITRE ATT&CK Mapping

Security events were mapped to MITRE ATT&CK techniques for threat detection and analysis.

## Screenshots

Screenshots are included for all completed lab activities.

## Author

Vaishak VJ
Cyber Security Student

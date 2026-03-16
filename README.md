# Wazuh SIEM Security Monitoring Lab

## Overview

This project demonstrates the deployment of a Wazuh SIEM environment and detection of simulated cyber attacks.

The lab includes:

- Wazuh SIEM deployment
- SSH brute force attack simulation using Hydra
- Security event monitoring
- Log analysis

---

## Lab Architecture

Kali Linux (Attacker)  
        ↓  
SSH Brute Force Attack (Hydra)  
        ↓  
Ubuntu Server (Wazuh Agent)  
        ↓  
Wazuh Manager & Indexer  
        ↓  
Wazuh Dashboard (Security Monitoring)
---

## Tools Used

- Wazuh SIEM
- Kali Linux
- Hydra
- OpenSSH
- VMware

---


## Attack Simulation

### SSH Brute Force Attack

The Hydra tool was used from Kali Linux to simulate a brute force attack against the SSH service running on the monitored Ubuntu server.


Command used:

hydra -l anshika -P passwords.txt ssh://192.168.72.148

---

## Results

Wazuh successfully detected multiple failed SSH login attempts and generated security alerts in the dashboard.
Security alerts were visible in the Wazuh Dashboard under the Authentication events section.

## Screenshots

### Hydra Brute Force Attack

![Hydra Attack](screenshots/hydra-attack.png)

### Wazuh Detection Alert

![Wazuh Alert](screenshots/wazuh-alert.png)

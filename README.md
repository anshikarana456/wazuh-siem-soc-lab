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

## Attack Demonstration

### Kali Attacker Machine

![Kali IP](screenshots/kali-ip.png)

### SSH Service Running on Target

![SSH Service](screenshots/ssh-service-running.png)

### Password Wordlist

![Password Wordlist](screenshots/password-wordlist.png)

### Hydra Brute Force Attack

![Hydra Attack](screenshots/hydra-attack.png)

### Wazuh Alert Detection

![Wazuh Alert](screenshots/wazuh-alert.png)


## Threat Detection Mapping (MITRE ATT&CK)

The simulated attack in this lab aligns with the following MITRE ATT&CK technique:

| Attack Technique | MITRE ID | Description |
|-----------------|----------|-------------|
| SSH Brute Force | T1110 | Attempting multiple password combinations to gain unauthorized access |

Wazuh SIEM detects this behavior by monitoring authentication logs and identifying multiple failed login attempts.

# SSH Brute Force Attack Simulation

## Description

Hydra was used to simulate an SSH brute force attack against the monitored Ubuntu server.

## Command

hydra -l anshika -P passwords.txt ssh://192.168.72.148

## Result

Multiple failed authentication attempts were detected by Wazuh SIEM.

The alerts were visible in the Wazuh Dashboard under Security Events.

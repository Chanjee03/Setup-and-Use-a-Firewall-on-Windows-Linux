# Setup-and-Use-a-Firewall-on-Windows-Linux
A firewall configuration project for Linux (using UFW) and Windows (using built-in firewall). Implements port blocking, SSH allowance, rule verification, connectivity testing, and restoration of settings to demonstrate practical network security management across both operating systems.
# Firewall Configuration Project for Linux & Windows

## Overview

This project demonstrates practical firewall rule management on **Linux** and **Windows** operating systems. It includes tasks for configuring, testing, and restoring firewall settings to secure network traffic by controlling port access.

---

## Supported Platforms

- **Linux**: Using **UFW (Uncomplicated Firewall)**
- **Windows**: Using **Windows Defender Firewall**

---

## Linux Firewall Configuration (Using UFW)

### Tasks:

1. List current firewall rules.
2. Block inbound traffic on port 23 (Telnet).
3. Test blocking of port 23 using `netcat`.
4. Allow SSH traffic on port 22.
5. Remove test blocking rule to restore original state.

### Key Commands:

```bash
sudo ufw status numbered
sudo ufw deny 23
nc -vz localhost 23
sudo ufw allow 22/tcp
sudo ufw delete <rule_number>
sudo ufw status

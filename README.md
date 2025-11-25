# SOC Firewall Analysis Project

## Overview
This is a SOC oriented project that simulates attacker activity against a target workstation. The goal of this project is to demonstrate skills such as traffic monitoring, log analysis, and attack detection. It also aims to provide insight as to what SOC analysts might come across when monitoring firewall logs. 

---

## Lab Environment

- **Attacker**: Kali VM (used to perform various scans, reconnaissance, and brute-force simulation)
- **Target**: Windows VM (acts as the target device, used to bring up pfsense web interface GUI)
- **Firewall:** pfSense (monitors and blocks traffic, log events)
- **Network topology:** Kali VM > pfSense > Windows VM

---
**All IPs in this project are masked for privacy.**
---

## Tools and commands used
| Tool | Purpose |
|------|---------|
| Nmap | Port scanning, OS detection, TCP scans |
| Nikto | Web server vulnerability scanning |
| Hydra | Brute force attack through SSH and RDP |
| pfSense | Firewall used to create rules, logging, and traffic analysis |

**Sanitized command examples:**
# Nmap commands
- nmap -sS \<Target IP\>
- nmap -O '<Target IP>"

# Nikto command
nikto -h '<Target IP>'

# Brute Force commands
- hydra -V -l '<Target-hostname' -P /home/<Target-hostname>/Documents/passlist.txt **rdp**://'<Target IP>'
- hydra -V -l '<Target-hostname>' -P /home/<Target-hostname>/Documents/passlist.txt **ssh**://'<Target IP>'


**Summary** 
---
An OS detection scan was sent from the attacker machine (Kali) to the target windows machine. This type of scan 
sends multiple packets so that it could indentify the OS the target machine is running. 

**Indicators in pfSense**
---
- **TCP:A** - pfSense was able to identify an incoming SYN packet interpreted as ACK
- All traffic blocked by firewall rules
- Nmap -O is noisy because it sends multiple probes/packets to the target machine, which will usually result in multiple
  logs. As we can see in "nmap -O raw logs" and "nmap -O dynamic logs", there are multiple logs in pfSense system logs.

**MITRE ATT&CK**
---
- Tactic: Reconnaissance
- Technique: Network Service Scanning and Vulnerability Scanning

**Impact Assessment**
---
- **Severity: Medium**
- Scans and detects which OS the target machine is on. This is dangerous because now hackers can change their attack path and
  use exploits they know will work on that OS.

**Recommendations**
---
- Enable IDS/IPS rules to detect OS fingerprinting
- Block unnecessary ICMP traffic



    

  


**Summary**
---
A security vulnerability scan was initiated on the target Windows machine. Nikto was used to find any vulnerabilties
in web servers or applications. *This Windows VM does not have a web server so it results in zero host found when doing
the nikto scan.*

**Indicators in pfSense**
---
- Multiple logs to port 80 (no web server)
- Burst of TCP:RA protocols
- Quick successions of logs in pfSense

**MITRE ATT&CK**
---
- Tactic: Reconnaissance
- Technique: Vulnerability Scanning

**Impact Assessment**
- **Severity: Medium**
- 

**Summary**
---
The Kali machine used Hydra to performed a brute force attack using SSH. The attack uses a list of passwords
from a notepad and attempts to log-in in quick succession. SSH is usually used when attackers want quick access 
to the terminal once they have compromised the target machine. 

**Indicators in pfSense**
---
- Multiple logs blocked from port 22 as seen in the dynamic and raw logs
- Multiple logs appeared back to back indicating multiple failed attempts
- 

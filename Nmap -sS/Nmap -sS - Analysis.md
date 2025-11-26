**Summary**
---
A SYN scan was initiated from the attacker machine onto the target Windows machine to perform reconnaissance. 
Kali used a stealither version of nmap, to go undetected. This technique uses -sS which stops before completing 
the TCP handshake, but pfSense was able to block and log an attack.

**Indicators in pfSense**
---
- **TCP:A** - Incoming SYN packet interpreted as ACK.
- All traffic blocked by firewall rules

**Impact Assessment**
---
- **Severity: Low**
- Although an attempt of reconnaissance was performed, pfSense only logged one attempt, meaning high volume scans
  were not performed. As we can from the "nmap -sS kali command" picture, it was still able to identify some open ports
  so we should still be cautious and continue to monitor.

  **Recommendations**
  ---
  - Monitor for repeated reconnaissance attempts
  - Enable IDS/IPS rules to detect SYN scan patterns

<img width="1137" height="657" alt="destination ports" src="https://github.com/user-attachments/assets/20f94fff-1470-425d-b923-765106b6aeee" />

**Analysis**
---
The pfSense graph shows multiple ports being probed by outside the network. Ports 22 (SSH) and 3389 (RDP), which are common ports 
associated with remote access, appears on the list suggesting some sort of remote access attack was attempted. Uncommon ports such as 
1 and 53294 also makes an appearance on the chart, indicating some type of scanning of the internal network.

**Observed Behavior**
---
- Port 3389 and 22 has notable high traffic, brute force attempts most likely occured
- Port 135 was targeted (WAN > LAN) which probably means a vulnerability scan attack attempt
- Port 1 indicates scanning
- Port 53294 most likely indicates scanning

**Potential Security Implications**
---
- Brute Force attempts using SSH and RDP services
- Reconnaissance scanning suggested by port 1 and 53294
- Vulnerability scanning

**Recommendations**
---
- Enable IDS/IPS rules to detect scanning and brute force behavior
- Apply rate limiting for repeated attempts on remote access ports
- Strengthen internal hosts by disabling unused services and ensuring up-to-date patches

**Conclusion**
---
Many different ports that are usually targeted for malicious behavior were present on the destination pie chart. This highly suggests
that there is an attack coming from outside the network. To reduce exposure and protect internal systems, setting up IDS/IPS rules, applying 
rate limiting on remote access ports, restricting unnecessary services, and continued/strengthened monitoring should be applied. 

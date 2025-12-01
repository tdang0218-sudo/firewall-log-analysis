<img width="1137" height="657" alt="destination ports" src="https://github.com/user-attachments/assets/20f94fff-1470-425d-b923-765106b6aeee" />

**Summary**
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

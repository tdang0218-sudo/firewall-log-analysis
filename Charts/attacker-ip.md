<img width="1138" height="563" alt="ips blocked" src="https://github.com/user-attachments/assets/38db515a-8578-41a7-a747-41941505fa5a" />

**Analysis**
---
The pfSense dashboard shows source IPs that the firewall has logged. We can see that one IP (redacted) in particular
has been logged more than others. This indicates that the particular IP source is generating large amount of activity
towards the network. 

**Observed Behavior**
---
- A particular IP source (Kali) is accounted for most of the traffic volume
- The other IP sources are barely contributing to traffic volume

**Security Implications**
---
- Scanning or probing activity
- Repeated connection attempts via brute force
- Vulnerability scanning

**Recommendations**
---
**1.** Investigate the IP source with the highest traffic volume  
**2.** Block or restrict the IP  
**3.** Configure IDS/IPS to automatically block malicious behavior from IP  
**4.** Disable unnecessary services on WAN  
**5.** Limit number of connections for that particular IP

**Conclusion**
---
One IP in particular is generating an unusual amount of traffic. The high amount of traffic is concerning since it can
implicate malicious activities such as brute force attempts and various attacks such as probing and vulnerability scanning. 
To keep assets within internal network safe, the IP source should be investigated and if need be, appropriate actions should
take place such as, blocking the IP, disabling unnecessary services on WAN, and limiting the number of connections for that IP.

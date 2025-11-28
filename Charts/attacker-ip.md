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

**

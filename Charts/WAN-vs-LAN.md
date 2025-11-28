<img width="1139" height="537" alt="WAN vs LAN" src="https://github.com/user-attachments/assets/4403b481-2bda-4831-8383-e88153c0b8ac" />

**Analysis**
---
The chart shown in pfSense shows more traffic originating from WAN than LAN. This indicates that an attack is 
originating from outside the network and is attacking an asset on the internal LAN.

**Observed Behavior**
---
- WAN traffic unusually high compared to LAN traffic.
- LAN traffic mostly low, this most likely suggests that the LAN host was responding to attack pings.

**Potential Security Implications**
---
- External reconnaissance
- Brute-force or login attempts
- Probing for exploitable services

**Recommendations**
---
**1.** Review firewall logs for source IP, destination ports, and connection attempts  
**2.** Enable IDS/IPS for WAN to LAN activities  
**3.** Apply rate limiting on WAN services to prevent rapid connection attempts

**Conclusion**
---
Heavy WAN traffic compared to LAN indicates that external network attacks might be occuring.
Possible reconnaissance, brute force, or probing might be occuring, so it's best to review firewall
logs, enable IDS/IPS for WAN to LAN activities, and apply rate limiting to protect assets within the 
network. 













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
1. 







This is a chart shown in pfSense. We can see here that there is much more WAN traffic than LAN. In the 
lab set up, Kali was placed on the WAN interface (em0) and Windows on LAN (em1), sitting between them 
was pfSense. If we were to look at this from a SOC analyst perspective, we can conclude that this chart 
indicates that an attack is happening outside of the network. This lines up with the type of scans we did
against the Windows machine, such as Nmap scans, Nikto scans, and Hydra brute force attempts. By knowing 
that there is heavy traffic coming from outside the network, SOC analysts can recommends certain type of 





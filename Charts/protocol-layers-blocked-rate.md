<img width="1137" height="528" alt="protocols blocked" src="https://github.com/user-attachments/assets/4570d1ff-d230-4d0b-9f6e-9fabc35a5eb6" />

**Analysis**
---
The graph above shows the type of protocols pfSense has blocked. Most of the recorded attacks were TCP, which lines up with the
destination ports seen in earlier pictures. Some ports that were recorded included 22, 3389, 1, and 135 which indicates brute force
attempts, scanning, and reconnaissance which are all attacks that uses TCP.

**Observed Behavior**
---
- TCP makes up the majority of blocked protocols

**Potential Security Implications**
---
- Brute force attacks using SSH and RDP was attempted
- Scanning of internal network
- Vulnerable scanning to find exploitable services

**Recommendations**
--- 
- Enable IDS/IPS rules to detect scannings and high volume of attempted login
- Continue monitoring blocked protocols to see if pattern changes

**Conclusion**
---
Multiple attacks using TCP protocols were initiated, hence why the graph mostly shows TCP being blocked. Strengthening monitoring, enabling
IDS/IPS rules, and limiting exposure of high risk services will help keep internal network strong.

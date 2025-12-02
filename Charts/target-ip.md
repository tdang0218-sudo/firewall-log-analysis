<img width="1140" height="610" alt="target ips" src="https://github.com/user-attachments/assets/7a416d94-262f-4d8a-9c0b-07327b88b271" />

*Note:* The two Windows IP entries should be treated as a single host. One of the Kali attack runs included a mistyped target IP, 
which caused pfSense to register an additional Windows IP. For analysis purposes, please disregard the duplicate and assume both
entries represent the same Windows machine moving forward.

**Analysis**
---
The pfSense destination chart shows the internal IP that was pinged during the external attack. According to the graph, there is one IP
in particular that seems to be dominating. This suggets that this specific IP is being targeted by an attacker outside the network.

**Observed Behavior**
---
- One destination IP is receiving way more data points compared to others
- One other IP was recorded but it's not generating as much data points

**Potential Security Implications**
---
- Large data points for the same IP suggests a brute force attack may be happening
- Reconnaissance may also be happening
- Possibility of web vulnerability probing happening since it generates a lot of traffic
- Lateral movement may be a possibility if target IP was compromised

**Recommendations**
---
- Isolate and harden targeted host in case it might've been compromised
- Implement MFA (multi-factor authentication) to keep host more secured
- Review system logs on targeted host to see if any lateral movement or privilege escalation occured
- Monitor host very closely to see if any suspicious activities occurs

**Conclusion**
---
The high volume of data points for a single IP suggests that the IP is being targeted, and attacks such as brute force, reconnaissance,
and web vulnerability scanning was most likely attempted on the host. In order to keep the host and internal network safe, it is highly 
suggested that the host be isolated from the network, harden security through MFA, review system logs, and monitor for any suspicious changes.

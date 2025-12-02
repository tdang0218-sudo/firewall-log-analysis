<img width="1140" height="610" alt="target ips" src="https://github.com/user-attachments/assets/7a416d94-262f-4d8a-9c0b-07327b88b271" />

*Note:* The two Windows IP entries should be treated as a single host. One of the Kali attack runs included a mistyped target IP, which caused pfSense to register an additional Windows IP. For analysis purposes, please disregard the duplicate and assume both entries represent the same Windows machine moving forward.

**Analysis**
---
The pfSense destination chart shows the internal IP that was pinged during the external attack. There is one IP that 

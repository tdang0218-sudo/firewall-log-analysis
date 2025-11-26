**Summary**
---
A SYN scan was initiated from an attacker onto the target Windows machine to perform reconnaissance. 
The attacker used a stealither version of nmap, likely to go undetected. This technique uses -sS which stops 
before completing the TCP handshake, but pfSense was able to block and log an attack.


**Indicators in pfSense**
TCP:S

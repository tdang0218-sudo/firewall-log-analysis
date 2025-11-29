<img width="800" height="583" alt="firewall rule blocks" src="https://github.com/user-attachments/assets/7b57264e-d9a0-4dc3-bdc8-7b9ac3b7ab42" />

**Analysis**
---
The pfSense dashboard shows a pie chart of the block rate logged. As we can see from the image above, pfSense has a 100% block
rate against incoming traffic, meaning that the firewall rules are successfully blocking the attacks.

**Observed Behavior**
---
- Ninety two instances of traffic were initiated and pfSense was able to block all ninety two.

**Potential Security Implications**
---
- The firewall rules in place are successfully blocking traffic, keeping the network safe
- There are default deny rules in place, which means some sort of attack is coming from outside the network

**Recommendations**
---
- Maintian current firewall rules and maybe add new ones since we know an attempt of an attack is happening
- Enable IDS/IPS to detect patterns in blocked traffic, which may indicate targeted attacks
- Confirm with internal hosts inside the network to see if they are attempting outbound connections which may be causing the
  blocked traffic

**Conclusion**
---
The 100% block rate shows us that pfSense default deny rule is working and it is protecting attacks from outside the network.
In order to further keep a 100% block rate in the future, it would be beneficial to add new default deny rules to cover bases for
new attacks. Continued monitoring of the block rate chart is also recommended.

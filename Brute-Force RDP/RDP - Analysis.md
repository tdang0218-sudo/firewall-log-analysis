**Summary**
---
Hydra was used to attempt brute force RDP on the target machine. Just like the SSH brute force, the RDP attack used a list of passwords
in a notepad and tries to log-in in quick succession. RDP attempts many connections over port 3389 and is usually used when an
attacker wants full GUI desktop access.

**Indicators in pfSense**
---
- **TCP:S** - new RDP connections
- Port 3389 blocked as seen in raw and dynamic logs
- Many connection attempts from the same IP
- Multiple logs generated in quick succession

**MITRE ATT&CK**
---
- Tactic: Credential Access
- Technique: Brute Force

**Impact Assessment**
---
**Severity: High**
- Just like SSH, RDP can be dangerous if a log-in attempt is successful. The difference with RDP though is when a brute force attack is
  successful, the attacker has full access to the GUI desktop, making it much more easy for low level hackers and overall giving
  more options to attacks.

  **Recommendations**
  - 

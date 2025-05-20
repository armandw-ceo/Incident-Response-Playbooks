# 🛡️ Data Exfiltration Incident Response Playbook

## 🔍 1. Detection

### ✅ Detection Checklist
- Access of sensitive file outside of normal operating hours
- DLP (Data Loss Prevention) tool triggers on sensitive file movement
- Unusual outbound network traffic (e.g., cloud uploads, FTP/SFTP, Tor)
- Detection of known exfiltration tools or malware (e.g., C2 communication)
  
---

## 🧪 2. Investigation

### Key Actions:
- Identify systems or users involved 
- Determine what data was accessed or copied
- Analyze outbound traffic destinations, volume, and protocols
- Match access times with user working hours or behavioral baselines
- Review file-level access logs
- Search for tools used to compress, encrypt, or stage data for exfil

---

## 🚨 3. Containment

- Block ongoing data transfers or exfiltration channels (e.g., FTP, cloud app access)
- Isolate affected systems
- Disable compromised user account or accounts
- Revoke API tokens or third-party app integrations
- Quarantine any malware or staging scripts
- Restrict egress traffic or apply temporary firewall rules

---

## 🔧 4. Eradication

- Remove exfiltration tools or malware from endpoints
- Disable or uninstall malicious applications or browser extensions
- Reset credentials and tokens used in unauthorized transfers
- Patch vulnerabilities (if exploited to gain access)
- Remove or archive logs from unauthorized applications/scripts

---

## 🔁 5. Recovery

- Re-enable accounts or access only after validating integrity
- Reconfigure cloud or on-prem access control policies
- Resume business operations with additional monitoring
- Restore user trust (if impacted)
- Ensure logging and DLP protections are active and effective

---

## 📝 6. Lessons Learned

- Determine root cause and impact (What data? Who? How?)
- Update DLP policies or SIEM detection rules
- Conduct user awareness training (especially around file sharing)
- Improve visibility into sensitive file access and movement
- Update playbooks and conduct internal briefing

---

## 📂 Metadata

| Field         | Value                                        |
|---------------|-----------------------------------------------|
| Incident Type | Data Exfiltration                             |
| Severity      | High (especially if sensitive data involved)  |
| TLP Label     | TLP:CLEAR                                     |
| Last Updated  | 2025-05-17                                    |
| Author        | Armand Williams                               |

---

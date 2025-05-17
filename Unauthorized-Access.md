# Unauthorized Access Incident Response Playbook

## 1. Detection

- SIEM alert triggered for login anomalies 
- Multiple failed login attempts followed by success 
- Account usage outside of normal business hours
- Login from unexpected IP addresses or devices
- MFA bypass or token reuse detected
- User reports suspicious activity (e.g., password change, unexpected emails)

---

## 2. Investigation

- Identify affected accounts
- Correlate timestamps of suspicious logins with:
  - Known phishing attempts
  - Other alerts or endpoint activity
- Review logs for privilege escalation or lateral movement
- Search for signs of data access or export
- Determine how the credentials were compromised 
  
---

## 3. Containment

- Disable or lock the compromised account(s)
- Invalidate sessions or reset tokens
- Force password reset with MFA re-enrollment
- Remove unauthorized access or privileges
- If applicable, isolate impacted systems from the network

---

## 4. Eradication

- Revoke any persistence mechanisms or backdoors created
- Clear unauthorized admin roles or access changes
- Clean up inbox rules (in case of email account compromise)
- Confirm malware is not involved (if compromise originated from endpoint)

---

## 5. Recovery

- Re-enable user account with new secure credentials and MFA
- Notify user and provide guidance on password hygiene
- Monitor account and related systems for post-compromise activity
- Resume services affected by account-based access control

---

## 6. Lessons Learned

- Document timeline and root cause 
- Update detection rules 
- Improve password policies or MFA enforcement
- Conduct awareness training if human error was involved
- Identify gaps in identity or access controls and update playbooks

---

## 📂 Metadata

| Field         | Value                                          |
|---------------|-------------------------------------------------|
| Incident Type | Unauthorized Access / Account Compromise        |
| Severity      | Medium / High (depending on access level)       |
| TLP Label     | TLP:CLEAR                                       |
| Last Updated  | 2025-05-17                                      |
| Author        | Armand Williams                                 |

---

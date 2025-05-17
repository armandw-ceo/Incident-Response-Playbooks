# Phishing Email Incident Response Playbook

## 1. Detection
- User reported suspicious email
- Alert triggered by email filter

## 2. Investigation
- Review email headers
- Review email body
- Sandbox URLs and attachments
- Review logs for user clicks/interactionswho

## 3. Containment
- Block sender/domain at the email gateway
- Block malicious links
- Quarantine emails
- Notify impacted users if any

## 4. Eradication
- Remove phishing email from all inboxes
- Patch any exploited systems if needed

## 5. Recovery
- Monitor user systems for abnormal behavior
- Reinforce email security policies
- Update playbook

## 6. Lessons Learned
- Update detection rules
- Phishing awareness training
- Document IOCs and update threat internal feeds

## Metadata
| Field        | Value                          |
|--------------|--------------------------------|
| Incident Type| Phishing Email                 |
| Severity     | Low / Medium (depending on user interaction)|
| TLP Label    | TLP:CLEAR                      |
| Last Updated | 2025-05-16                     |
| Author       | Armand Williams                |

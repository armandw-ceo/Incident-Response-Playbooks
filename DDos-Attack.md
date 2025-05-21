# DDoS Attack Incident Response Playbook

## 1. Detection

### ✅ Detection Checklist
- Abnormal spikes in inbound traffic
- Network performance degradation or service outages reported
- Alerts from IDS/IPS 
- Network Logs show traffic floods from multiple IPs or unusual geographic sources
- Application logs show repeated, abnormal requests (e.g., HTTP floods)

---

## 2. Investigation

- Identify the type of DDoS attack:
  - Volumetric (bandwidth exhaustion)
  - Protocol (e.g., SYN flood, ping of death)
  - Application-layer (e.g., HTTP GET/POST floods)
- Confirm target: which service, IP, or application is under attack?
- Analyze logs to determine:
  - Source IPs and geolocation
  - Patterns in traffic (same user agent, referrer, URI, etc.)
  - Duration and frequency of traffic spikes

---

## 3. Containment

- Activate DDoS mitigation services (e.g., AWS Shield, Cloudflare, Akamai)
- Geo-block or rate-limit suspicious IP ranges or traffic types
- Apply rate limiting or WAF (Web Application Firewall) rules
- Work with ISP or cloud provider for traffic redirection/blackholing
- Temporarily disable exposed APIs or endpoints if needed

---

## 4. Eradication

- Remove temporary firewall or WAF rules after confirming stability
- Re-enable affected systems/services cautiously
- If part of botnet traffic, submit IOCs to threat feeds or law enforcement
- Review and patch any exposed services that could be abused

---

## 5. Recovery

- Monitor traffic closely for recurrence
- Gradually restore services if they were taken offline
- Perform system health checks on impacted infrastructure
- Inform stakeholders of restored service availability

---

## 6. Lessons Learned

### Post-Incident Activities:
- Document attack type, scale, duration, and response timeline
- Update detection rules or thresholds in monitoring tools
- Evaluate performance of existing DDoS protections
- Engage with cloud/CDN provider about persistent protection
- Perform a tabletop exercise simulating a future DDoS attack

---

## Metadata

| Field         | Value                                      |
|---------------|---------------------------------------------|
| Incident Type | DDoS Attack                                 |
| Severity      | High (if service disruption occurred)       |
| TLP Label     | TLP:CLEAR                                   |
| Last Updated  | 2025-05-18                                  |
| Author        | Armand Williams                             |

---

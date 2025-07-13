# SIEM Fundamentals
Security Information and Event Management (SIEM), Its a platform that collects, normalizes, and analyzes logs to detect threats and support incident response.

### SIEM Use Cases
- Real-time alerting and monitoring
- Threat detection and correlation
- Compliance reporting (PCI, HIPAA, etc.)
- Forensic investigations

### Correlation Rules
- Logic to detect complex attack patterns using multiple log events (e.g., brute force + privilege escalation).
- Example: “5 failed logins + 1 success within 2 minutes” = potential credential stuffing.
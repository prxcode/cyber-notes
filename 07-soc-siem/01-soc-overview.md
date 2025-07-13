# Security Operations Center
### SOC Roles
- SOC Analyst (Tier 1-3) – Monitors alerts, investigates incidents, and escalates.
- SOC Manager – Oversees operations, team performance, policy enforcement.
- Threat Hunter – Proactively searches for hidden threats (often Tier 3+).
- Incident Responder – Handles and contains active threats/incidents.
- Forensic Analyst – Examines systems post-incident for legal/reporting purposes.

### SOC Tiers
- Tier 1 – Alert Analyst: Triages alerts, does basic investigation.
- Tier 2 – Incident Responder: Deep investigation, containment, and remediation.
- Tier 3 – Threat Hunter/SME: Proactive hunting, malware reverse engineering.
- Tier 4 – Support/Engineering (optional): Maintains tools, automates playbooks.
Incident Response (IR)

### Log Management
- Common Log Sources
    - Network Devices: Firewalls, IDS/IPS, routers, switches
    - Endpoints: Workstations, servers
    - Applications: Web servers, databases, cloud services
    - Security Tools: Antivirus, EDR, IAM systems

- Syslog Basics
    - Standard protocol for sending logs across devices
- Ports:
    - UDP 514 (default)
    - TCP 514 (reliable transport)
- Log levels (0-7): Emergency to Debug

### Windows Event Logs
- System Logs: OS-level messages (driver load failure, shutdown)
- Application Logs: App-specific messages (SQL errors)
- Security Logs: Login events, privilege use
- Key Event IDs:
    - 4624: Successful logon
    - 4625: Failed logon
    - 4670: Permissions on an object changed
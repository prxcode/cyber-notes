# OWASP Top 10 (2021)
### 1: Injection
- Common types: SQL, NoSQL, Command Injection.
- Happens when untrusted input is executed as code.
- Prevention: Prepared statements, input validation.

### 2: Broken Authentication
- Flaws in login systems (e.g., predictable passwords, session IDs).
- Exploits: Credential stuffing, brute-force attacks.
- Fixes: MFA, strong password policies, secure session management.

### 3: Sensitive Data Exposure
- Leaking sensitive info (e.g., PII, passwords).
- Encryption issues, poor storage practices.
- Use HTTPS, encrypt data at rest and in transit.

### 4: XML External Entities (XXE)
- Attackers exploit XML parsers to access internal files or systems.
- Prevention: Disable external entity resolution in XML parsers.

### 5: Broken Access Control
- Users access unauthorized resources.
- Examples: IDOR (Insecure Direct Object Reference).
- Fixes: Enforce access control at server level, proper role checks.

### 6: Security Misconfiguration
- Default credentials, unnecessary services, verbose errors.
- Secure configurations, regular audits, and hardening are crucial.

### 7: Cross-Site Scripting (XSS)
- Injection of malicious scripts into web pages.
- Types: Stored, Reflected, DOM-based.
- Prevent by escaping output, using CSP, input validation.

### 8: Insecure Deserialization
- Allows attackers to execute arbitrary code via crafted input.
- Prevention: Avoid deserialization of untrusted data, use safe formats.

### 9: Using Components with Known Vulnerabilities
- Libraries, frameworks with known CVEs.
- Regular dependency checks, update management (e.g., npm audit, pip-audit).

### 10: Insufficient Logging and Monitoring
- Missed signs of attack due to poor logging.
- Enable centralized logging, alerts, and audit trails.

---

### OWASP ZAP
- Open-source alternative to Burp.
- Active/passive scanning.
- Ideal for automated vulnerability discovery.
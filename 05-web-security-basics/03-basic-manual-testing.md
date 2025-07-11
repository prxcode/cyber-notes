# Basic Manual Web App Testing
Manual testing helps uncover vulnerabilities that automated tools might miss.

### Test Planning

1. Understand the application:
   - What does it do?
   - Who are the users?
2. Map out features (Login, Uploads, Search, etc.).
3. Look at exposed endpoints using Burp Suite/ZAP.

---

### Authentication Testing

- Test for:
  - Weak/default passwords
  - Missing account lockout
  - Session fixation: Does session ID change after login?
  - Brute-force vulnerabilities (no rate limiting)
- Try:
  - `admin:admin`, `test:test`, `password:123456`

---

### Session Management

- Check:
  - Session expiration on logout
  - Session timeout after inactivity
  - Secure/HttpOnly cookie flags
- Tamper session tokens (Burp Suite)

---

### Authorization Testing

- **Horizontal Access** (Same level):
  - Can user A access user B's resources?
- **Vertical Access** (Privilege escalation):
  - Can a low-priv user access admin features?
- Manual Test:
  - Change user ID in URLs: `/user/123` → `/user/124`
  - Remove `isAdmin=false` → `true` in requests

---

### Input Validation & Injection Testing

- **SQL Injection**:
  - Payloads: `' OR 1=1--`, `UNION SELECT null, null`
  - Use login forms, search bars, or URL params.
- **XSS (Cross-Site Scripting)**:
  - Payload: `<script>alert(1)</script>`
  - Try reflected, stored, DOM-based XSS.
- **Command Injection**:
  - Payload: `;ls`, `&& whoami`
- Tools:
  - Burp Suite (Repeater, Intruder)
  - Manual input fuzzing

---

### File Upload Testing

- Try uploading:
  - Malicious scripts (`.php`, `.jsp`)
  - Files with changed extensions (`.php.jpg`)
- Bypass file type checks:
  - Tamper content-type in requests
  - Double extensions: `file.jpg.php`

---

### Security Headers

- Check using:
  - `curl -I https://example.com`
  - Burp/ZAP
- Headers to look for:
  - `Content-Security-Policy`
  - `Strict-Transport-Security`
  - `X-Content-Type-Options`
  - `X-Frame-Options`

---

### Directory & Parameter Fuzzing

- Tools: `ffuf`, `gobuster`, `dirsearch`
- Discover hidden endpoints or directories:
  - Admin panels, backups, APIs

```bash
ffuf -u https://example.com/FUZZ -w /path/to/wordlist.txt
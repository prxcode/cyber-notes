# Authentication Flaws – Web Pentesting Notes

## 1. What Are Authentication Flaws?

- Weaknesses in how a web app **verifies user identity**
- Can lead to:
  - Account takeover
  - Unauthorized access
  - Privilege escalation

---

## 2. Common Authentication Flaws

### 2.1 Broken or Missing Authentication

- No authentication mechanism implemented
- Sensitive pages accessible without login
- Example:
  - /admin/dashboard accessible directly without credentials

---

### 2.2 Weak Credential Policies

- No password strength requirements
- Allows easily guessable or reused passwords
- No enforcement of MFA

---

### 2.3 Brute-force & Credential Stuffing

- No rate-limiting or account lockout
- Attacker uses:
  - Dictionary attack
  - Leaked credential sets

- Tools:
  - Hydra
  - Burp Intruder
  - Patator

---

### 2.4 Insecure Password Storage

- Plaintext passwords in DB or logs
- Weak hashing (e.g., MD5, SHA1)
- Best practice: bcrypt, scrypt, Argon2 with proper salting

---

### 2.5 Bypassing Authentication

- Logic flaws (e.g., login bypass via `true` condition)
- Unvalidated redirects or manipulated parameters
- Example:
  - Changing `isAdmin=false` to `isAdmin=true`

---

### 2.6 Session Fixation

- Session ID set before authentication and not refreshed
- Attacker can set a known session ID and hijack it post-login

---

### 2.7 Predictable Login / Reset URLs

- Token in password reset URL is predictable
- Example:
  - /reset-password?token=123456

---

### 2.8 Insecure Multi-Factor Authentication (MFA)

- MFA codes predictable, brute-forceable, or exposed via insecure channels (e.g., email, SMS)
- Logic flaws: e.g., bypass MFA by skipping a step in the flow

---

### 2.9 Insecure Session Management

- No proper session expiration
- Session tokens stored in:
  - Local storage (XSS-prone)
  - URL (leak via referrer headers)

---

### 2.10 Username Enumeration

- Different error messages for valid vs. invalid usernames
- Time-based differences
- Example:
  - "Invalid username" vs "Incorrect password"

---

## 3. Testing Techniques

- Check for login/logout flow bugs
- Brute-force login page using Hydra, Burp Intruder
- Tamper POST body and headers for logic flaws
- Monitor cookies for:
  - Session ID reuse
  - JWT tampering
- Intercept password reset flow and test token manipulation

---

## 4. Tools for Testing Authentication

- Burp Suite
- Hydra / THC-Hydra
- wfuzz / ffuf
- owasp-zap
- jwt-tool (for token analysis)

---

## 5. Prevention & Best Practices (Dev Perspective)

- Use secure, modern authentication libraries
- Enforce strong password policy and MFA
- Use secure session management:
  - HttpOnly, Secure cookies
  - Regenerate tokens after login
- Implement brute-force protection:
  - Rate limiting
  - CAPTCHA
- Proper error handling to avoid user enumeration

---

## 6. Cheat Sheet – Test Payloads & Checks

| Test | What to Try |
|------|-------------|
| Login Bypass | `' OR 1=1--`, empty password, tamper roles |
| Brute Force | Common creds, slow delays |
| Reset Token | Manipulate reset token value |
| Session Fixation | Set your own `JSESSIONID` or cookie |
| Username Enum | Observe error messages or timing |
| JWT Auth | Modify JWT payload or use weak secrets |

---

## 7. OWASP Top 10 Reference

- A07:2021 – Identification and Authentication Failures
- Related to:
  - Credential stuffing
  - Password mismanagement
  - Session hijacking


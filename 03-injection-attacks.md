# Injection Attacks – Web Pentesting Notes

## 1. What is an Injection Attack?

- Injection occurs when **untrusted input** is sent to an interpreter (e.g., SQL, OS shell, LDAP).
- Allows attackers to **alter the intended logic** or execute **malicious commands**.
- Common goal: **Data exfiltration**, **code execution**, **privilege escalation**.

---

## 2. Common Types of Injection Attacks

### 2.1 SQL Injection (SQLi)

- Targets: SQL queries in backend DBMS (MySQL, MSSQL, PostgreSQL)
- Payload Examples:
  - `' OR 1=1--`
  - `'; DROP TABLE users--`
- Techniques:
  - Error-based
  - Union-based
  - Boolean-based blind
  - Time-based blind
- Tools: `sqlmap`, `sqlitebrowser`, `burp`, `NoSQLMap`

---

### 2.2 NoSQL Injection

- Targets: MongoDB, CouchDB, Firebase
- Payloads:
  - `{"username": {"$ne": null}, "password": {"$ne": null}}`
- Common with JSON-based APIs

---

### 2.3 OS Command Injection

- Executes system-level commands via vulnerable input
- Payload Examples:
  - `; ls -la`
  - `&& whoami`
- Detection:
  - Look for execution delay (e.g., `sleep 5`)
- Tools: `commix`, `burp`, `ffuf`

---

### 2.4 LDAP Injection

- Targets LDAP queries (used for auth/search)
- Payload:
  - `*)(uid=*))(|(uid=*`
- Goal: Bypass login or escalate privileges

---

### 2.5 XML Injection

- Manipulates XML structure or data
- Payload Example:
  - `<user><name>admin</name></user>` → inject custom XML
- May lead to XXE or data tampering

---

### 2.6 XPath Injection

- Targets XPath expressions in XML data queries
- Payload:
  - `' or '1' = '1`
- Bypasses logic or extracts sensitive info

---

### 2.7 XXE (XML External Entity)

- Exploits XML parsers with external entity processing
- Payload:
  ```xml
  <!DOCTYPE foo [
    <!ENTITY xxe SYSTEM "file:///etc/passwd">
  ]>
  <data>&xxe;</data>

### 2.8 SSTI (Server-Side Template Injection)

* Targets templating engines like Jinja2, Twig, Smarty
* Payloads:

  * `{{7*7}}` → Output: 49
  * `{{config.items()}}`
* May lead to RCE depending on context

---

### 2.9 CRLF Injection

* Inserts `\r\n` into headers to manipulate HTTP responses
* Payload:

  * `%0d%0aSet-Cookie: admin=true`
* Can lead to:

  * Web cache poisoning
  * HTTP response splitting

---

### 2.10 Expression Language (EL) Injection

* Affects Java apps using JSP, Spring, or Struts
* Payload:

  * `${7*7}` or `${''.getClass().forName('java.lang.Runtime').getRuntime().exec('id')}`
* Often leads to RCE

---

## 3. Detection & Testing Tips

* Use **single quote `'`** or special characters to test for errors
* Monitor **response delays**, **status codes**, and **reflected inputs**
* Use **burp repeater** to test payloads manually
* Observe **error messages** or debug info

---

## 4. Prevention & Mitigation (Dev Perspective)

* Use parameterized queries (Prepared Statements)
* Whitelist input validation
* Disable unnecessary interpreters (e.g., XML entity processing)
* Use proper escaping, encoding
* Web Application Firewalls (WAF) as additional layer

---

## 5. Tools for Injection Testing

* sqlmap
* NoSQLMap
* commix
* burp suite
* wfuzz
* ffuf
* nuclei templates
* XSStrike (for reflected payloads)

---

## 6. Cheat Sheet – Payload Starters

| Injection Type | Sample Payload                              |           |
| -------------- | ------------------------------------------- | --------- |
| SQLi           | `' OR 1=1--`                                |           |
| NoSQL          | `{"username": {"$ne": null}}`               |           |
| OS Command     | `; whoami`                                  |           |
| LDAP           | \`*)(uid=*))(                               | (uid=\*\` |
| XXE            | `<!ENTITY xxe SYSTEM "file:///etc/passwd">` |           |
| SSTI           | `{{7*7}}`                                   |           |
| CRLF           | `%0d%0aSet-Cookie: admin=true`              |           |
| EL Injection   | `${7*7}`                                    |           |

---

## 7. OWASP Top 10 Reference

* A03:2021 - Injection
* A04:2021 - Insecure Design (includes template flaws)
* A05:2021 - Security Misconfiguration (relates to XXE, etc.)

```

Let me know if you'd like this converted into a downloadable `.md` or PDF file.
```

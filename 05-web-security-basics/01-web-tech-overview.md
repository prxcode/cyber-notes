# Web Architecture
### Client-Server Model
- **Client**: The user-facing interface (browser, mobile app).
- **Server**: Hosts the application/backend logic.
- Communication occurs over HTTP/HTTPS.
- Web applications typically follow a request-response cycle.

### HTTP/HTTPS Basics
- **HTTP** (HyperText Transfer Protocol): Stateless, plain-text protocol.
- **HTTPS**: Secure version using SSL/TLS encryption.
- Key Methods:
    - **GET**: Retrieve data
    - **POST**: Send data
    - **PUT**: Update data
    - **DELETE**: Delete data

### Cookies & Sessions
- **Cookies**: Stored on the client side. Used for state management.
- **Sessions**: Stored on the server. Tied to session ID (often in a cookie).
- Risks: Session hijacking, fixation, etc.

### Common Web Security Concepts
- Same-Origin Policy
    - Prevents a webpage from making requests to a different domain.
    - Core browser security feature.

- CORS (Cross-Origin Resource Sharing)

    - Controlled relaxation of same-origin policy.
    - Must be configured securely to prevent data leaks.

- CSRF (Cross-Site Request Forgery)
    - Tricks users into performing unintended actions.
    - Fix: CSRF tokens, SameSite cookie attribute.

- Input Validation & Sanitization
    - Validation: Ensure input meets expected format.
    - Sanitization: Strip or encode dangerous characters.
    - Prevents injection attacks (XSS, SQLi).

- HTTP vs HTTPS
    - HTTP: Insecure, data sent in plaintext.
    - HTTPS: Encrypted using TLS, prevents MITM attacks.

### Tools Introduction
- Burp Suite Basics
    - Intercept and modify HTTP/S requests.
    - Key Tools: Repeater, Intruder, Scanner.
    - Used for manual testing and automation.

- OWASP ZAP
    - Open-source web vulnerability scanner.
    - Features: Spider, Active Scan, Fuzzer, Passive Scan.
    - Good for learning and beginner-friendly.
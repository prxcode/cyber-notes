# Web Architecture
### Client-Server Model
- **Client**: The user-facing interface (browser, mobile app).
- **Server**: Hosts the application/backend logic.
- Communication occurs over HTTP/HTTPS.
- Web applications typically follow a request-response cycle.

### HTTP/HTTPS Basics
- **HTTP** (HyperText Transfer Protocol): Stateless, plain-text protocol.
- **HTTPS**: Secure version using SSL/TLS encryption.

### HTTP Request
A packet asking to load a website includes GET/POST headers and body. Example of HTTP Request.
- `<request line>` -> GET /doc/test html http/1.1
- `<request header>` -> host/accept/user agent/content length
- `<blank line to seprate header and body>`
- `<request message body>`

#### Types of Request Method
- 1. **GET**: Data transfer through URL easily visible and not secure.
- 2. **POST**: Sends user information & files in body to secure using html forms.
- 3. **PUT**: Replaces all current representations of the target resources with uploaded content.
- 4. **DELETE**: Remove all current representatios of the target resources given by a URL.
- 5. **OPTIONS**: Describe the communication options for the target resource.
- 6. **TRACE**: Performs a message loop back test along the path to the target resource.
- 7. **CONNECT**: Establishes a tunnel to the server identified by given URL.

### Domain Name and DNS
- **Domain**: Name of IP like **google.com**, **facebook.com** which is easy to remember.
- **DNS(Domain Name System)**: Aka Address book of internet, translate domain to IP, all records are stored zone file to redirect to that IP based on domain name translating zone file.
- **Zonefile**: A text file of DNS records of domain, it does IP mapping to find what domain for what IP it is always connected to a name server.

### Record in DNS and there use
- A: IP of domain name
- CNAME: Forwards domain and subdomain to another domain
- MX: Directs mail to email server
- NS: Name server of DNS entry
- SOA: Admin info about the domain
- SRV: Specify port for specific service
- PTR: Provides domain name in reverse lookup

  
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

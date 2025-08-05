# What is Web Application Architecture
It’s the structure of a web application, how its components interact:
- Frontend (Client-side)
- Backend (Server-side)
- Databases
- APIs
- Web Servers & Infrastructure

### Common Web App Architecture Types
- Monolithic: All components tightly coupled, Single point of failure
- 3-Tier (Presentation → Logic → DB): Standard Model, Attack surface at each layer
- Microservices: Independent services via APIs, More endpoints, more attack surface
- Serverless: 	Functions as a Service (e.g., AWS Lambda), Event-based, limited visibility


### Components to Focus On in Pentesting
- Client-Side (Frontend)
    - HTML, CSS, JavaScript
    - Attack Vectors: XSS, CSRF, DOM-based attacks

- Web Server
    - Handles HTTP requests
    - Examples: Apache, Nginx
    - Attack Vectors: Directory traversal, Info disclosure, Misconfigurations

- Application Server / Backend
    - Business logic, user management
    - Languages: PHP, Node.js, Python, Java
    - Attack Vectors: Authentication bypass, Logic flaws

- Database
    - Stores data (MySQL, MongoDB, PostgreSQL)
    - Attack Vectors: SQLi, NoSQLi, Privilege Escalation

- APIs
    - REST, GraphQL, SOAP
    - Attack Vectors: Insecure endpoints, Broken auth, IDOR, Mass Assignment
  

### Common Architectures & Their Attack Surfaces
- Single Page Application (SPA): Heavy JS, prone to XSS, insecure APIs
- Traditional Multi-page App (MPA): More server-side logic, CSRF possible
- PWAs (Progressive Web Apps):	Local storage, service workers – attackable offline

### Protocols & Communication
- HTTP/HTTPS → Sniffing, MiTM, weak TLS configs
- WebSockets → Real-time data; test for auth, data leakage
- JSON/XML → Injection, parsing bugs

### Authentication & Session Management
- Attack vectors:
    - Weak password policies
    - Session fixation
    - Token reuse
    - Insecure JWT storage

###  DevOps & Deployment Layers
- CI/CD pipelines (Jenkins, GitHub Actions)
- Containers (Docker), Orchestration (K8s)
- Infrastructure as Code (IaC)
- Common issues: Secrets in repos, Misconfigured containers, Exposed admin panels

### Tools by Architecture Layer
- Frontend:	Burp Suite, OWASP ZAP, Browser Dev Tools
- Backend: Burp Repeater, Postman, ffuf, curl
- DB: sqlmap, NoSQLMap
- APIs:	Postman, Burp Suite, SoapUI
- Infra: Nmap, Nikto, dirsearch, Shodan 

###  Pentesting Tips by Architecture
- Understand the flow: login → action → data → response
- Map all endpoints using crawling or passive discovery
- Test APIs even if the frontend doesn’t expose them fully
- Replay sessions and test for insecure session handling
- Check CORS, CSP, cookies, headers for misconfig
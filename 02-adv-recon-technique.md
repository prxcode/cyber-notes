# Advanced Reconnaissance Techniques in Web Pentesting

## 1. Subdomain Enumeration (Deep)

- Tools:
  - subfinder
  - amass
  - assetfinder
  - findomain
  - dnsx
  - massdns
  - crt.sh, certspotter (for Certificate Transparency)

- Techniques:
  - Passive: Use public sources, no interaction
  - Active: Brute-force and resolve DNS
  - Recursive: Enumerate subdomains of discovered subdomains
  - Permutation: Generate variations of known subdomains

---

## 2. Port Scanning & Fingerprinting

- Tools:
  - nmap
  - naabu
  - masscan

- Techniques:
  - nmap -sV -Pn -p- to discover all open ports and services
  - Use httpx to detect running web services
  - Fingerprint technologies with whatweb, nuclei, httprobe

---

## 3. URL & Endpoint Discovery

- Tools:
  - gau
  - waybackurls
  - hakrawler
  - katana
  - paramspider

- Techniques:
  - Extract historical URLs
  - Discover hidden parameters
  - Analyze sitemap.xml and robots.txt

---

## 4. JavaScript Recon

- Tools:
  - JSParser
  - LinkFinder
  - SecretFinder
  - subjs

- Goals:
  - Extract API endpoints, secrets, keys, and tokens
  - Identify hardcoded credentials or endpoints
  - Discover undocumented APIs

---

## 5. Directory & File Bruteforcing

- Tools:
  - ffuf
  - dirsearch
  - feroxbuster
  - gobuster

- Tips:
  - Use common and custom wordlists
  - Fuzz for file extensions (.php, .bak, .zip, etc.)
  - Look for backup or misconfigured files

---

## 6. Parameter Discovery (Fuzzing)

- Tools:
  - Arjun
  - ffuf
  - ParamSpider
  - Kiterunner

- Techniques:
  - Discover hidden GET/POST parameters
  - Fuzz parameter names and values
  - Attempt WAF bypass using encoding and tampering

---

## 7. Content Discovery via Crawling

- Tools:
  - hakrawler
  - gospider
  - crawlee
  - katana

- Tips:
  - Crawl authenticated sections using cookies or headers
  - Use headless mode for JS-heavy applications

---

## 8. Fingerprinting Web Technologies

- Tools:
  - whatweb
  - wappalyzer
  - webanalyze

- Goals:
  - Identify server software and CMS
  - Detect JS frameworks (React, Angular, Vue)
  - Map plugin or tech versions for known CVEs

---

## 9. OSINT & External Info Gathering

- Tools:
  - theHarvester
  - Maltego
  - SpiderFoot
  - intelx.io

- Sources:
  - Pastebin
  - GitHub
  - LinkedIn
  - Reddit
  - Google Dorking

---

## 10. Endpoint & API Recon

- Tools:
  - Postman
  - httpx
  - Kiterunner
  - graphqlmap

- Techniques:
  - Search for OpenAPI, Swagger, GraphQL endpoints
  - Use introspection in GraphQL to find queries/mutations
  - Test for multiple API versions (/v1/, /v2/, /beta/)

---

## 11. Favicon Hashing

- Tools:
  - httpx -favicon
  - Shodan
  - hashes.com

- Technique:
  - Calculate favicon hash and search known hashes
  - Identify software or shared infrastructure

---

## 12. TLS/SSL Recon

- Tools:
  - sslyze
  - testssl.sh
  - Shodan
  - Censys

- Goals:
  - Detect weak or outdated TLS versions and ciphers
  - Identify

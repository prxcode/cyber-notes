# Automation Tools for Web Application Pentesting

## 1. Reconnaissance Tools

### Subdomain Enumeration
- **subfinder** – Passive subdomain discovery
- **amass** – Passive and active enumeration
- **assetfinder** – Finds related subdomains via sources
- **findomain** – Fast, supports multiple APIs
- **crt.sh / certspotter** – Certificate transparency logs

### Port Scanning
- **nmap** – Full port + service version scan
- **naabu** – Fast port scanner (ProjectDiscovery)
- **masscan** – Internet-wide scanning

### Live Host Detection
- **httpx** – Probes URLs, gets titles, status, tech
- **httprobe** – Checks for live hosts on HTTP/HTTPS

---

## 2. Content Discovery

### Directory & File Bruteforcing
- **ffuf** – Fast web fuzzer for directories/params
- **dirsearch** – Directory and file brute-forcing
- **gobuster** – Directory, DNS, and vhost bruteforce
- **feroxbuster** – Recursive content discovery

### JS & Parameter Extraction
- **LinkFinder** – Finds endpoints in JS files
- **ParamSpider** – Crawls and finds URL params
- **Arjun** – GET/POST parameter discovery
- **JSParser** – Static JS parsing for URLs

### Crawlers
- **hakrawler** – Fast crawler for recon
- **katana** – Modern, configurable recon crawler
- **gospider** – Fast Go-based crawler

---

## 3. Vulnerability Scanners

- **nuclei** – Fast, template-based scanner for CVEs, misconfigs, and more
- **nikto** – Web server scanner for known vulnerabilities
- **wpscan** – WordPress vulnerability scanner
- **joomscan** – Joomla CMS scanner
- **whatweb** – Web tech fingerprinting

---

## 4. Injection & Exploit Tools

- **sqlmap** – Automates SQL injection detection & exploitation
- **NoSQLMap** – Exploits NoSQL injections (MongoDB)
- **XSStrike** – Advanced XSS detection
- **commix** – Command injection scanner and exploiter
- **jwt_tool** – JWT vulnerability analyzer & cracker

---

## 5. Authentication Testing Tools

- **hydra** – Password bruteforcer (SSH, FTP, HTTP, etc.)
- **patator** – Multi-purpose brute-force tool
- **Burp Suite** – Intruder for login fuzzing and brute-force

---

## 6. API & WebSocket Testing

- **Postman** – Manual API testing
- **Kiterunner** – API endpoint discovery using wordlists
- **GraphQLmap** – GraphQL security testing
- **wuzz / curl** – For quick endpoint interaction
- **Websocat** – WebSocket CLI client

---

## 7. OSINT Automation Tools

- **theHarvester** – Gathers emails, subdomains, and more
- **SpiderFoot** – Automated recon and OSINT framework
- **Amass Intel** – Passive OSINT on domains
- **GitHub-dorking tools** – e.g., `github-subdomains`, `truffleHog`

---

## 8. Automation Frameworks / Recon Workflows

- **reconftw** – End-to-end recon automation
- **LazyRecon** – Bash-based passive and active recon
- **bounty-machine** – Bug bounty automation suite
- **Osmedeus** – Full-stack automated offensive security framework

---

## 9. Wordlists (Essential for Automation)

- **SecLists** – Wordlists for fuzzing, brute-force, etc.
- **PayloadsAllTheThings** – Exploit payloads, tips, fuzzing inputs

---

## 10. Containerization / Setup

- **docker** – Run tools in containers
- **tmux** – Run multiple tools in parallel sessions
- **Makefiles / bash scripts** – For chaining toolsets

---

## Example Automation Flow

```bash
# Subdomain enumeration
subfinder -d example.com -o subs.txt

# Probing live hosts
httpx -l subs.txt -o live.txt

# Directory fuzzing
ffuf -w wordlist.txt -u https://example.com/FUZZ -o dirs.txt

# Nuclei scanning
nuclei -l live.txt -t vulnerabilities/ -o scan_results.txt

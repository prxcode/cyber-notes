#Basic Reconnaissance
Reconnaissance (Recon) is the **first phase** of penetration testing, focused on gathering information about the target.

### Types of Recon

#### 1. Passive Recon
- Collects data **without directly interacting** with the target.
- Avoids detection.

##### Tools & Techniques:
- **Google Dorking**:
  - Use advanced search operators.
  - Example: `site:example.com filetype:pdf` or `intitle:"index of" site:example.com`
- **Whois Lookup**:
  - Domain registration info.
  - Tool: `whois example.com`
- **DNS Enumeration**:
  - Tools: `dig`, `nslookup`, `dnsenum`, `dnsrecon`
  - Get A, MX, TXT, and NS records.
- **Social Media & Breach Data**:
  - Check LinkedIn, GitHub, Pastebin, HaveIBeenPwned.

#### 2. Active Recon
- Directly engages with the target to get deeper information.

##### Tools & Techniques:
- **Port Scanning**:
  - Tool: `nmap -sS -sV -Pn example.com`
  - Find open ports, services, versions.
- **Subdomain Enumeration**:
  - Tools: `Sublist3r`, `Amass`, `Assetfinder`, `crt.sh`
- **Tech Stack Detection**:
  - Tools: `Wappalyzer`, `WhatWeb`, `BuiltWith`
- **Directory Brute Forcing**:
  - Tool: `dirsearch`, `gobuster`, `feroxbuster`
  - Example: `gobuster dir -u https://example.com -w wordlist.txt`
- **SSL/TLS Analysis**:
  - Tool: `ssllabs.com`, `testssl.sh`
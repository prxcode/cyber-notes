# Indicators of Compromise (IoCs)
Artifacts observed on a network or in an operating system that indicate a potential intrusion.
### Common IoC Types:
- File hashes (MD5, SHA256) – Known malware files
- IP addresses/domains – Used in C2 (Command and Control)
- Filenames/processes – e.g., mimikatz.exe, svchost.exe in wrong path
- Registry changes – Persistence techniques
- Unusual network traffic – Data exfiltration or lateral movement
- Behavioral patterns – Time of access, frequency of log in failures

### Tools to Detect IoCs:
- SIEMs (e.g., Splunk with threat feeds)
- EDR tools (CrowdStrike, SentinelOne)
- Threat intel platforms (MISP, VirusTotal)
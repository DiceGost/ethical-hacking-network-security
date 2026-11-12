# Findings and Defensive Recommendations

## 1. Network reconnaissance
**Assigned contributor area:** Host discovery and initial reconnaissance using Nmap in a controlled virtual environment.

**Observation:** Discovery identified reachable machines within the assigned lab network. The host list enabled the team to plan further enumeration against intentionally vulnerable systems.

**Takeaway:** Asset inventories, segmentation, and restricted access to management services help limit exposed attack surfaces.

## 2. Legacy services and service enumeration
**Team exercise:** A separate team member conducted detailed service and OS fingerprinting of the Metasploitable lab server.

**Observation:** The report documents intentionally vulnerable or insecure services including FTP, Telnet, and HTTP. It also records a Metasploit demonstration against the known vsftpd 2.3.4 backdoor in the lab.

**Defenses:** Remove obsolete services; patch or replace vulnerable software; prefer encrypted protocols such as SSH and HTTPS; restrict access by least privilege and network segmentation.

## 3. ARP spoofing and network interception
**Team exercise:** Team members used an isolated demonstration setup to test local network traffic interception.

**Observation:** The report describes changes in observed ARP mappings and traffic visibility through a lab intermediary. Separate team members used different network configurations, so results should not be interpreted as a single identical environment.

**Defenses:** Use Dynamic ARP Inspection where supported, DHCP snooping, switch port controls, segmentation, endpoint protections and anomaly monitoring. Static ARP entries are practical only in narrow, managed situations.

## 4. Encrypted traffic analysis
**Team exercise:** Wireshark packet analysis.

**Observation:** Captured HTTPS sessions used TLS encryption. The report identified visible connection metadata but did not show recovered plaintext credentials from TLS-protected sessions.

**Defenses:** Enforce HTTPS/TLS, disable obsolete cleartext services, maintain certificates, and monitor for unexpected routing and ARP changes.

## 5. DNS spoofing risks
**Team exercise:** A separate member documented a DNS redirection demonstration within a testing environment.

**Defenses:** Use trusted resolvers, DNSSEC validation when applicable, secure endpoint DNS configuration, transport encryption, and network anomaly detection. DNSSEC validates signed DNS records but is not a complete solution to all MITM threats.

## Limitations
- Findings were documented by different group members across separate virtual machines and network layouts.
- The repository summarizes the academic report rather than publishing third-party personal information, packet captures, exploit payloads, or original unredacted submissions.
- The project does not demonstrate a real-world compromise or a complete production penetration test.

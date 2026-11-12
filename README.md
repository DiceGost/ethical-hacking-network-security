# Ethical Hacking: Network Security & MITM Analysis

**Academic group project | CSCI369 Ethical Hacking | University of Wollongong in Dubai**

## Overview
This project documents an authorized educational assessment of network security in virtual lab environments. The team investigated network reconnaissance, exposed services, man-in-the-middle (MITM) risks, ARP and DNS spoofing, traffic analysis, and defensive controls.

## My contribution
My assigned work focused on:
- **Network reconnaissance:** Used Nmap host discovery in a controlled virtual subnet to identify reachable systems.
- **Initial attack-surface analysis:** Documented discovered hosts to support subsequent team service enumeration and testing.
- **Mitigations and defenses:** Researched and documented ways to reduce the risks demonstrated in the team's lab exercises.

Other team members carried out the service enumeration, ARP/DNS spoofing, packet capture and Metasploit demonstrations described in the shared report. This repository does **not** present those exercises as my individual work.

## Team's lab toolkit
Kali Linux · VirtualBox · Ubuntu · Metasploitable 2 · Nmap · Wireshark · Metasploit · TCP/IP

## Team's documented findings
- Nmap discovery and service enumeration exposed hosts and legacy services on the intentionally vulnerable test server.
- The team's ARP-spoofing demonstration showed how local network traffic can be redirected within the lab.
- Wireshark analysis showed encrypted TLS traffic: the team observed connection metadata, **not plaintext HTTPS credentials**.
- The exercises highlighted the risks of insecure protocols, legacy services, and weak local-network protections.

See [findings and mitigations](docs/findings-and-mitigations.md) for a concise write-up.

## Scope and ethics
This is a **group educational security lab**, not an assessment of a live organization. Team members used separate virtual lab environments, so observed addresses and network layouts were not identical across all exercises. No production systems were authorized targets. Sensitive student details and raw lab artifacts are intentionally excluded from this public version.

## Project format
This repository contains documentation of a completed practical assignment, **not an original software application**. Its purpose is to showcase security analysis, lab methodology, technical communication, and mitigation research.

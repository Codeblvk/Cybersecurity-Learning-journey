# Nmap - Network Scanning Fundamentals

## Overview

This documentation summarizes my hands-on learning of Nmap, a widely used network discovery and security auditing tool. The objective was to understand how hosts and services can be identified, how ports are scanned, and how Nmap assists security professionals during reconnaissance and network assessments.

> **Note:** All exercises were performed in an authorized lab environment for educational purposes.

---

# Learning Objectives

- Understand the purpose of network scanning.
- Identify live hosts on a network.
- Discover open ports and running services.
- Perform service and operating system detection.
- Learn common Nmap scan types.
- Interpret scan results.

---

# Topics Covered

- Host Discovery
- Port Scanning
- TCP Connect Scan
- SYN Scan
- UDP Scan
- Service Version Detection
- Operating System Detection
- Aggressive Scan
- NSE (Nmap Scripting Engine)
- Output Formats

---

# Common Nmap Commands

## Host Discovery

```bash
nmap 192.168.1.10
```

Scans the target for open ports.

---

## Scan Multiple Hosts

```bash
nmap 192.168.1.0/24
```

Discovers hosts on a subnet.

---

## Scan Specific Ports

```bash
nmap -p 22,80,443 192.168.1.10
```

---

## TCP SYN Scan

```bash
nmap -sS 192.168.1.10
```

Performs a stealth SYN scan.

---

## TCP Connect Scan

```bash
nmap -sT 192.168.1.10
```

Uses the full TCP handshake.

---

## UDP Scan

```bash
nmap -sU 192.168.1.10
```

Scans UDP ports.

---

## Service Version Detection

```bash
nmap -sV 192.168.1.10
```

Attempts to identify application versions.

---

## Operating System Detection

```bash
nmap -O 192.168.1.10
```

Attempts to identify the operating system.

---

## Aggressive Scan

```bash
nmap -A 192.168.1.10
```

Enables:

- OS Detection
- Version Detection
- Default NSE Scripts
- Traceroute

---

## Save Results

```bash
nmap -oN scan.txt 192.168.1.10
```

Normal output.

```bash
nmap -oX scan.xml 192.168.1.10
```

XML output.

---

# Scan States

Nmap reports ports as:

| State | Meaning |
|--------|---------|
| Open | Service is accepting connections |
| Closed | No service listening |
| Filtered | Firewall prevented determination |
| Unfiltered | Reachable but state unknown |
| Open|Filtered | Cannot distinguish |
| Closed|Filtered | Cannot distinguish |

---

# Common Ports Observed

| Port | Service |
|------|----------|
| 21 | FTP |
| 22 | SSH |
| 23 | Telnet |
| 25 | SMTP |
| 53 | DNS |
| 80 | HTTP |
| 110 | POP3 |
| 139 | NetBIOS |
| 143 | IMAP |
| 443 | HTTPS |
| 445 | SMB |
| 3389 | RDP |

---

# Practical Workflow

Target Selection

↓

Host Discovery

↓

Port Scan

↓

Version Detection

↓

OS Detection

↓

Service Enumeration

↓

Report Findings

---

# Defensive Perspective

Nmap is widely used by defenders to:

- Audit network exposure.
- Verify firewall rules.
- Identify unnecessary services.
- Discover unauthorized hosts.
- Validate network segmentation.

Understanding Nmap also helps SOC analysts recognize reconnaissance activity performed by attackers.

---

# Skills Demonstrated

- Network Discovery
- TCP/IP
- Port Scanning
- Service Enumeration
- Operating System Fingerprinting
- Network Reconnaissance
- Security Assessment

---

# Key Learnings

- Network scanning is the first stage of many security assessments.
- Open ports represent available services, not vulnerabilities by themselves.
- Service version detection provides additional context during investigations.
- OS fingerprinting is probabilistic and may not always be accurate.
- Results should always be interpreted alongside other evidence.
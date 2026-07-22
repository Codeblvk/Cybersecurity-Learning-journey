# Tcpdump - Packet Capture Fundamentals

## Overview

This documentation summarizes my study of tcpdump, a command-line packet analyzer used to capture and inspect network traffic. Tcpdump is widely used in incident response, troubleshooting, and network analysis.

> **Note:** Packet captures were performed in an authorized lab environment.

---

# Learning Objectives

- Capture network packets.
- Apply capture filters.
- Inspect protocol traffic.
- Save captures for later analysis.
- Understand packet-level troubleshooting.

---

# Topics Covered

- Packet Capture
- Interface Selection
- Capture Filters
- Protocol Filters
- Host Filters
- Port Filters
- Reading PCAP Files
- Saving Captures

---

# Basic Syntax

```bash
tcpdump [options] [filter]
```

---

# List Network Interfaces

```bash
tcpdump -D
```

---

# Capture Packets

```bash
sudo tcpdump
```

---

# Capture on Specific Interface

```bash
sudo tcpdump -i eth0
```

---

# Capture Specific Number of Packets

```bash
sudo tcpdump -c 100
```

---

# Save Capture

```bash
sudo tcpdump -w capture.pcap
```

---

# Read Saved Capture

```bash
tcpdump -r capture.pcap
```

---

# Capture TCP Traffic

```bash
tcpdump tcp
```

---

# Capture UDP Traffic

```bash
tcpdump udp
```

---

# Capture ICMP

```bash
tcpdump icmp
```

---

# Capture HTTP

```bash
tcpdump port 80
```

---

# Capture HTTPS

```bash
tcpdump port 443
```

---

# Capture SSH

```bash
tcpdump port 22
```

---

# Capture DNS

```bash
tcpdump port 53
```

---

# Capture from a Host

```bash
tcpdump host 192.168.1.10
```

---

# Capture Source Traffic

```bash
tcpdump src host 192.168.1.10
```

---

# Capture Destination Traffic

```bash
tcpdump dst host 192.168.1.10
```

---

# Combine Filters

```bash
tcpdump tcp and port 80
```

---

# Practical Workflow

Select Interface

↓

Start Capture

↓

Apply Filters

↓

Observe Packets

↓

Save Capture

↓

Analyze in Wireshark

---

# Why Tcpdump Matters

Tcpdump allows analysts to:

- Troubleshoot network connectivity.
- Investigate suspicious traffic.
- Capture evidence during incidents.
- Validate firewall behavior.
- Analyze protocol communication.

It is commonly used on Linux servers where a graphical interface is unavailable.

---

# Skills Demonstrated

- Packet Capture
- Linux Networking
- TCP/IP
- Traffic Filtering
- Network Troubleshooting
- PCAP Analysis
- Command-Line Networking

---

# Key Learnings

- Capture filters reduce unnecessary traffic.
- Saving packet captures enables offline analysis.
- Tcpdump complements Wireshark by providing lightweight packet capture on servers.
- Effective filtering improves investigation efficiency.
- Understanding packet flow is essential for SOC investigations.
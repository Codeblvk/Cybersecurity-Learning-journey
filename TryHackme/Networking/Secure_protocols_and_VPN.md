# Secure Protocols and VPN

## Why Secure Protocols?

Many original Internet protocols were designed without encryption. Secure protocols were developed to provide:

- Confidentiality
- Integrity
- Authentication

---

## TLS (Transport Layer Security)

TLS is a cryptographic protocol used to secure communications over a network.

### Functions

- Encrypts data
- Verifies server identity
- Protects against eavesdropping

### Common Usage

- HTTPS
- SMTPS
- FTPS

### Key Learning

TLS is the foundation of many secure Internet services.

---

## HTTPS

HTTPS (HyperText Transfer Protocol Secure) is the secure version of HTTP.

### Port

443

### Features

- Uses TLS encryption
- Protects web traffic
- Verifies website identity using certificates

### Example

https://tryhackme.com

### Key Learning

HTTPS protects data exchanged between browsers and web servers.

---

## SMTPS

Secure Simple Mail Transfer Protocol.

### Ports

465 or 587 (with STARTTLS)

### Purpose

Securely sends email using encryption.

### Key Learning

SMTPS protects email transmission from interception.

---

## POP3S

Secure Post Office Protocol Version 3.

### Port

995

### Purpose

Securely retrieves emails from a mail server.

### Key Learning

POP3S encrypts email retrieval traffic.

---

## SSH (Secure Shell)

SSH provides secure remote access to systems.

### Port

22

### Common Commands

```bash
ssh username@ip_address
```

Example:

```bash
ssh kali@192.168.1.10
```

### Features

- Encryption
- Authentication
- Remote administration

### Key Learning

SSH is the standard method for secure remote administration.

---

## SFTP

SSH File Transfer Protocol.

### Port

22

### Purpose

Secure file transfer using SSH.

### Example

```bash
sftp username@ip_address
```

### Key Learning

SFTP securely transfers files through an SSH connection.

---

## FTPS

File Transfer Protocol Secure.

### Ports

21 + TLS encryption

### Features

- FTP with TLS security
- Encrypted file transfers

### Key Learning

FTPS improves security over traditional FTP.

---

## VPN (Virtual Private Network)

A VPN creates an encrypted tunnel between a device and a remote network.

### Benefits

- Encrypts traffic
- Protects privacy
- Enables secure remote access

### Common Uses

- Remote work
- Secure public Wi-Fi usage
- Accessing internal company networks

### Key Learning

VPNs protect network traffic while it travels across untrusted networks.

---

# Summary Table

| Protocol | Port | Purpose |
|-----------|------|----------|
| HTTPS | 443 | Secure Web Browsing |
| SMTPS | 465/587 | Secure Email Sending |
| POP3S | 995 | Secure Email Retrieval |
| SSH | 22 | Secure Remote Access |
| SFTP | 22 | Secure File Transfer |
| FTPS | 21 + TLS | Secure FTP |
| VPN | Varies | Secure Network Tunnel |
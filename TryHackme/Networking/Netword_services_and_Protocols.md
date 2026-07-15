# Network Services and Protocols

## DNS (Domain Name System)

DNS translates human-readable domain names into IP addresses.

### Example

google.com → 142.250.x.x

Without DNS, users would need to remember IP addresses instead of domain names.

### DNS Records

#### A Record
Maps a domain name to an IPv4 address.

Example:
google.com → 142.250.193.78

#### AAAA Record
Maps a domain name to an IPv6 address.

#### CNAME Record
Creates an alias for another domain.

Example:
www.example.com → example.com

#### MX Record
Specifies the mail server responsible for receiving emails.

### DNS Lookup Commands


nslookup google.com 

## HTTP (Hyper Text Transfer Protocol)

HyperText Transfer Protocol is used to transfer web pages between clients and servers.

### Default Port - 80

### Characteristics

Application Layer Protocol
Stateless
Uses TCP

Example:
GET / HTTP/1.1
Host: example.com

## HTTPS(HyperText Transfer Protocol Secure)

HyperText Transfer Protocol Secure is the encrypted version of HTTP.

### Default Port - 443

### Features

Encryption
Confidentiality
Integrity
Authenticity

### Technologies Used

SSL/TLS
TCP

Key Leaning:
HTTPS protects data during transmission.

## FTP (File Transfer Protocol)

File Transfer Protocol is used for transferring files between systems.

### Default Ports

21 (Control Connection)
20 (Data Connection)

### Commands

ftp <server-ip>

### Screenshot
![FTP](/TryHackme/Screenshot/ftp%20(1).png)
![FTP](/TryHackme/Screenshot/ftp%20(2).png)
![FTP](/TryHackme/Screenshot/ftp%20(5).png.png)

## SMTP (Simple Mail Transfer Protocol)

Simple Mail Transfer Protocol is used for sending emails.

### DEfualt Ports

25
5877
465

### Purpose

Client → Mail Server

Mail Server → Mail Server

Key Learning:
SMTP is responsible for sending emails.

## POP3 (Post Office Protocol Version 3)

Post Office Protocol Version 3 is used to retrieve emails from a mail server.

### Default Port

110
995(Secure Port)

## Characteristics

Downloads emails locally
Often removes emails from server

Key Learning:
POP3 is used for email retrieval.

## IMAP

Internet Message Access Protocol is used to access emails stored on a mail server.

### Default Port

143

993(Secure Port)

### Charateristics 

Synchronizes emails
Supports multiple devices
Keeps emails on server

Key Learning
IMAP allows email access from multiple devices.

## Summary Table

| Protocol | Port       | Purpose               |
| -------- | ---------- | --------------------- |
| HTTP     | 80         | Web Browsing          |
| HTTPS    | 443        | Secure Web Browsing   |
| FTP      | 21         | File Transfer         |
| SMTP     | 25/587/465 | Sending Email         |
| POP3     | 110/995    | Receiving Email       |
| IMAP     | 143/993    | Email Synchronization |
| DNS      | 53         | Name Resolution       |
| WHOIS    | 43         | Domain Information    |
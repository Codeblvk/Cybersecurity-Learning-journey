# Network Fundamentals

## OSI Model

The OSI (Open Systems Interconnection) Model is a 7-layer framework used to understand how data travels across a network.

### Layers

7. Application - User-facing services (HTTP, FTP, SMTP)
6. Presentation - Data formatting and encryption
5. Session - Manages communication sessions
4. Transport - Reliable communication (TCP, UDP)
3. Network - Logical addressing and routing (IP)
2. Data Link - MAC addressing and frame delivery
1. Physical - Transmission of bits over cables/wireless

### Key Learning

Each layer performs a specific function and communicates with the layer above and below it.

---

## TCP/IP Model

The TCP/IP model is the practical networking model used on the Internet.

### Layers

1. Application
2. Transport
3. Internet
4. Network Access

### OSI vs TCP/IP

OSI has 7 layers while TCP/IP has 4 layers.

### Key Learning

All Internet communication follows the TCP/IP model.

---

## TCP

Transmission Control Protocol (TCP) provides reliable communication.

### Features

- Connection-oriented
- Reliable delivery
- Error checking
- Packet ordering
- Three-way handshake

### Three-Way Handshake

1. SYN
2. SYN-ACK
3. ACK

### Common TCP Ports

- HTTP - 80
- HTTPS - 443
- SSH - 22
- FTP - 21

### Key Learning

TCP ensures data arrives correctly and in order.

---

## UDP

User Datagram Protocol (UDP) is a fast communication protocol.

### Features

- Connectionless
- Faster than TCP
- No packet ordering
- No delivery guarantee

### Common UDP Uses

- DNS
- Video Streaming
- Online Gaming

### Key Learning

UDP prioritizes speed over reliability.

---

## Encapsulation

Encapsulation is the process of adding protocol information as data moves down the network stack.

### Process

Application Data
↓
TCP Segment
↓
IP Packet
↓
Ethernet Frame

### Decapsulation

The receiving device removes headers layer by layer to retrieve the original data.

### Key Learning

Data is wrapped with headers at each layer before transmission.

---

## DHCP

Dynamic Host Configuration Protocol automatically assigns network settings to devices.

### DHCP Process

1. Discover
2. Offer
3. Request
4. Acknowledge

### Information Assigned

- IP Address
- Subnet Mask
- Default Gateway
- DNS Server

### Key Learning

DHCP eliminates manual IP configuration.

---

## ARP

Address Resolution Protocol maps IP addresses to MAC addresses within a local network.

### Example

Computer wants to reach:

IP: 192.168.1.1

ARP asks:

"Who has 192.168.1.1?"

Router responds with its MAC address.

### Key Learning

ARP is used for local network communication.

---

## ICMP

Internet Control Message Protocol is used for diagnostics and error reporting.

### Common Uses

- Ping
- Traceroute
- Error messages

### Example

ping google.com

Sends ICMP Echo Requests and receives Echo Replies.

### Key Learning

ICMP helps troubleshoot network connectivity.
# Routing and NAT

## Routing

Routing is the process of forwarding packets from one network to another.

### Router Function

A router examines the destination IP address and decides the best path for packet delivery.

### Key Learning

Routers connect different networks and forward packets.

---

## Routing Algorithms

Routing algorithms help routers determine the best path to a destination.

Factors considered:

- Hop Count
- Bandwidth
- Delay
- Reliability

### Key Learning

Routing algorithms enable efficient packet delivery.

---

## RIP

Routing Information Protocol is a distance-vector routing protocol.

### Features

- Uses Hop Count
- Maximum 15 hops
- Slow convergence

### Metric

Hop Count

### Key Learning

RIP is simple but not suitable for large networks.

---

## OSPF

Open Shortest Path First is a link-state routing protocol.

### Features

- Fast convergence
- Uses SPF Algorithm
- Supports large networks

### Metric

Cost

### Key Learning

OSPF is commonly used in enterprise networks.

---

## EIGRP

Enhanced Interior Gateway Routing Protocol is a Cisco routing protocol.

### Features

- Fast convergence
- Efficient route calculation
- Supports multiple metrics

### Metric

- Bandwidth
- Delay
- Reliability
- Load

### Key Learning

EIGRP is optimized for Cisco environments.

---

## BGP

Border Gateway Protocol is the routing protocol used on the Internet.

### Features

- Connects different Autonomous Systems
- Highly scalable
- Path-vector protocol

### Usage

ISP to ISP communication

### Key Learning

BGP powers Internet routing worldwide.

---

## NAT

Network Address Translation translates private IP addresses into public IP addresses.

### Purpose

Allows multiple devices to share one public IP address.

### Example

Private IP:
192.168.1.10

Translated Public IP:
49.x.x.x

### Benefits

- Conserves IPv4 addresses
- Improves security
- Enables Internet access

### Types

- Static NAT
- Dynamic NAT
- PAT (Port Address Translation)

### Key Learning

NAT allows private networks to communicate with the Internet.
# Project Objectives

The purpose of this project is to simulate a small enterprise network while applying core networking concepts.

The project objectives include:

- Build a basic enterprise network topology
- Configure routing between two LANs
- Implement DHCP services
- Deploy DNS services
- Host an internal web server
- Backup device configurations using TFTP
- Provide wireless connectivity
- Practice Cisco IOS configuration
- Improve network documentation skills

---

# Enterprise Network Overview

The simulated enterprise network consists of two separate Local Area Networks.

## LAN 1 - User Network

LAN 1 represents the employee network where end users connect to the organization's infrastructure.

This network contains:

- Router Gateway
- Layer 2 Switch
- DHCP Server
- Wireless Access Point
- Two Wireless Laptops
- One Desktop PC
- One DHCP Client

---

## LAN 2 - Server Network

LAN 2 represents the organization's server infrastructure.

This network contains:

- Router Gateway
- Layer 2 Switch
- DNS Server
- TFTP Server
- Web Server

Separating users from servers is a common enterprise design that improves organization, scalability, and security.

---

# Network Topology

*A detailed topology diagram is available inside the `screenshots/` folder.*

---

# IP Addressing Scheme

| Device | IP Address | Purpose |
|---------|------------|---------|
| Router G0/0 | 192.168.1.1 | Gateway (LAN 1) |
| Router G0/1 | 192.168.2.1 | Gateway (LAN 2) |
| Switch 1 | 192.168.1.2 | Management |
| Switch 2 | 192.168.2.2 | Management |
| PC 1 | 192.168.1.3 | Static Client |
| DHCP Server | 192.168.1.254 | Dynamic IP Assignment |
| DNS Server | 192.168.2.10 | Name Resolution |
| TFTP Server | 192.168.2.20 | Configuration Backup |
| Web Server | 192.168.2.30 | HTTP Service |
| Laptop 1 | DHCP | Wireless Client |
| Laptop 2 | DHCP | Wireless Client |
| Laptop 0 | DHCP | DHCP Testing |

---

# Network Devices

The project uses the following Cisco networking devices:

- Cisco Router
- Cisco Layer 2 Switches
- Wireless Access Point
- Desktop PCs
- Laptop Clients
- DHCP Server
- DNS Server
- TFTP Server
- Web Server

---

# Network Services

## DHCP (Dynamic Host Configuration Protocol)

DHCP automatically assigns IP addresses and network configuration to client devices, eliminating the need for manual IP configuration.

---

## DNS (Domain Name System)

DNS translates domain names into IP addresses, allowing users to access services using easy-to-remember names instead of numerical addresses.

---

## HTTP (Web Server)

The HTTP server hosts a simple internal website that can be accessed by clients within the enterprise network.

---

## TFTP (Trivial File Transfer Protocol)

TFTP is commonly used by network administrators to backup and restore Cisco device configurations.

In this project, both switches and the router will save their running configurations to the TFTP server.

---

## Wireless Access Point

The Access Point provides wireless connectivity for mobile devices within LAN 1 while allowing them to communicate with the wired network.

---

# Configuration Summary

The project includes configuration of:

- Basic Router Configuration
- Basic Switch Configuration
- Interface Configuration
- Static IPv4 Addressing
- DHCP Configuration
- DNS Configuration
- HTTP Configuration
- Wireless Configuration
- TFTP Backup
- Connectivity Testing

---

# Verification

The network will be verified by performing the following tests:

- Successful Ping between LAN 1 and LAN 2
- DHCP Address Assignment
- DNS Name Resolution
- HTTP Web Access
- Wireless Connectivity
- TFTP Configuration Backup

---

# Skills Demonstrated

This project demonstrates practical experience with:

- Cisco IOS CLI
- Enterprise Network Design
- IPv4 Addressing
- Router Configuration
- Switch Configuration
- DHCP
- DNS
- HTTP
- TFTP
- Wireless Networking
- Network Troubleshooting
- Configuration Backup
- Technical Documentation

---

# Repository Structure

```

CCNA-001-Common-Enterprise-Network
│
├── README.md
├── packet-tracer
│   └── common-enterprise-topology.pkt
│
├── configs
│   ├── R1.txt
│   ├── SW1.txt
│   ├── SW2.txt
│   └── GENERAL-GUIDE.md
│
└── screenshots
    ├── TOPOLOGY.png
    ├── DHCP-TEST.png
    ├── DNS-TEST.png
    ├── ROUTING-TABLE.png
    ├── ROUTER-VERIFICATION.png
    ├── SWITCHES-INTERFACES.png
    ├── PING-TEST.png
    ├── DHCP-CONFIGURATION.png
    ├── WEB-TEST.png
    └── TFTP-BACKUP.png



```

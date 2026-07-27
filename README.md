# Secure Virtual Home Network

## Project Overview

This project demonstrates the design and implementation of a secure virtual home network using Cisco Packet Tracer.

The objective of this project is to simulate a realistic home network environment while applying networking and cybersecurity concepts such as IP addressing, DHCP, wireless networking, VLAN segmentation, inter-VLAN routing, Access Control Lists (ACLs), SSH remote management, switch port security, and Cisco device hardening.

The project is developed in multiple phases, progressing from a functional home network to a security-focused network architecture.

---

# Objectives

- Design a functional and secure home network topology
- Configure routers, switches, and wireless devices
- Implement IPv4 addressing and DHCP services
- Configure VLAN-based network segmentation
- Implement Router-on-a-Stick for inter-VLAN routing
- Configure secure remote management using SSH
- Restrict network access using Access Control Lists (ACLs)
- Protect switch ports using Port Security
- Apply Cisco device hardening best practices
- Document network configurations, testing procedures, and implementation results

---

# Technologies Used

- Cisco Packet Tracer
- Cisco IOS Command Line Interface (CLI)
- IPv4 Networking
- DHCP
- VLAN Configuration
- IEEE 802.1Q Trunking
- Router-on-a-Stick
- Inter-VLAN Routing
- SSH Remote Management
- Access Control Lists (ACL)
- Switch Port Security
- Cisco Device Hardening
- Git & GitHub

---

# Network Devices Used

| Device | Purpose |
|---------|---------|
| Cisco ISR 4331 Router | Routing, DHCP, and Inter-VLAN Routing |
| Cisco Catalyst 2960 Switch | LAN Switching and VLAN Management |
| Cisco AP-PT | Wireless Access Point |
| Desktop-PC | Personal Wired Client |
| Work Laptop | Wireless Client |
| Home Server | Internal Services |
| Network Printer | Shared Network Printer |
| Mobile Phone | Guest WiFi Client |
| Tablet | Guest WiFi Client |

---

# Network Topology

![Network Topology](images/phase1-topology.png)

---

# Phase 1 – Functional Home Network ✅

Completed implementation:

- Designed the home network topology
- Configured Cisco ISR 4331 router
- Configured Catalyst 2960 switch
- Implemented DHCP services
- Assigned static IP addresses for infrastructure devices
- Configured wireless networking using AP-PT
- Connected wired and wireless clients
- Performed connectivity testing

---

# Phase 2 – Network Segmentation and Secure Management ✅

Completed implementation:

- Created VLAN-based network segmentation
- Configured VLAN 10 (Personal)
- Configured VLAN 30 (Guest WiFi)
- Configured VLAN 40 (Servers)
- Configured VLAN 99 (Management)
- Configured IEEE 802.1Q trunking
- Implemented Router-on-a-Stick
- Enabled Inter-VLAN Routing
- Configured SSH remote management
- Validated VLAN communication

---

# Phase 3 – Network Security Hardening ✅

Completed implementation:

- Implemented Extended Access Control Lists (ACLs)
- Isolated Guest WiFi from trusted VLANs
- Protected switch access ports using Port Security
- Configured Sticky MAC Address learning
- Configured Port Security violation mode
- Hardened router and switch configurations
- Enabled password encryption
- Configured administrative login banner
- Configured session timeout
- Limited SSH authentication attempts
- Disabled unnecessary DNS lookup
- Validated all implemented security controls

---

# VLAN Design

| VLAN | Name | Network | Gateway |
|------|------|----------|----------|
| 10 | Personal | 192.168.10.0/24 | 192.168.10.1 |
| 30 | Guest WiFi | 192.168.30.0/24 | 192.168.30.1 |
| 40 | Servers | 192.168.40.0/24 | 192.168.40.1 |
| 99 | Management | 192.168.99.0/24 | 192.168.99.1 |

---

# Device IP Addressing

| Device | VLAN | IP Address | Assignment |
|---------|------|------------|------------|
| Router (VLAN 10) | 10 | 192.168.10.1 | Gateway |
| Router (VLAN 30) | 30 | 192.168.30.1 | Gateway |
| Router (VLAN 40) | 40 | 192.168.40.1 | Gateway |
| Router (VLAN 99) | 99 | 192.168.99.1 | Gateway |
| Desktop-PC | 10 | 192.168.10.21 | Static |
| Work Laptop | 30 | 192.168.30.3 | Static |
| Mobile Phone | 30 | 192.168.30.2 | Static |
| Tablet | 30 | 192.168.30.4 | Static |
| Home Server | 40 | 192.168.40.10 | Static |
| Network Printer | 40 | 192.168.40.20 | Static |
| Switch Management | 99 | 192.168.99.2 | Static |

---

# Wireless Configuration

Wireless connectivity is provided using Cisco AP-PT.

**SSID**

```
Fahmi-Home-Network
```

**Security**

```
WPA2-PSK
```

**Encryption**

```
AES
```

Connected wireless clients:

- Work Laptop
- Mobile Phone
- Tablet

---

# Security Features

Implemented security controls include:

- VLAN Segmentation
- Router-on-a-Stick
- Inter-VLAN Routing
- SSH Remote Management
- Extended Access Control Lists (ACL)
- Guest WiFi Isolation
- Switch Port Security
- Sticky MAC Address Learning
- Password Encryption
- Administrative Login Banner
- Device Hardening
- Session Timeout Configuration

---

# Project Structure

```text
virtual-home-network/

├── packet-tracer/
│   └── HomeNetwork.pkt
│
├── diagrams/
│
├── configs/
│
├── documentation/
│   ├── 01-network-design.md
│   ├── 02-ip-addressing.md
│   ├── 03-wireless-configuration.md
│   ├── 04-testing-results.md
│   ├── 05-vlan-configuration.md
│   ├── 06-router-on-stick.md
│   ├── 07-ssh-management.md
│   ├── 08-acl-security.md
│   ├── 09-port-security.md
│   ├── 10-device-hardening.md
│   └── 11-phase3-testing.md
│
├── images/
│   └── phase1-topology.png
│
└── README.md
```

---

# Documentation

Detailed implementation guides are available below:

- [01 - Network Design](documentation/01-network-design.md)
- [02 - IP Addressing](documentation/02-ip-addressing.md)
- [03 - Wireless Configuration](documentation/03-wireless-configuration.md)
- [04 - Testing Results](documentation/04-testing-results.md)
- [05 - VLAN Configuration](documentation/05-vlan-configuration.md)
- [06 - Router-on-a-Stick Configuration](documentation/06-router-on-stick.md)
- [07 - SSH Management](documentation/07-ssh-management.md)
- [08 - ACL Security](documentation/08-acl-security.md)
- [09 - Port Security](documentation/09-port-security.md)
- [10 - Device Hardening](documentation/10-device-hardening.md)
- [11 - Phase 3 Testing](documentation/11-phase3-testing.md)

---

# Testing

Testing performed throughout the project includes:

- Device connectivity testing
- DHCP verification
- VLAN verification
- Inter-VLAN routing testing
- Wireless connectivity testing
- SSH remote management testing
- ACL validation
- Port Security verification
- Device hardening verification
- Configuration validation

---

# Future Improvements

Planned enhancements for the final phase include:

- Syslog Server
- Network Time Protocol (NTP)
- Firewall integration
- VPN remote access
- Network monitoring
- Security logging
- Intrusion Detection System (IDS) simulation
- Final security audit

---

# Author

**Muhammad Fahmi**

Cybersecurity Student  
Multimedia University (MMU)
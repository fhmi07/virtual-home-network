# Secure Virtual Home Network

## Project Overview

This project demonstrates the design and implementation of a secure virtual home network using Cisco Packet Tracer.

The objective of this project is to simulate a realistic home network environment while applying networking and cybersecurity concepts such as IP addressing, DHCP configuration, wireless networking, VLAN segmentation, inter-VLAN routing, secure remote management, and network hardening.

The project is developed in multiple phases, starting with a functional network foundation before implementing cybersecurity improvements.

---

# Objectives

- Design a functional and secure home network topology
- Configure routers, switches, and wireless devices
- Implement proper IP addressing and network communication
- Configure DHCP services for client devices
- Implement VLAN-based network segmentation
- Configure secure device management using SSH
- Apply cybersecurity practices to improve network security
- Document network configurations and testing results

---

# Technologies Used

- Cisco Packet Tracer
- Cisco IOS Command Line Interface (CLI)
- IPv4 Networking
- DHCP
- VLAN Configuration
- Router-on-a-Stick (802.1Q Trunking)
- Inter-VLAN Routing
- SSH Remote Management
- Access Control Lists (ACL)
- Switch Port Security
- Git & GitHub

---

# Network Devices Used

| Device | Purpose |
|---|---|
| Cisco ISR 4331 Router | Routing, DHCP, and inter-VLAN communication |
| Cisco Catalyst 2960 Switch | LAN connectivity and VLAN management |
| Cisco AP-PT | Wireless network access |
| Desktop-PC | Personal wired client |
| Work-Laptop | Wireless client |
| Home Server | Internal network service |
| Network Printer | Network peripheral |
| Mobile Phone | Wireless client |
| Tablet | Wireless client |

---

# Network Topology

![Phase 1 Network Topology](images/phase1-topology.png)

---

# Phase 1: Functional Home Network ✅

Completed implementation:

- Designed basic home network topology
- Configured Cisco ISR 4331 router
- Configured Catalyst 2960 switch connectivity
- Implemented DHCP services
- Assigned static IP addresses for server and printer
- Configured wireless connectivity using AP-PT
- Connected wired and wireless clients
- Performed connectivity testing

---

# Phase 2: Network Segmentation and Secure Management ✅

Completed implementation:

- Created VLAN-based network segmentation
- Configured separate networks for personal devices, guest WiFi, servers, and management
- Implemented 802.1Q trunking between router and switch
- Configured router-on-a-stick using router subinterfaces
- Enabled inter-VLAN routing
- Configured SSH remote management for secure switch administration
- Tested communication between VLAN networks

---

# VLAN Design and IP Addressing

| VLAN | Purpose | Network | Gateway |
|---|---|---|---|
| VLAN 10 | Personal Devices | 192.168.10.0/24 | 192.168.10.1 |
| VLAN 30 | Guest WiFi | 192.168.30.0/24 | 192.168.30.1 |
| VLAN 40 | Servers | 192.168.40.0/24 | 192.168.40.1 |
| VLAN 99 | Management | 192.168.99.0/24 | 192.168.99.1 |

---

# Device IP Addressing

| Device | VLAN | IP Address | Assignment |
|---|---|---|---|
| Router VLAN 10 | VLAN 10 | 192.168.10.1 | Gateway |
| Router VLAN 30 | VLAN 30 | 192.168.30.1 | Gateway |
| Router VLAN 40 | VLAN 40 | VLAN 40 | Gateway |
| Router VLAN 99 | VLAN 99 | 192.168.99.1 | Gateway |
| Desktop-PC | VLAN 10 | 192.168.10.21 | Static |
| Work-Laptop | VLAN 30 | 192.168.30.3 | Static |
| Mobile Phone | VLAN 30 | 192.168.30.2 | Static |
| Tablet | VLAN 30 | 192.168.30.4 | Static |
| Home Server | VLAN 40 | 192.168.40.10 | Static |
| Network Printer | VLAN 40 | 192.168.40.20 | Static |
| Switch Management | VLAN 99 | 192.168.99.2 | Static |

---

# Wireless Configuration

Wireless network implemented using Cisco AP-PT.

SSID:

```
Fahmi-Home-Network
```

Security:

```
WPA2-PSK
```

Encryption:

```
AES
```

Wireless clients:

- Work-Laptop
- Mobile Phone
- Tablet

---

# Project Structure

```
virtual-home-network/

├── packet-tracer/
│   └── Cisco Packet Tracer project files
│
├── diagrams/
│   └── Network topology diagrams
│
├── configs/
│   └── Device configuration files
│
├── documentation/
│   └── Technical documentation
│
└── images/
    └── Screenshots and project visuals
```

---

# Documentation

Detailed project documentation:

- [Basic Network Setup](documentation/01-network-design.md)
- [IP Addressing](documentation/02-ip-addressing.md)
- [Wireless Configuration](documentation/03-wireless-configuration.md)
- [Testing Results](documentation/04-testing-results.md)
- [VLAN Configuration](documentation/05-vlan-configuration.md)
- [Router-on-a-Stick Configuration](documentation/06-router-on-stick.md)
- [SSH Management](documentation/07-ssh-management.md)

---

# Security Implementation

## Completed Security Features

- VLAN-based network segmentation
- Network separation between personal, guest, server, and management networks
- Secure device management using SSH
- Strong authentication configuration
- Basic network hardening practices

## Future Security Enhancements

Future improvements include:

- Access Control Lists (ACL)
- Switch port security
- Guest WiFi isolation rules
- Firewall implementation
- IDS monitoring simulation
- Network logging and security analysis

---

# Testing

Testing performed:

- Device connectivity testing
- IP address verification
- VLAN communication testing
- Inter-VLAN routing verification
- SSH remote management testing
- Configuration validation

---

# Future Improvements

Future enhancements may include:

- Firewall configuration
- Intrusion Detection System (IDS) simulation
- IoT device security
- VPN configuration
- Network monitoring and logging
- Security event analysis

---

# Author

Muhammad Fahmi

Cybersecurity Student  
Multimedia University (MMU)
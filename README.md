# Secure Virtual Home Network

## Project Overview

This project demonstrates the design and implementation of a secure virtual home network using Cisco Packet Tracer.

The project simulates a realistic home network while applying networking and cybersecurity concepts including VLAN segmentation, inter-VLAN routing, wireless networking, Access Control Lists (ACLs), SSH remote management, switch port security, and device hardening.

The project is developed in multiple phases, progressing from a functional network to a security-focused architecture.

---

# Objectives

- Design a functional home network topology
- Configure routers, switches, and wireless devices
- Implement IPv4 addressing and DHCP
- Configure VLAN segmentation
- Implement secure remote management using SSH
- Restrict network traffic using ACLs
- Protect switch ports using Port Security
- Apply Cisco device hardening best practices
- Document configurations and testing results

---

# Technologies Used

- Cisco Packet Tracer
- Cisco IOS CLI
- IPv4 Networking
- DHCP
- VLANs
- Router-on-a-Stick
- SSH
- Access Control Lists (ACL)
- Switch Port Security
- Device Hardening
- Git & GitHub

---

# Network Devices

| Device | Purpose |
|---------|---------|
| Cisco ISR 4331 | Routing, DHCP, Inter-VLAN Routing |
| Cisco Catalyst 2960 | Layer 2 Switching |
| Cisco AP-PT | Wireless Access Point |
| Desktop-PC | Personal Device |
| Work Laptop | Wireless Client |
| Home Server | Internal Services |
| Network Printer | Shared Resource |
| Mobile Phone | Guest WiFi Client |
| Tablet | Guest WiFi Client |

---

# Network Topology

![Network Topology](images/phase1-topology.png)

---

# Implemented Features

## Phase 1 – Network Foundation

- Home network topology
- DHCP configuration
- Static IP assignment
- Wireless network
- Connectivity testing

---

## Phase 2 – Network Segmentation

- VLAN 10 – Personal
- VLAN 30 – Guest WiFi
- VLAN 40 – Servers
- VLAN 99 – Management
- Router-on-a-Stick
- Inter-VLAN Routing
- SSH Remote Management

---

## Phase 3 – Network Security

- Extended Access Control Lists (ACL)
- Guest WiFi Isolation
- Switch Port Security
- Sticky MAC Address Learning
- Device Hardening
- Password Encryption
- Login Banner
- Secure SSH Configuration
- Session Timeout Configuration

---

# VLAN Design

| VLAN | Name | Network |
|------|------|----------|
| 10 | Personal | 192.168.10.0/24 |
| 30 | Guest WiFi | 192.168.30.0/24 |
| 40 | Servers | 192.168.40.0/24 |
| 99 | Management | 192.168.99.0/24 |

---

# Security Features

- VLAN Segmentation
- Router-on-a-Stick
- SSH Management
- Access Control Lists (ACL)
- Guest Network Isolation
- Switch Port Security
- Sticky MAC Address Learning
- Password Encryption
- Device Hardening
- Administrative Login Banner

---

# Project Structure

```
virtual-home-network/

├── packet-tracer/
├── diagrams/
├── configs/
├── documentation/
├── images/
└── README.md
```

---

# Documentation

- 01 Network Design
- 02 IP Addressing
- 03 Wireless Configuration
- 04 Testing Results
- 05 VLAN Configuration
- 06 Router-on-a-Stick Configuration
- 07 SSH Management
- 08 ACL Security
- 09 Port Security
- 10 Device Hardening
- 11 Phase 3 Testing

---

# Future Improvements

- Syslog Server
- NTP Configuration
- Network Monitoring
- Firewall Integration
- VPN Remote Access
- IDS / IPS Simulation

---

# Author

Muhammad Fahmi

Cybersecurity Student  
Multimedia University (MMU)
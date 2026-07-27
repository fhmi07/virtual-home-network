# Network Design Overview

## Project Purpose

The purpose of this project is to design and implement a secure virtual home network using Cisco Packet Tracer.

The network simulates a realistic home environment containing personal devices, wireless clients, internal services, and network management infrastructure while applying networking and cybersecurity concepts.

The project is implemented in multiple phases, beginning with a functional network foundation followed by security improvements through segmentation and secure management.

---

# Network Requirements

The virtual home network is designed to support:

- Wired and wireless device connectivity
- Internal network communication
- DHCP services
- VLAN-based network segmentation
- Inter-VLAN routing
- Secure remote device management
- Future security controls such as ACL and port security

---

# Network Devices

The following devices are implemented:

| Device | Purpose |
|---|---|
| Cisco ISR 4331 Router | Provides routing, DHCP services, and inter-VLAN communication |
| Cisco Catalyst 2960 Switch | Provides LAN connectivity and VLAN management |
| Cisco AP-PT | Provides wireless network access |
| Desktop-PC | Represents trusted personal workstation |
| Work-Laptop | Represents wireless client device |
| Home Server | Provides internal network services |
| Network Printer | Represents shared network peripheral |
| Mobile Phone | Represents wireless client |
| Tablet | Represents wireless client |

---

# Implemented Network Architecture

The network follows a segmented architecture using VLANs.

```
                         ISR 4331 Router
                              |
                       802.1Q Trunk Link
                              |
                       Catalyst 2960 Switch
                              |
        ------------------------------------------------
        |                 |              |              |
     VLAN 10          VLAN 30        VLAN 40        VLAN 99
    PERSONAL        GUEST_WIFI      SERVERS      MANAGEMENT
        |                 |              |              |
    Desktop-PC       Laptop         Server        Switch SSH
                     Phone          Printer
                     Tablet
```

---

# VLAN Design

| VLAN | Name | Purpose |
|---|---|---|
| VLAN 10 | PERSONAL | Trusted personal devices |
| VLAN 30 | GUEST_WIFI | Wireless client devices |
| VLAN 40 | SERVERS | Internal servers and network services |
| VLAN 99 | MANAGEMENT | Network device administration |

---

# Routing Design

Inter-VLAN communication is implemented using a router-on-a-stick design.

The ISR 4331 router uses subinterfaces with 802.1Q encapsulation to provide gateways for each VLAN.

Example:

```
GigabitEthernet0/0/0.10
192.168.10.1

GigabitEthernet0/0/0.30
192.168.30.1

GigabitEthernet0/0/0.40
192.168.40.1

GigabitEthernet0/0/0.99
192.168.99.1
```

---

# Security Considerations

Implemented security features:

- VLAN-based network segmentation
- Separate management network
- Secure remote management using SSH
- Strong authentication configuration
- Network configuration documentation

Future security enhancements:

- Access Control Lists (ACL)
- Switch port security
- Firewall implementation
- Intrusion Detection System simulation
- Network monitoring and logging

---

# Future Expansion

Possible future improvements:

- Internet access simulation
- Firewall deployment
- VPN access
- IoT network isolation
- Security event monitoring
- Advanced access control policies
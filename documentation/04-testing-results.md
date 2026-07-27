# Phase 1 Testing Results

## Overview

Phase 1 focused on implementing a functional virtual home network environment using Cisco Packet Tracer.

The objective was to establish wired and wireless connectivity, configure DHCP services, assign static IP addresses, and verify communication between network devices.

---

# Connectivity Testing

## Router Connectivity

All network devices successfully communicated with the ISR 4331 router.

Router IP:

192.168.10.1

Result:

PASS

---

## Internal Network Communication

Server:

192.168.10.10

Printer:

192.168.10.20

Testing performed:

- Desktop-PC to Server
- Work-Laptop to Server
- Wireless clients to Server
- Wired and wireless device communication

Result:

PASS

---

## DHCP Testing

The ISR 4331 router was configured as the DHCP server for client devices.

Dynamic IP assignments:

| Device | IP Address |
|---|---|
| Desktop-PC | 192.168.10.21 |
| Work-Laptop | 192.168.10.24 |
| Mobile Phone | 192.168.10.26 |
| Tablet | 192.168.10.27 |

Result:

PASS

---

## Wireless Testing

Wireless connectivity was implemented using Cisco AP-PT.

The Access Point functions as a Layer 2 wireless bridge, allowing wireless devices to communicate with the wired LAN.

SSID:

Fahmi-Home-Network

Security:

WPA2-PSK

Encryption:

AES

Connected wireless clients:

- Work-Laptop
- Mobile Phone
- Tablet

Result:

PASS

---

# Phase 1 Conclusion

The virtual home network was successfully implemented and tested.

The completed network provides:

- Wired LAN connectivity
- Wireless connectivity
- DHCP services
- Static IP management
- Internal device communication

The next phase will focus on improving network security through:

- VLAN segmentation
- Secure device management
- Access control policies
- Network hardening techniques
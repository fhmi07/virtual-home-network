# Wireless Network Configuration

## Overview

Wireless connectivity was implemented using Cisco AP-PT to provide WiFi access for mobile devices within the virtual home network.

The Access Point operates as a Layer 2 wireless bridge, allowing wireless clients to communicate with the wired LAN through the Catalyst 2960 switch.

---

## Wireless Device

Device:

Cisco AP-PT

Connection:

AP-PT connected to Catalyst 2960 switch.

---

## Wireless Configuration

SSID:

Fahmi-Home-Network

Security:

WPA2-PSK

Encryption:

AES

---

## Connected Wireless Clients

| Device | IP Address |
|---|---|
| Work-Laptop | 192.168.10.24 |
| Mobile Phone | 192.168.10.26 |
| Tablet | 192.168.10.27 |

---

## DHCP Integration

Wireless clients obtain IP addresses automatically from the ISR 4331 router DHCP service.

---

## Result

Wireless connectivity was successfully implemented and tested.

Wireless devices were able to communicate with:

- Router
- Server
- Wired clients
- Other wireless clients
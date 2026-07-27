# Wireless Network Configuration

## Overview

Wireless connectivity was implemented using Cisco AP-PT to provide wireless access within the virtual home network.

The Access Point operates as a Layer 2 wireless bridge, allowing wireless clients to connect to the network through the Catalyst 2960 switch.

During Phase 2, the wireless network was separated into its own VLAN to improve network organization and security.

---

# Wireless Device

Device:

```
Cisco AP-PT
```

Connection:

```
AP-PT connected to Catalyst 2960 switch
```

Switch Port:

```
FastEthernet0/6
```

Assigned VLAN:

```
VLAN 30 - GUEST_WIFI
```

---

# Wireless Configuration

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

---

# Wireless Network Design

Wireless clients are placed into:

```
VLAN 30 - GUEST_WIFI
```

Network:

```
192.168.30.0/24
```

Default Gateway:

```
192.168.30.1
```

---

# Connected Wireless Clients

| Device | VLAN | IP Address |
|---|---|---|
| Work-Laptop | VLAN 30 | 192.168.30.3 |
| Mobile Phone | VLAN 30 | 192.168.30.2 |
| Tablet | VLAN 30 | 192.168.30.4 |

---

# DHCP Integration

Wireless clients receive IP addresses from the ISR 4331 router DHCP service.

DHCP network:

```
192.168.30.0/24
```

Gateway assigned:

```
192.168.30.1
```

---

# Testing

Wireless connectivity was tested by verifying:

- Client connection to AP-PT
- IP address assignment
- Communication with router
- Communication with other VLAN networks

Testing results:

PASS

---

# Result

Wireless connectivity was successfully implemented.

The wireless network now provides:

- Secure WiFi access using WPA2-PSK
- Separate guest wireless VLAN
- DHCP-based IP assignment
- Communication through inter-VLAN routing
- Improved network segmentation
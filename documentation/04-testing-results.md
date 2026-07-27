# Network Testing Results

## Overview

Testing was performed throughout the implementation phases of the virtual home network.

Phase 1 focused on establishing a functional network environment including wired connectivity, wireless connectivity, DHCP services, and basic communication testing.

Phase 2 focused on validating network segmentation, VLAN configuration, inter-VLAN routing, and secure remote management using SSH.

---

# Phase 1 Testing Results

## Router Connectivity

All network devices successfully communicated with the ISR 4331 router.

Router:

```
192.168.10.1
```

Result:

PASS

---

## Internal Network Communication

Initial testing was performed on the flat network design.

Devices tested:

- Desktop-PC to Server
- Desktop-PC to Printer
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

Connected wireless clients:

- Work-Laptop
- Mobile Phone
- Tablet

Result:

PASS

---

# Phase 2 Testing Results

## VLAN Configuration Testing

The switch was configured with multiple VLANs to separate network traffic.

Configured VLANs:

| VLAN | Purpose |
|---|---|
| VLAN 10 | Personal Devices |
| VLAN 30 | Guest WiFi |
| VLAN 40 | Servers |
| VLAN 99 | Management |

Verification command:

```
show vlan brief
```

Result:

PASS

---

## Trunk Link Testing

The connection between the ISR 4331 router and Catalyst 2960 switch was configured as an 802.1Q trunk.

Interface:

```
Router G0/0/0
|
Switch Gi0/1
```

Verification command:

```
show interfaces trunk
```

Expected result:

```
Gig0/1 trunking
```

Result:

PASS

---

## Inter-VLAN Routing Testing

Router-on-a-stick was implemented using router subinterfaces.

Configured gateways:

| VLAN | Gateway |
|---|---|
| VLAN 10 | 192.168.10.1 |
| VLAN 30 | 192.168.30.1 |
| VLAN 40 | 192.168.40.1 |
| VLAN 99 | 192.168.99.1 |

Connectivity tests:

| Source | Destination | Result |
|---|---|---|
| Desktop-PC (192.168.10.21) | Server (192.168.40.10) | PASS |
| Desktop-PC (192.168.10.21) | Mobile Phone (192.168.30.2) | PASS |

Result:

PASS

---

## SSH Remote Management Testing

Secure remote management was configured on the Catalyst 2960 switch.

Switch Management IP:

```
192.168.99.2
```

Testing performed:

- SSH connection from Desktop-PC
- User authentication verification
- Privileged EXEC access verification

SSH command:

```
ssh -l fahmi 192.168.99.2
```

Result:

PASS

---

# Current Network Status

The virtual home network currently provides:

- Wired network connectivity
- Wireless network connectivity
- VLAN-based segmentation
- Inter-VLAN communication
- Secure remote switch management
- Separate personal, guest, server, and management networks

---

# Future Testing

Future phases will include testing of:

- ACL traffic filtering
- Guest network isolation
- Switch port security
- Firewall rules
- Network monitoring capabilities
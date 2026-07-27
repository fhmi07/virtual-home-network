# IP Addressing Plan

## Network Information

The virtual home network uses multiple IPv4 networks to support VLAN-based segmentation.

Subnet Mask:

```
255.255.255.0
```

---

# VLAN Addressing Scheme

| VLAN | Purpose | Network | Default Gateway |
|---|---|---|---|
| VLAN 10 | Personal Devices | 192.168.10.0/24 | 192.168.10.1 |
| VLAN 30 | Guest WiFi | 192.168.30.0/24 | 192.168.30.1 |
| VLAN 40 | Servers | 192.168.40.0/24 | 192.168.40.1 |
| VLAN 99 | Management | 192.168.99.0/24 | 192.168.99.1 |

---

# Static Devices

| Device | VLAN | IP Address |
|---|---|---|
| Home-Router VLAN 10 | VLAN 10 | 192.168.10.1 |
| Home-Router VLAN 30 | VLAN 30 | 192.168.30.1 |
| Home-Router VLAN 40 | VLAN 40 | 192.168.40.1 |
| Home-Router VLAN 99 | VLAN 99 | 192.168.99.1 |
| Home-Server | VLAN 40 | 192.168.40.10 |
| Network-Printer | VLAN 40 | 192.168.40.20 |
| Home-Switch Management | VLAN 99 | 192.168.99.2 |

---

# Client Devices

| Device | VLAN | IP Address | Assignment |
|---|---|---|---|
| Desktop-PC | VLAN 10 | 192.168.10.21 | Static |
| Work-Laptop | VLAN 30 | 192.168.30.3 | Static |
| Mobile Phone | VLAN 30 | 192.168.30.2 | Static |
| Tablet | VLAN 30 | 192.168.30.4 | Static |

---

# DHCP Configuration

DHCP services are provided by the ISR 4331 router.

Configured DHCP networks:

## VLAN 10 - Personal Devices

Network:

```
192.168.10.0/24
```

Gateway:

```
192.168.10.1
```

---

## VLAN 30 - Guest WiFi

Network:

```
192.168.30.0/24
```

Gateway:

```
192.168.30.1
```

---

# Addressing Design Explanation

The network was divided into multiple subnets using VLANs to improve:

- Network organization
- Traffic separation
- Security control
- Future scalability

Each VLAN represents a different network segment, allowing security policies such as ACL filtering and access restrictions to be implemented in future phases.
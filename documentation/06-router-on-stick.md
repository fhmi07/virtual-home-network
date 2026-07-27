# Router-on-a-Stick Configuration

## Overview

Inter-VLAN routing was implemented using a router-on-a-stick design.

The ISR 4331 router uses a single physical interface connected to the Catalyst 2960 switch through an 802.1Q trunk link.

Subinterfaces were configured on the router to provide gateways for each VLAN.

---

## Network Design

Connection:

```
ISR 4331 G0/0/0
        |
        |
802.1Q Trunk
        |
        |
Catalyst 2960 Gi0/1
```

---

## Router Subinterfaces

| Interface | VLAN | Gateway |
|---|---|---|
| G0/0/0.10 | VLAN 10 | 192.168.10.1 |
| G0/0/0.30 | VLAN 30 | 192.168.30.1 |
| G0/0/0.40 | VLAN 40 | 192.168.40.1 |
| G0/0/0.99 | VLAN 99 | 192.168.99.1 |

---

## Switch Trunk Configuration

The switch port connected to the router was configured as a trunk port.

Interface:

```
GigabitEthernet0/1
```

Verification command:

```
show interfaces trunk
```

---

## Testing

Inter-VLAN communication was tested between network segments.

Tests performed:

| Source | Destination | Result |
|---|---|---|
| Desktop-PC | Server | PASS |
| Desktop-PC | Mobile Phone | PASS |

---

## Result

Router-on-a-stick was successfully implemented.

The router is now able to route traffic between VLAN networks while maintaining network segmentation.
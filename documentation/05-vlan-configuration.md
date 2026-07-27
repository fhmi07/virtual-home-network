# VLAN Configuration

## Overview

VLAN segmentation was implemented to divide the virtual home network into separate logical networks.

The purpose of VLAN implementation is to improve network organization, reduce unnecessary traffic, and provide a foundation for future security controls such as ACL filtering and access restrictions.

---

## Configured VLANs

| VLAN ID | Name | Purpose |
|---|---|---|
| VLAN 10 | PERSONAL | Trusted personal devices |
| VLAN 30 | GUEST_WIFI | Wireless client devices |
| VLAN 40 | SERVERS | Internal services and network peripherals |
| VLAN 99 | MANAGEMENT | Network device administration |

---

## Switch Port Assignment

| Interface | Connected Device | VLAN |
|---|---|---|
| Fa0/2 | Desktop-PC | VLAN 10 |
| Fa0/4 | Home Server | VLAN 40 |
| Fa0/5 | Printer | VLAN 40 |
| Fa0/6 | AP-PT | VLAN 30 |
| Gi0/1 | Router | Trunk |

---

## VLAN Verification

The following command was used to verify VLAN configuration:

```
show vlan brief
```

Expected result:

- VLANs 10, 30, 40, and 99 are active
- Devices are assigned to the correct VLANs

---

## Result

VLAN segmentation was successfully implemented.

The network is now separated into multiple logical segments, allowing future security policies to be applied between different network zones.
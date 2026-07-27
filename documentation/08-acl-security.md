# Access Control List (ACL) Security

## Overview

Extended Access Control Lists (ACLs) were implemented on the ISR 4331 router to restrict communication between VLANs.

The primary objective was to isolate the Guest WiFi network from trusted internal resources while allowing legitimate traffic within the network.

---

# ACL Design

ACL Name:

GUEST_WIFI_FILTER

Applied Interface:

GigabitEthernet0/0/0.30

Direction:

Inbound

---

# Security Policy

| Source | Destination | Action |
|---------|-------------|--------|
| Guest WiFi (VLAN 30) | Personal VLAN (VLAN 10) | Deny |
| Guest WiFi (VLAN 30) | Server VLAN (VLAN 40) | Deny |
| Guest WiFi (VLAN 30) | Management VLAN (VLAN 99) | Deny |
| Guest WiFi (VLAN 30) | Other Traffic | Permit |

---

# Configuration Summary

- Extended ACL created
- Applied inbound on Guest WiFi interface
- Guest network isolated from trusted VLANs
- Inter-VLAN security enforced

---

# Testing

Verified that Guest WiFi devices could not communicate with:

- Personal devices
- Home Server
- Management VLAN

ACL hit counters confirmed that blocked traffic matched the configured rules.
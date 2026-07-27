# SSH Management Configuration

## Overview

Secure remote management was implemented using SSH on the Catalyst 2960 switch.

SSH allows administrators to securely access network devices through encrypted communication instead of using insecure remote management protocols.

---

## Management Network

Management VLAN:

```
VLAN 99
```

Switch Management IP:

```
192.168.99.2
```

Default Gateway:

```
192.168.99.1
```

---

## SSH Configuration

SSH access was configured with:

- Local user authentication
- Encrypted remote access
- Privileged EXEC access

SSH login:

```
ssh -l fahmi 192.168.99.2
```

---

## Authentication

Username:

```
fahmi
```

Password:

```
Configured locally
```

---

## Testing

SSH connection was tested from Desktop-PC.

Testing steps:

1. Open Desktop-PC command prompt
2. Connect to switch using SSH
3. Authenticate using configured credentials
4. Access privileged EXEC mode

Result:

PASS

---

## Security Benefit

SSH improves network security by:

- Encrypting management traffic
- Preventing plaintext credential transmission
- Providing controlled administrator access

---

## Result

Secure remote management was successfully implemented on the Catalyst 2960 switch.
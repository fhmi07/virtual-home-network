# Switch Port Security

## Overview

Port Security was implemented on the Catalyst 2960 switch to prevent unauthorized devices from connecting to the network.

Sticky MAC address learning was used so the switch automatically learns and secures the first connected device.

---

# Protected Interfaces

| Interface | Device |
|-----------|--------|
| Fa0/2 | Desktop-PC |
| Fa0/4 | Home Server |
| Fa0/5 | Network Printer |

---

# Configuration

Security Features:

- Maximum MAC Address: 1
- Sticky MAC Address Learning
- Violation Mode: Shutdown

---

# Benefits

Port Security provides protection against:

- Unauthorized device connections
- MAC flooding attacks
- Physical network misuse

---

# Verification

Port Security status confirmed:

- Secure-Up state
- Sticky MAC learned successfully
- No security violations detected
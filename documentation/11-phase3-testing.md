# Phase 3 Testing Results

## Overview

Phase 3 focused on validating the network security controls implemented within the virtual home network.

Testing confirmed that the configured security features operated as expected.

---

# ACL Testing

| Test | Result |
|------|--------|
| Guest WiFi → Personal VLAN | PASS (Blocked) |
| Guest WiFi → Server VLAN | PASS (Blocked) |
| Guest WiFi → Management VLAN | PASS (Blocked) |
| Personal VLAN → Server VLAN | PASS |

---

# Port Security Testing

Verified:

- Port Security enabled
- Sticky MAC learning operational
- Protected interfaces secured
- No security violations detected

Result:

PASS

---

# SSH Testing

Verified:

- SSH remote login
- Local user authentication
- Successful administrative access

Result:

PASS

---

# Device Hardening Testing

Verified:

- Password encryption enabled
- Login banner displayed
- Session timeout configured
- DNS lookup disabled

Result:

PASS

---

# Phase 3 Conclusion

The virtual home network now incorporates multiple layers of security, including network segmentation, traffic filtering, secure remote management, port-level protection, and device hardening.

These controls significantly improve the security posture of the simulated network while demonstrating enterprise networking and cybersecurity best practices.
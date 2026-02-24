# Network+ Mini Enterprise Lab (Packet Tracer)

# VLAN + Inter-VLAN Routing + DHCP + ACL + Port Security Lab

## 📌 Objective
Simulate a small enterprise network with:

- Multiple VLANs
- Inter-VLAN routing (Router-on-a-Stick)
- DHCP configuration
- Extended ACL implementation
- Port Security
- Trunk configuration
- STP verification

---

## 🏗 Topology Overview

- 2 Access Switches
- 1 Router (Core)
- VLANs:
  - VLAN 10 → Sales
  - VLAN 20 → HR
  - VLAN 99 → Management

---

## ⚙️ Technologies Used

- 802.1Q Trunking
- Subinterfaces (Router-on-a-Stick)
- DHCP Pools
- Extended ACL (deny VLAN10 → VLAN99)
- Port Security (Sticky MAC)
- Spanning Tree Protocol

---

## 🔐 Security Implementation

- VLAN 10 denied access to VLAN 99
- Port Security enabled on access port
- Management VLAN isolated

---

## 🧪 Verification Steps

- `show vlan brief`
- `show interfaces trunk`
- `show ip route`
- `show access-lists`
- `show port-security`
- DHCP auto-assignment verified
- ACL tested via ping

---

## 📸 Screenshots

See `/screenshots` folder.

---

## 🚀 Skills Demonstrated

- Layer 2 & Layer 3 integration
- Traffic segmentation
- Access control
- Troubleshooting
- Enterprise switch configuration
  ---

## 🛠 Troubleshooting Encountered

During DHCP testing, PC3 failed to obtain an IP address and received an APIPA address instead.

Root cause:
- The PC was assigned to the wrong VLAN.

Resolution:
- Verified switch port VLAN assignment.
- Corrected the VLAN configuration.
- Renewed DHCP request successfully.

Lesson learned:
Always verify VLAN membership before troubleshooting DHCP or routing issues.

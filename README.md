# router-on-a-stick-vlan-lab
Cisco Packet Tracer lab implementing VLAN segmentation and inter-VLAN routing using Router-on-a-Stick with 2 VLANs, trunk configuration, and subnet separation.
# Router-on-a-Stick VLAN Lab (Multi-PC Network)

## Objective
To design and configure a VLAN-based network using Router-on-a-Stick to enable inter-VLAN communication.

---

## Network Overview
- 6 PCs connected to a single switch
- 2 VLANs configured:
  - VLAN 10 (IT Department) → 3 PCs
  - VLAN 20 (HR Department) → 3 PCs
- Inter-VLAN routing enabled using a router

---

## Technologies Used
- VLAN (Virtual LAN)
- 802.1Q Trunking
- Router-on-a-Stick (Subinterfaces)
- Cisco Packet Tracer

---

## Configuration Summary

### Switch Configuration
- Created VLAN 10 and VLAN 20
- Assigned access ports to respective VLANs
- Configured trunk port between switch and router

### Router Configuration
- Created subinterfaces for VLAN 10 and VLAN 20
- Assigned IP addresses as default gateways
- Enabled 802.1Q encapsulation

---

## Key Learnings
- Devices in the same VLAN communicate directly at Layer 2
- Inter-VLAN communication requires Layer 3 routing
- Trunk links carry traffic for multiple VLANs using tagging
- Each VLAN requires its own subnet and gateway

---

## Observation
Initial ping between VLANs failed due to ARP resolution delay, which is normal behavior in first-time communication between devices.

---

## Verification Commands Used
- `show vlan brief`
- `show ip interface brief`
- `ping`
- `show interfaces trunk`

---

## Conclusion
This lab helped reinforce VLAN segmentation, trunking, and inter-VLAN routing concepts by implementing a real multi-PC network scenario.

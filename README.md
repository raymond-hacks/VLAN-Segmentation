# SOHO Network VLAN Segmentation & Inter-VLAN Routing

A Cisco Packet Tracer project demonstrating VLAN segmentation, 802.1Q trunking, and inter-VLAN routing using a router-on-a-stick design.

## Project Overview

This project simulates a small-office/home-office (SOHO) network in which three departments are logically separated into different Virtual Local Area Networks (VLANs).

The design uses VLANs to separate broadcast domains and a router to enable Layer 3 communication between the departmental networks.

**Project status:** Implemented in Cisco Packet Tracer. See the verification evidence for tested functionality.

## Objectives

- Create and name VLANs for three departments.
- Assign switch access ports to the correct VLANs.
- Configure trunking to carry VLAN traffic between network devices.
- Configure router subinterfaces for inter-VLAN routing.
- Assign IP addresses and default gateways.
- Verify VLAN membership, trunk status, and end-to-end connectivity.
- Document troubleshooting and configuration decisions.

## Technologies Used

- Cisco Packet Tracer
- Cisco IOS CLI
- Virtual LANs (VLANs)
- IEEE 802.1Q trunking
- Router-on-a-stick
- IPv4 addressing and subnetting
- ICMP connectivity testing

## Network Topology

![Network topology](topology/network-topology.png)

The topology diagram illustrates the network devices, VLAN assignments, IP subnets, and links used in the simulation.

## VLAN and IP Addressing Plan

| VLAN ID | Department | Network | Default Gateway |
|---|---|---|---|
| 10 | Sales | 192.168.10.0/24 | 192.168.10.1 |
| 20 | HR | 192.168.20.0/24 | 192.168.20.1 |
| 30 | IT | 192.168.30.0/24 | 192.168.30.1 |

The default gateways are configured on the corresponding router subinterfaces.

## Implementation

1. Created VLANs 10, 20, and 30 on the switch.
2. Assigned end-device ports to their respective VLANs.
3. Configured the required trunk link.
4. Created router subinterfaces for the VLANs.
5. Configured 802.1Q encapsulation and gateway IP addresses.
6. Assigned IPv4 addresses and default gateways to end devices.
7. Tested connectivity within and between VLANs.

See the `configs/` directory for the device configurations.

## Verification

The following commands can be used to validate the configuration:

| Command | Purpose |
|---|---|
| `show vlan brief` | Verify VLANs and access-port assignments |
| `show interfaces trunk` | Check trunk status and allowed VLANs |
| `show ip interface brief` | Check interface status and IP addresses |
| `show running-config` | Inspect active device configuration |
| `ping <destination-IP>` | Test end-to-end connectivity |

Screenshots of the actual test results are available in the `screenshots/` directory.

## Troubleshooting

Use a structured troubleshooting process:

1. Verify the host IP address, subnet mask, and default gateway.
2. Check VLAN membership on the switch.
3. Confirm that the trunk link is operational and carries the required VLANs.
4. Verify router subinterface configuration and interface status.
5. Test connectivity to the local gateway before testing remote VLANs.

Document any issues encountered, their root causes, and the corrections made during the lab.

## Repository Contents

- `topology/` — network topology diagram.
- `packet-tracer/` — Cisco Packet Tracer simulation file.
- `configs/` — device configuration and verification command references.
- `screenshots/` — implementation and test evidence.
- `docs/` — additional documentation and troubleshooting notes.

## Key Learning Outcomes

- VLAN creation and logical network segmentation.
- Access-port and trunk configuration.
- Router-on-a-stick inter-VLAN routing.
- IPv4 addressing and default gateway configuration.
- Layer 2 and Layer 3 verification.
- Systematic network troubleshooting.

## Conclusion

This project demonstrates the configuration and verification of a segmented network in Cisco Packet Tracer. It forms part of a practical networking portfolio focused on switching, routing, and troubleshooting.

Author: Raymond Nyongesa

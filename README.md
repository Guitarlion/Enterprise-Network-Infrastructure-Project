# Enterprise-Network-Infrastructure-Project
Cisco Packet Tracer enterprise network project featuring multi-area OSPF, six departmental VLANs, inter-VLAN routing, VLSM subnetting, extended ACLs, and network troubleshooting.



**Cisco Packet Tracer | Multi-Area OSPF | VLANs | Inter-VLAN Routing | VLSM | ACLs**

## Project Overview

This project demonstrates the design, configuration, and troubleshooting of a simulated multi-site enterprise network using Cisco Packet Tracer.

The network was designed to simulate an organization with multiple departments distributed across two locations, using VLAN segmentation, dynamic routing, and access control policies to provide connectivity while restricting unauthorized access to network resources.

The primary objective is to gain hands-on experience with enterprise networking technologies while preparing for the CCNA certification.

## Network Architecture

<img width="1690" height="657" alt="Screenshot 2026-11-18 at 7 56 55 PM" src="https://github.com/user-attachments/assets/437ee3e0-824e-4368-a3c9-9ab2125836f7" />


The simulated enterprise infrastructure includes:

- Multiple Cisco routers interconnected using multi-area OSPF.
- Cisco switches supporting six departmental VLANs across two locations.
- Router-on-a-stick configurations using IEEE 802.1Q trunking.
- Dedicated server network connected through a separate router.
- Extended Access Control Lists (ACLs) for network security and segmentation.

### VLAN Configuration

| VLAN | Department | Network |
|---|---|---|
| 10 | IT | 192.168.100.0/26 |
| 20 | Human Resources | 192.168.100.64/26 |
| 30 | Finance | 192.168.100.128/26 |
| 40 | Sales | 192.168.200.0/26 |
| 50 | Operations | 192.168.200.64/26 |
| 60 | Management | 192.168.200.128/26 |

**Server Network:** 192.168.150.0/28

## Technologies Implemented

### 1. Multi-Area OSPF Routing

- Configured OSPF to dynamically exchange routing information between interconnected Cisco routers.
- Established and verified OSPF neighbor adjacencies.
- Implemented routing across multiple OSPF areas.
- Verified learned routes using `show ip route` and `show ip ospf neighbor`.

### 2. VLAN Segmentation

- Created six VLANs to separate departmental networks across two simulated locations.
- Configured switch access ports and VLAN membership.
- Implemented IEEE 802.1Q trunking between switches and routers.

### 3. Inter-VLAN Routing

- Configured router-on-a-stick using Cisco router subinterfaces.
- Assigned individual default gateways to departmental VLANs.
- Verified communication between VLANs and remote networks.

### 4. IP Addressing and VLSM

- Designed an IP addressing scheme using Variable Length Subnet Masking.
- Allocated /26 subnets for departmental workstations.
- Configured a /28 subnet for centralized server infrastructure.
- Verified subnet assignments, interface addressing, and routing tables.

### 5. Network Security Using ACLs

- Configured extended ACLs to restrict access to the server network.
- Allowed authorized IT VLAN traffic to access server resources.
- Implemented ICMP reply permissions to support connectivity testing.
- Applied ACLs to Cisco router interfaces.

Additional departmental access restrictions and service-specific permissions are being developed and tested.

### 6. Network Troubleshooting

Performed troubleshooting using:

- `show ip route`
- `show ip ospf neighbor`
- `show ip interface brief`
- `show interfaces trunk`
- `show access-lists`
- `ping`
- `tracert`

**Troubleshooting example:**

During server network integration, the server could successfully ping its local gateway but could not reach remote VLANs.

I investigated routing tables, interface configurations, and ACL policies before identifying an incorrect default gateway configuration on the server.

After correcting the default gateway, I verified successful communication between the server network, remote routers, and workstations.

This reinforced the importance of systematic troubleshooting and validating Layer 3 connectivity before making changes to routing protocols.

## Connectivity Verification


Successfully verified:

- OSPF routing between multiple network segments.
- Communication between workstations across simulated locations.
- Connectivity between the server subnet and remote VLAN gateways.
- Server-to-workstation connectivity across the routed network.
- ACL configuration and interface application.

## Planned Enhancements

The project is actively being expanded to include:

- Centralized DHCP services and DHCP relay.
- Internal DNS resolution.
- HTTP web server for a simulated company intranet.
- Syslog monitoring and NTP synchronization.
- AAA/RADIUS authentication.
- Additional ACL policies and security testing.
- SSH-based administrative access restrictions.

## Project Purpose

This lab provides an opportunity to apply networking concepts in a practical environment, develop Cisco IOS configuration skills, and strengthen my ability to troubleshoot enterprise network infrastructure.

It also serves as an ongoing portfolio project documenting my progress toward the CCNA certification and my transition into network engineering.

## Tools and Technologies

Cisco Packet Tracer | Cisco IOS | OSPF | VLANs | IEEE 802.1Q | TCP/IP | VLSM | Extended ACLs | ICMP | Network Troubleshooting

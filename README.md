# Enterprise Core-Access Network Design with Multi-Department VLAN Segmentation

## Overview
Designed and implemented a 3-tier campus network in Cisco Packet Tracer featuring an Edge Router, a Core Layer 3 Switch performing Inter-VLAN routing, and 3 Access Switches segmenting 6 VLANs across departments.

## Topology Diagram
![Topology Diagram](docs/topology_diagram.png)

## IP Addressing & VLAN Scheme
| VLAN ID | Name | Subnet | Gateway (SVI) | Purpose |
|---|---|---|---|---|
| 10 | SALES      | 172.16.1.0/26   | 172.16.1.62  | Workstations           |
| 20 | IT DEP     | 172.16.1.64/27  | 172.16.1.94  | IT Support and Servers |
| 30 | HR DEP     | 172.16.1.96/27  | 172.16.1.126 | Human Resource         |
| 40 | MANAGEMENT | 172.16.1.126/28 | 172.16.1.142 | Management             |
| 50 | GUEST-WIFI | 172.16.1.144/28 | 172.16.1.158 | Isolated Guests        |

## Key Technical Features
- **Layer 3 Switching (SVIs):** Routed inter-VLAN traffic at line rate on the Core switch using `ip routing`.
- **802.1Q Trunking:** Dynamic trunk configuration carrying all VLAN traffic to access switches.
- **Default & Static Routing:** Integrated edge routing path (`0.0.0.0/0`) upstream to the edge router.

## Verification & Testing
- Validated end-to-end connectivity across subnets via ICMP ping tests.
- Verified routing table convergence with `show ip route`.
- Confirmed VLAN isolation and trunk status via `show interfaces trunk` and `show vlan brief`.

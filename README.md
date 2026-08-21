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

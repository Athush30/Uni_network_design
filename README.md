# University of Moratuwa Network Design Documentation

1. **Introduction**  
   Provides an overview of the proposed backbone network, emphasizing the use of fiber-optic cables, high-performance switches, and modern routing techniques for fast, reliable, and stable communication.

2. **Internal Network of the ENTC Building**  
   Details the LAN architecture for the Department of Electronic and Telecommunication Engineering (ENTC), including:
   - Flat LAN architecture connected to the backbone via a Layer 3 switch (ENTC node).
   - Connectivity details for Layer 2 switches, wireless access points, and laboratories.
   - Security measures for wireless access, including VLAN segmentation, WPA2-Enterprise authentication, and controlled wireless coverage.
   - Network diagrams and simulation results for the ENTC LAN.

3. **The Backbone Network for University of Moratuwa**  
   Describes the campus-wide backbone network, including:
   - **Hierarchical Network Architecture**: Core, Distribution, and Access layers for modularity and scalability.
   - **High-Speed Switching and Cabling**: Use of Layer 3 switches, fiber-optic cables, and copper UTP cables.
   - **Resilience and Redundancy**: Implementation of LACP, dual power supplies, and backup systems.
   - **Security and Traffic Segmentation**: Use of ACLs, firewalls, IDS/IPS, and VLANs.
   - **Centralized Monitoring**: SNMP-based tools for real-time network management.
   - **Core Network Architecture**: Ring topology connecting key nodes (e.g., Sumanadasa Building, CITeS, and various departments).
   - **Design Considerations and Assumptions**: High-bandwidth leased lines, Frame Relay, and centralized NOC.
   - **Network Diagrams and Simulations**: Visual representations of the backbone network (physical and logical views).
   - **OSPF in Ring Topology**: Explanation of OSPF’s compatibility with ring topology for dynamic routing and redundancy.

4. **IPv4 Addressing Scheme**  
   Provides detailed IP configurations for Layer 3 switches across various departments and buildings, including:

   ### Sumanadasa Building
   | Port                | IP Address    | Subnet Mask     |
   |---------------------|---------------|------------------|
   | GigabitEthernet1/0/1 | 10.0.112.1    | 255.255.252.0    |
   | GigabitEthernet1/0/2 | 10.0.116.1    | 255.255.252.0    |
   | GigabitEthernet1/0/3 | 10.0.120.1    | 255.255.252.0    |
   | GigabitEthernet1/0/4 | 10.0.124.1    | 255.255.252.0    |
   | GigabitEthernet1/0/5 | 10.10.130.2   | 255.255.255.0    |
   | GigabitEthernet1/1/1 | 192.168.50.1  | 255.255.255.0    |
   | GigabitEthernet1/1/3 | 192.168.60.2  | 255.255.255.0    |

   ### Mechanical Engineering Department
   | Port                | IP Address    | Subnet Mask     |
   |---------------------|---------------|------------------|
   | GigabitEthernet1/0/1 | 192.168.40.1  | 255.255.255.0    |
   | GigabitEthernet1/0/2 | 10.0.96.1     | 255.255.252.0    |
   | GigabitEthernet1/0/3 | 10.0.100.1    | 255.255.252.0    |
   | GigabitEthernet1/0/4 | 10.0.104.1    | 255.255.252.0    |
   | GigabitEthernet1/1/1 | 192.168.50.2  | 255.255.255.0    |

   ### Administration Building
   | Port                | IP Address    | Subnet Mask     |
   |---------------------|---------------|------------------|
   | GigabitEthernet1/0/1 | 192.168.40.2  | 255.255.255.0    |
   | GigabitEthernet1/0/2 | 10.0.80.1     | 255.255.252.0    |
   | GigabitEthernet1/0/3 | 10.0.84.1     | 255.255.252.0    |
   | GigabitEthernet1/0/4 | 10.0.88.1     | 255.255.252.0    |
   | GigabitEthernet1/1/1 | 192.168.30.2  | 255.255.255.0    |

   ### Library
   | Port                | IP Address    | Subnet Mask     |
   |---------------------|---------------|------------------|
   | GigabitEthernet1/0/1 | 10.0.64.1     | 255.255.252.0    |
   | GigabitEthernet1/0/2 | 10.0.68.1     | 255.255.252.0    |
   | GigabitEthernet1/0/3 | 10.0.72.1     | 255.255.252.0    |
   | GigabitEthernet1/1/1 | 192.168.30.1  | 255.255.255.0    |
   | GigabitEthernet1/1/2 | 192.168.20.2  | 255.255.255.0    |

   ### ENTC Department
   | Port                | IP Address    | Subnet Mask     |
   |---------------------|---------------|------------------|
   | GigabitEthernet1/0/1 | 10.0.16.1     | 255.255.252.0    |
   | GigabitEthernet1/0/2 | 10.0.20.1     | 255.255.252.0    |
   | GigabitEthernet1/0/3 | 10.0.24.1     | 255.255.252.0    |
   | GigabitEthernet1/1/1 | 192.168.10.2  | 255.255.255.0    |
   | GigabitEthernet1/1/2 | 192.168.20.1  | 255.255.255.0    |

   ### Network Operations Center (NOC)
   | Port                | IP Address    | Subnet Mask     |
   |---------------------|---------------|------------------|
   | GigabitEthernet1/0/1 | 10.100.0.2    | 255.255.255.0    |
   | GigabitEthernet1/1/1 | 192.168.10.1  | 255.255.255.0    |
   | GigabitEthernet1/1/2 | 192.168.100.1 | 255.255.255.0    |
   | GigabitEthernet1/1/3 | 192.168.80.1  | 255.255.255.0    |

   ### Civil Engineering Department
   | Port                | IP Address    | Subnet Mask     |
   |---------------------|---------------|------------------|
   | GigabitEthernet1/0/1 | 10.0.48.1     | 255.255.252.0    |
   | GigabitEthernet1/0/2 | 10.0.52.1     | 255.255.252.0    |
   | GigabitEthernet1/0/3 | 10.0.56.1     | 255.255.252.0    |
   | GigabitEthernet1/1/1 | 192.168.90.1  | 255.255.255.0    |
   | GigabitEthernet1/1/2 | 192.168.80.2  | 255.255.255.0    |

   ### Textile Engineering Department
   | Port                | IP Address    | Subnet Mask     |
   |---------------------|---------------|------------------|
   | GigabitEthernet1/0/1 | 192.168.70.1  | 255.255.255.0    |
   | GigabitEthernet1/0/2 | 10.0.128.1    | 255.255.252.0    |
   | GigabitEthernet1/0/3 | 10.0.132.1    | 255.255.252.0    |
   | GigabitEthernet1/0/4 | 10.0.136.1    | 255.255.252.0    |
   | GigabitEthernet1/1/1 | 192.168.90.2  | 255.255.255.0    |

   ### Faculty of IT
   | Port                | IP Address    | Subnet Mask     |
   |---------------------|---------------|------------------|
   | GigabitEthernet1/0/1 | 192.168.70.2  | 255.255.255.0    |
   | GigabitEthernet1/0/2 | 10.0.32.1     | 255.255.252.0    |
   | GigabitEthernet1/0/3 | 10.0.36.1     | 255.255.252.0    |
   | GigabitEthernet1/0/4 | 10.0.40.1     | 255.255.252.0    |
   | GigabitEthernet1/1/1 | 192.168.100.2 | 255.255.255.0    |
   | GigabitEthernet1/1/2 | 192.168.60.1  | 255.255.255.0    |

5. **Justification for Backbone**  
   Explains the preference for active routers and Layer 3 switches over traditional routers, highlighting their performance, scalability, and cost-effectiveness. It also details the selection of single-mode and multi-mode fiber-optic cables for different network segments.

## Key Features
- **Scalable and Hierarchical Design**: Ensures modularity, fault isolation, and future expansion.
- **High-Performance Infrastructure**: Utilizes fiber-optic cables, Layer 3 switches, and dynamic routing protocols (OSPF, EIGRP).
- **Robust Security**: Implements VLAN segmentation, WPA2-Enterprise, ACLs, firewalls, and IDS/IPS.
- **Redundancy and Reliability**: Features ring topology, LACP, and dual power supplies for minimal downtime.
- **Centralized Management**: Employs SNMP for real-time monitoring and fault detection.
- **Validated Design**: Includes simulations and logical validations for both ENTC LAN and backbone network.

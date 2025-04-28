# Cisco and MikroTik Dynamic Routing
This simulation uses Cisco and MikroTik network devices to configure dynamic routing. In contrast to static routing configurations ([Cisco](https://github.com/eightball270/CodingStudio-ComputerNetworkFundamentals?tab=readme-ov-file#static-routing) and [MikroTik](https://github.com/eightball270/MikroTik-Static-Routing/tree/main?tab=readme-ov-file#mikrotik-static-routing)) where routing tables are created manually, dynamic routing requires only the addition of directly connected network addresses on each router. The configured dynamic routing protocol then automatically generates the routing tables. The dynamic routing protocols used in this simulation are RIP and OSPF.

RIP (Routing Information Protocol) is a dynamic routing protocol that uses a distance-vector algorithm to determine the best path in a computer network. In contrast, OSPF (Open Shortest Path First) is a dynamic routing protocol that uses a link-state algorithm to determine the optimal path in an IP network. The key difference between the two is that RIP has a simpler configuration but is limited to a maximum of 15 hops and experiences slow convergence, making it suitable for small-scale networks. OSPF, on the other hand, has a more complex configuration but offers faster convergence and no hop count limitation, making it ideal for large-scale networks.

## Technology Used
1. Cisco Packet Tracer
2. GNS3 (MikroTik)

## Requirements
1. 3 Routers and Switches (divided 2 VLANs)
2. 12 Client PCs
3. Straight-Through Cables
4. Crossover Cables (for inter-router connection)

## Configuration Completed
1. VLANs on routers and switches
2. The IP address on the router is used as the gateway for each client PC and for the inter-router network
3. Static IP address of each client PCs
4. RIP routing using version 2 (RIPv2) via command-line
5. Port forwarding on the router to remote via Winbox (MikroTik)
6. OSPF routing configuration via command-line (Cisco) and Winbox (MikroTik)

## RIP (Routing Information Protocol)
This configuration uses RIP version 2 (RIPv2), as it supports subnetting through Variable Length Subnet Masking (VLSM).

### Cisco

![RIP Routing.png](https://github.com/eightball270/Cisco-and-MikroTik-Dynamic-Routing/blob/main/Cisco/RIP%20Routing.png)

[Project File Link (Packet Tracer)](https://github.com/eightball270/Cisco-and-MikroTik-Dynamic-Routing/blob/main/Cisco/RIP%20Routing.pkt)

Traceroute from PC0 (192.168.1.2/25) to PC5 (192.168.2.3/25) and PC10 (192.168.3.130/25) :

![RIP Routing (1).png](https://github.com/eightball270/Cisco-and-MikroTik-Dynamic-Routing/blob/main/Cisco/RIP%20Routing%20(1).png) ![RIP Routing (2).png](https://github.com/eightball270/Cisco-and-MikroTik-Dynamic-Routing/blob/main/Cisco/RIP%20Routing%20(2).png) ![RIP Routing (3).png](https://github.com/eightball270/Cisco-and-MikroTik-Dynamic-Routing/blob/main/Cisco/RIP%20Routing%20(3).png)

### MikroTik

![RIP Routing (MikroTik).png)](https://github.com/eightball270/Cisco-and-MikroTik-Dynamic-Routing/blob/main/MikroTik/RIP%20Routing%20(MikroTik).png)

[Project File Link (GNS3)](https://github.com/eightball270/Cisco-and-MikroTik-Dynamic-Routing/blob/main/MikroTik/RIP%20Routing%20(MikroTik).gns3project.rar) (extract the file first)

Traceroute from PC3 (192.168.10.130/25) to PC6 (192.168.20.3/25) and PC11 (192.168.3.130/25) :

![RIP Routing (MikroTik) (1).png](https://github.com/eightball270/Cisco-and-MikroTik-Dynamic-Routing/blob/main/MikroTik/RIP%20Routing%20(MikroTik)%20(1).png)

## OSPF (Open Shortest Path First)
OSPF configuration on Cisco is similar to RIP, but it is necessary to specify the process ID (Cisco) or router ID (MikroTik) along with the area ID.

### Cisco

![OSPF Routing.png](https://github.com/eightball270/Cisco-and-MikroTik-Dynamic-Routing/blob/main/Cisco/OSPF%20Routing.png)

[Project File Link (Packet Tracer)](https://github.com/eightball270/Cisco-and-MikroTik-Dynamic-Routing/blob/main/Cisco/OSPF%20Routing.pkt)

Traceroute from PC10 (192.168.3.130/25) to PC4 (192.168.2.2/25) and PC3 (192.168.1.131/25) :

![OSPF Routing (1).png](https://github.com/eightball270/Cisco-and-MikroTik-Dynamic-Routing/blob/main/Cisco/OSPF%20Routing%20(1).png) ![OSPF Routing (2).png](https://github.com/eightball270/Cisco-and-MikroTik-Dynamic-Routing/blob/main/Cisco/OSPF%20Routing%20(2).png) ![OSPF Routing (3).png](https://github.com/eightball270/Cisco-and-MikroTik-Dynamic-Routing/blob/main/Cisco/OSPF%20Routing%20(3).png)

### MikroTik

![OSPF Routing (Mikrotik).png](https://github.com/eightball270/Cisco-and-MikroTik-Dynamic-Routing/blob/main/MikroTik/OSPF%20Routing%20(Mikrotik).png)

[Project File Link (GNS3)](https://github.com/eightball270/Cisco-and-MikroTik-Dynamic-Routing/blob/main/MikroTik/OSPF%20Routing%20(MikroTik).gns3project.rar) (extract the file first)

Traceroute from PC9 (192.168.30.2/25) to PC8 (192.168.20.131/25) and PC2 (192.168.10.3/25) :

![OSPF Routing (Mikrotik) (1).png](https://github.com/eightball270/Cisco-and-MikroTik-Dynamic-Routing/blob/main/MikroTik/OSPF%20Routing%20(Mikrotik)%20(1).png)

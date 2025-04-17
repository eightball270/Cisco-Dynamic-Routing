# Cisco and MikroTik Dynamic Routingg
This simulation uses Cisco and Mikrotik network devices to configure dynamic routing, in contrast to static routing configurations ([Cisco](https://github.com/eightball270/CodingStudio-ComputerNetworkFundamentals?tab=readme-ov-file#static-routing) and [MikroTik](https://github.com/eightball270/MikroTik-Static-Routing/tree/main?tab=readme-ov-file#mikrotik-static-routing)) which create routing tables manually, in dynamic routing configurations only add network addresses that are directly connected to each router, then the configured dynamic routing protocol makes the router will create routing tables automatically. The dynamic routing protocols used in this simulation are RIP and OSPF.

RIP (Routing Information Protocol) is a dynamic routing protocol that uses a distance-vector algorithm to determine the best path in a computer network. While OSPF (Open Shortest Path First) is a dynamic routing protocol that uses a link-state algorithm to determine the best path in an IP network. The difference between the two is that the RIP protocol has a simple configuration but has a maximum hop count limitation of 15 hops and slow convergence making it suitable for small-scale networks, while the OSPF protocol has a more complex configuration but has no hop count limitation and fast convergence making it suitable for large-scale networks.

## Technology Used
1. Cisco Packet Tracer
2. GNS3 (MikroTik)

## Requirements
1. 3 Routers and Switches (divided 2 VLANs)
2. 12 Client PCs
3. Straight-Through Cables
4. Crossover Cables (for inter-router connection)

## Configuration Completed
1. VLAN on routers and switches
2. IP address on the router which is used as the gateway for each client PCs and inter-router network
3. Static IP address of each client PCs
4. RIP routing using version 2 (RIPv2) via command-line
5. Port forwarding on the router to remote via Winbox (MikroTik)
6. OSPF routing configuration via command-line (Cisco) and Winbox (MikroTik)

## RIP (Routing Information Protocol)
This configuration uses RIP version 2 (RIPv2) because this version supports subnetting (VLSM).

### Cisco

![RIP Routing](https://github.com/eightball270/Cisco-and-MikroTik-Dynamic-Routing/blob/main/Cisco/RIP%20Routing.png)

[Project File Link](https://github.com/eightball270/Cisco-and-MikroTik-Dynamic-Routing/blob/main/Cisco/RIP%20Routing.pkt)

Traceroute from PC0 (192.168.1.2/25) to PC5 (192.168.2.3/25) and PC10 (192.168.3.130/25) :

![RIP Routing (1)](https://github.com/eightball270/Cisco-and-MikroTik-Dynamic-Routing/blob/main/Cisco/RIP%20Routing%20(1).png) ![RIP Routing (2)](https://github.com/eightball270/Cisco-and-MikroTik-Dynamic-Routing/blob/main/Cisco/RIP%20Routing%20(2).png) ![RIP Routing (3)](https://github.com/eightball270/Cisco-and-MikroTik-Dynamic-Routing/blob/main/Cisco/RIP%20Routing%20(3).png)

### MikroTik

![RIP Routing (MikroTik)](https://github.com/eightball270/Cisco-and-MikroTik-Dynamic-Routing/blob/main/MikroTik/RIP%20Routing%20(MikroTik).png)

[Project File Link](https://github.com/eightball270/Cisco-and-MikroTik-Dynamic-Routing/blob/main/MikroTik/RIP%20Routing%20(MikroTik).gns3project.7z)

Traceroute from PC3 (192.168.10.130/25) to PC6 (192.168.20.3/25) and PC11 (192.168.3.130/25) :

![RIP Routing (MikroTik) (1)](https://github.com/eightball270/Cisco-and-MikroTik-Dynamic-Routing/blob/main/MikroTik/RIP%20Routing%20(MikroTik)%20(1).png)

## OSPF (Open Shortest Path First)
OSPF configuration on Cisco is almost the same as RIP, but must specify the process ID (Cisco)/router ID (MikroTik) with the area ID.

### Cisco

![OSPF Routing](https://github.com/eightball270/Cisco-and-MikroTik-Dynamic-Routing/blob/main/Cisco/OSPF%20Routing.png)

[Project File Link](https://github.com/eightball270/Cisco-and-MikroTik-Dynamic-Routing/blob/main/Cisco/OSPF%20Routing.pkt)

Traceroute from PC10 (192.168.3.130/25) to PC4 (192.168.2.2/25) and PC3 (192.168.1.131/25) :

![OSPF Routing (1)](https://github.com/eightball270/Cisco-and-MikroTik-Dynamic-Routing/blob/main/Cisco/OSPF%20Routing%20(1).png) ![OSPF Routing (2)](https://github.com/eightball270/Cisco-and-MikroTik-Dynamic-Routing/blob/main/Cisco/OSPF%20Routing%20(2).png) ![OSPF Routing (3)](https://github.com/eightball270/Cisco-and-MikroTik-Dynamic-Routing/blob/main/Cisco/OSPF%20Routing%20(3).png)

### MikroTik

![OSPF Routing (Mikrotik)](https://github.com/eightball270/Cisco-and-MikroTik-Dynamic-Routing/blob/main/MikroTik/OSPF%20Routing%20(Mikrotik).png)

[Project File Link](https://github.com/eightball270/Cisco-and-MikroTik-Dynamic-Routing/blob/main/MikroTik/OSPF%20Routing%20(MikroTik).gns3project.7z)

Traceroute from PC9 (192.168.30.2/25) to PC8 (192.168.20.131/25) and PC2 (192.168.10.3/25) :

![OSPF Routing (Mikrotik) (1)](https://github.com/eightball270/Cisco-and-MikroTik-Dynamic-Routing/blob/main/MikroTik/OSPF%20Routing%20(Mikrotik)%20(1).png)

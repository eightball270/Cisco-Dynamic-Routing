# Cisco-and-MikroTik-Dynamic-Routing
This project uses Cisco and Mikrotik network devices to configure dynamic routing such as RIP and OSPF. RIP (Routing Information Protocol) is a dynamic routing protocol that uses a distance-vector algorithm to determine the best path in a computer network. While OSPF (Open Shortest Path First) is a dynamic routing protocol that uses a link-state algorithm to determine the best path in an IP network. The difference between the two is that the RIP protocol has a simple configuration but has a maximum hop count limitation of 15 hops and slow convergence making it suitable for small-scale networks, while the OSPF protocol has a more complex configuration but has no hop count limitation and fast convergence making it suitable for large-scale networks.

## Technology Used
1. Cisco Packet Tracer v8.2.2
2. GNS3 (MikroTik)

## Equipment
1. 3 Routers and Switches (divided 2 VLANs)
2. 12 Client PCs
3. Straight-Through Cables
4. Crossover Cables (for Inter-Router network)

## Configuration Completed
1. VLAN on routers and switches
2. IP address on the router which is used as the gateway for each client PCs and inter-router network
3. Static IP address of each client PCs
4. RIP routing using version 2 (RIPv2) via command-line
5. Port forwarding on the router to remote via Winbox (MikroTik)
6. OSPF routing configuration via command-line (Cisco) and Winbox (MikroTik)

## RIP (Routing Information Protocol)
This configuration uses RIP version 2 (RIPv2) because this version supports subnetting (VLSM).

Cisco :

![RIP Routing](https://github.com/user-attachments/assets/25923fc7-0c58-4954-8604-7a7c82b84746)

Traceroute PC0 (192.168.1.2) to PC5 (192.168.2.3) and PC10 (192.168.3.130) :

![RIP Routing (1)](https://github.com/user-attachments/assets/a5e8960c-c9d3-47d7-a189-7b495a05a5ed) ![RIP Routing (2)](https://github.com/user-attachments/assets/db2f9e15-e554-4d09-ba97-a8750d1bc49b) ![RIP Routing (3)](https://github.com/user-attachments/assets/1a304b05-6244-4d06-b42e-e16b2fff00f6)

## OSPF (Open Shortest Path First)
OSPF configuration on Cisco is almost the same as RIP, but must specify the process ID (Cisco)/router ID (MikroTik) with the area ID.

![OSPF Routing](https://github.com/user-attachments/assets/c73a7e96-14d3-4592-a229-6f71c17ff5a1)


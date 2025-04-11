# Cisco-and-MikroTik-Dynamic-Routing
This project uses Cisco and Mikrotik network devices to configure dynamic routing, in contrast to static routing configurations ([Cisco](https://github.com/eightball270/CodingStudio-ComputerNetworkFundamentals?tab=readme-ov-file#static-routing) and [MikroTik](https://github.com/eightball270/MikroTik-Static-Routing/tree/main?tab=readme-ov-file#mikrotik-static-routing)) which create routing tables manually, in dynamic routing configurations only add network addresses that are directly connected to each router, then the configured dynamic routing protocol will create routing tables automatically. The dynamic routing protocols used in this project are RIP and OSPF. RIP (Routing Information Protocol) is a dynamic routing protocol that uses a distance-vector algorithm to determine the best path in a computer network. While OSPF (Open Shortest Path First) is a dynamic routing protocol that uses a link-state algorithm to determine the best path in an IP network. The difference between the two is that the RIP protocol has a simple configuration but has a maximum hop count limitation of 15 hops and slow convergence making it suitable for small-scale networks, while the OSPF protocol has a more complex configuration but has no hop count limitation and fast convergence making it suitable for large-scale networks.

## Technology Used
1. Cisco Packet Tracer v8.2.2
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

![RIP Routing](https://github.com/user-attachments/assets/25923fc7-0c58-4954-8604-7a7c82b84746)

Traceroute from PC0 (192.168.1.2/25) to PC5 (192.168.2.3/25) and PC10 (192.168.3.130/25) :

![RIP Routing (1)](https://github.com/user-attachments/assets/a5e8960c-c9d3-47d7-a189-7b495a05a5ed) ![RIP Routing (2)](https://github.com/user-attachments/assets/db2f9e15-e554-4d09-ba97-a8750d1bc49b) ![RIP Routing (3)](https://github.com/user-attachments/assets/1a304b05-6244-4d06-b42e-e16b2fff00f6)

### MikroTik

![RIP Routing (MikroTik)](https://github.com/user-attachments/assets/e355384a-1859-4f10-9cd9-c374cdf120b2)

Traceroute from PC3 (192.168.10.130/25) to PC6 (192.168.20.3/25) and PC11 (192.168.3.130/25) :

![RIP Routing (MikroTik) (1)](https://github.com/user-attachments/assets/e1d97fd3-d413-4f10-b106-a528dbbd15f2)

## OSPF (Open Shortest Path First)
OSPF configuration on Cisco is almost the same as RIP, but must specify the process ID (Cisco)/router ID (MikroTik) with the area ID.

### Cisco

![OSPF Routing](https://github.com/user-attachments/assets/c73a7e96-14d3-4592-a229-6f71c17ff5a1)

Traceroute from PC10 (192.168.3.130/25) to PC4 (192.168.2.2/25) and PC3 (192.168.1.131/25) :

![OSPF Routing (1)](https://github.com/user-attachments/assets/40317555-c388-4657-9867-62e4b12e2689) ![OSPF Routing (2)](https://github.com/user-attachments/assets/47d2299c-2090-4642-97a8-91bbc14eb479) ![OSPF Routing (3)](https://github.com/user-attachments/assets/f64e46dd-6088-4e0b-8ff5-19a0d6d0b3fc)

### MikroTik

![OSPF Routing (Mikrotik)](https://github.com/user-attachments/assets/6fa2ce52-41a9-4cc5-9d71-3c56e2655a4d)

Traceroute from PC9 (192.168.30.2/25) to PC8 (192.168.20.131/25) and PC2 (192.168.10.3/25) :

![OSPF Routing (Mikrotik) (1)](https://github.com/user-attachments/assets/afc495d9-8fad-4167-8f17-4109146c899d)

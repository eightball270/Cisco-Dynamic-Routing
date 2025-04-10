# Cisco-and-MikroTik-Dynamic-Routing
This project describes the configuration of dynamic routing, using 2 protocols which are RIP and OSPF. RIP (Routing Information Protocol) is a dynamic routing protocol that uses a distance-vector algorithm to determine the best path in a computer network. While OSPF (Open Shortest Path First) is a dynamic routing protocol that uses a link-state algorithm to determine the best path in an IP network. The difference between the two is that the RIP protocol has a simple configuration but has a maximum hop count limitation of 15 hops and slow convergence making it suitable for small-scale networks, while the OSPF protocol has a more complex configuration but has no hop count limitation and fast convergence making it suitable for large-scale networks.

## Objectives
1. understand the configuration of RIPv2 routing protocol
2. understand the configuration of OSPF routing protocol

## Equipment
1. 3 Routers and Switches (divided 2 VLANs)
2. 12 PC Clients

## RIP (Routing Information Protocol)
This configuration uses RIP version 2 (RIPv2) because this version supports subnetting (VLSM).

![RIP Routing](https://github.com/user-attachments/assets/689d8edb-d087-406d-abae-d8be4bdf7d92)

## OSPF (Open Shortest Path First)
OSPF configuration on Cisco is almost the same as RIP, but must specify the router ID with the area ID.

![OSPF Routing](https://github.com/user-attachments/assets/47b382b1-4ffb-4f58-b75c-d70558a95a8f)

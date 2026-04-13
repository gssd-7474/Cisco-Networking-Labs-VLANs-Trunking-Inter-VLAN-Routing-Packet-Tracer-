# Week 7 Lab – Inter-VLAN Routing (Router-on-a-Stick)

## 📌 Overview
This lab demonstrates inter-VLAN communication using a Router-on-a-Stick architecture. It involves configuring VLANs, trunking, and router subinterfaces to enable communication between different network segments.

:contentReference[oaicite:0]{index=0}

---

## 🧩 Lab Objectives
- Create VLANs and assign switch ports  
- Configure 802.1Q trunking between switches and router  
- Implement inter-VLAN routing using subinterfaces  
- Enable IPv4 and IPv6 communication  
- Verify connectivity between VLANs  

---

## 🌐 Network Topology
Devices used:
- 2 PCs (PC-A, PC-B)  
- 2 Switches (S1, S2)  
- 1 Router (R1)  

---

## 🔢 IP Addressing

### 🔹 Router Subinterfaces
| Interface     | VLAN | IPv4 Address     |
|--------------|------|------------------|
| G0/1.10      | 10   | 192.168.10.1     |
| G0/1.20      | 20   | 192.168.20.1     |
| G0/1.30      | 30   | 192.168.30.1     |

### 🔹 Hosts
| Device | IP Address     | VLAN |
|--------|---------------|------|
| PC-A   | 192.168.20.3  | 20   |
| PC-B   | 192.168.30.3  | 30   |

---

## ⚙️ Key Configurations

### 🔹 VLAN Configuration
- Created VLANs:
  - VLAN 10 → Management  
  - VLAN 20 → Sales  
  - VLAN 30 → Operations  
  - VLAN 999 → Parking Lot  
  - VLAN 1000 → Native  

- Assigned switch ports to appropriate VLANs  
- Disabled unused ports for security  

---

### 🔹 Trunking (802.1Q)
- Configured trunk links:
  - Between switches  
  - Between switch and router  
- Allowed VLANs:
  - 10, 20, 30, 1000  
- Set native VLAN to 1000  

---

### 🔹 Inter-VLAN Routing (Router-on-a-Stick)
- Configured router subinterfaces:
  - `G0/1.10` → VLAN 10  
  - `G0/1.20` → VLAN 20  
  - `G0/1.30` → VLAN 30  

- Applied:
  - `encapsulation dot1Q`  
  - IP addressing per VLAN  
- Enabled router interface with `no shutdown`  

---

### 🔹 IPv6 Configuration
- Configured IPv6 addressing on router subinterfaces  
- Enabled IPv6 routing  

---

## 🧪 Verification
- Verified trunk configuration:
  - `show interfaces trunk`  
- Verified interfaces:
  - `show ip interface brief`  
- Tested connectivity:
  - PC-A → Default Gateway  
  - PC-A → PC-B (inter-VLAN communication)  
  - PC-A → Switch (management VLAN)  

---

## 🛠 Tools Used
- Cisco Packet Tracer (v8.2.2+)  
- Cisco IOS CLI  

---

## 🎯 Learning Outcome
This lab helped me understand:
- Inter-VLAN communication using Layer 3 routing  
- Router-on-a-Stick architecture  
- VLAN segmentation and routing integration  
- 802.1Q trunking in real networks  
- Dual-stack (IPv4 + IPv6) configuration  

---

## 🚀 Key Takeaway
This lab demonstrates how multiple VLANs can communicate through a single router interface using subinterfaces, which is a common design used in small to medium enterprise networks.

# Week 5 Lab – Rapid PVST+, PortFast and BPDU Guard

## 📌 Overview
This lab focuses on configuring Spanning Tree Protocol (STP) and its enhanced version Rapid PVST+ to ensure loop-free Layer 2 network operation. It also includes implementing PortFast and BPDU Guard for improved performance and security.

---

## 🧩 Lab Objectives
- Configure VLANs, native VLAN, and trunk links  
- Configure root bridge selection for spanning tree  
- Analyze PVST+ convergence behavior  
- Configure Rapid PVST+ for faster convergence  
- Implement PortFast and BPDU Guard for edge port optimization and security  

---

## 🌐 Network Topology
Devices used:
- 2 PCs (PC-A, PC-C)  
- 3 Switches (S1, S2, S3)  

---

## 🔢 IP Addressing

| Device | Interface | IP Address     | Subnet Mask       |
|--------|----------|---------------|-------------------|
| S1     | VLAN 99  | 192.168.1.11  | 255.255.255.0     |
| S2     | VLAN 99  | 192.168.1.12  | 255.255.255.0     |
| S3     | VLAN 99  | 192.168.1.13  | 255.255.255.0     |
| PC-A   | NIC      | 192.168.0.2   | 255.255.255.0     |
| PC-C   | NIC      | 192.168.0.3   | 255.255.255.0     |

---

## ⚙️ Key Configurations

### 🔹 VLAN & Trunking
- Created VLANs:
  - VLAN 10 → User  
  - VLAN 99 → Management  
  - VLAN 1000 → Native  
- Configured trunk ports between switches  
- Allowed VLANs across trunk links  

---

### 🔹 Spanning Tree Configuration (PVST+)
- Verified default STP mode (PVST+)  
- Identified root bridge in the network  
- Configured:
  - Primary root bridge  
  - Secondary root bridge  
- Observed STP port states:
  - Blocking  
  - Listening  
  - Learning  
  - Forwarding  

---

### 🔹 Rapid PVST+ (RSTP)
- Enabled **Rapid PVST+** for faster convergence  
- Compared convergence time with standard PVST+  
- Observed improved network recovery after topology changes  

---

### 🔹 PortFast Configuration
- Enabled PortFast on access ports  
- Allowed immediate transition to forwarding state  
- Reduced delay for end devices  

---

### 🔹 BPDU Guard
- Enabled BPDU Guard on edge ports  
- Automatically disables port if BPDU is received  
- Protects network from unintended topology changes  

---

## 🧪 Verification
- Verified VLAN and trunk configurations  
- Used:
  - `show vlan brief`  
  - `show interfaces trunk`  
  - `show spanning-tree`  
- Tested connectivity between hosts  
- Observed STP convergence behavior during topology changes  

---

## 🛠 Tools Used
- Cisco Packet Tracer (v8.2.2)  
- Cisco IOS CLI  

---

## 🎯 Learning Outcome
This lab helped me understand:
- Spanning Tree Protocol (STP) fundamentals  
- Rapid PVST+ for faster convergence  
- Root bridge selection and network optimization  
- Layer 2 loop prevention mechanisms  
- Network security using BPDU Guard  
- Performance improvement using PortFast  

# Week 4 Lab – VLANs and Trunking Configuration

## 📌 Overview
This lab focuses on configuring Virtual Local Area Networks (VLANs) and implementing trunking between switches using Cisco Packet Tracer. It demonstrates how to segment a network and allow communication across switches using 802.1Q trunking.

---

## 🧩 Lab Objectives
- Build the network topology and configure basic device settings  
- Create VLANs and assign switch ports  
- Maintain VLAN database and port assignments  
- Configure 802.1Q trunking between switches  
- Verify VLAN communication across switches  

---

## 🌐 Network Topology
Devices used:
- 2 PCs (PC-A, PC-B)  
- 2 Switches (S1, S2)  

---

## 🔢 IP Addressing

| Device | Interface | IP Address     | Subnet Mask       | Default Gateway |
|--------|----------|---------------|-------------------|-----------------|
| S1     | VLAN 1   | 192.168.1.11  | 255.255.255.0     | N/A             |
| S2     | VLAN 1   | 192.168.1.12  | 255.255.255.0     | N/A             |
| PC-A   | NIC      | 192.168.10.3  | 255.255.255.0     | 192.168.10.1    |
| PC-B   | NIC      | 192.168.10.4  | 255.255.255.0     | 192.168.10.1    |

---

## ⚙️ Key Configurations

### 🔹 VLAN Configuration
- Created VLANs on both switches  
- Assigned switch ports to appropriate VLANs  
- Verified VLAN configuration using CLI commands  

### 🔹 Port Assignment
- Configured access ports for end devices  
- Ensured correct VLAN membership for each port  

### 🔹 Trunk Configuration
- Configured **802.1Q trunking** between switches  
- Allowed multiple VLANs to pass through a single link  
- Verified trunk status using:
  - `show interfaces trunk`  

---

## 🧪 Verification
- Tested connectivity between devices in the same VLAN  
- Verified VLAN segmentation  
- Confirmed trunk link operation between switches  

---

## 🛠 Tools Used
- Cisco Packet Tracer (v8.2.2)  
- Cisco IOS CLI  

---

## 🎯 Learning Outcome
This lab helped me understand:
- VLAN segmentation and network design  
- 802.1Q trunking between switches  
- Broadcast domain separation  
- Basic Layer 2 network security concepts  

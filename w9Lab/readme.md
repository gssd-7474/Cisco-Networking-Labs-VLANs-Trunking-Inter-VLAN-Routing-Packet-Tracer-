# Week 9 Lab – VLSM Network Design and Implementation

## 📌 Overview
This lab focuses on designing and implementing a Variable Length Subnet Mask (VLSM) addressing scheme to efficiently allocate IP addresses based on network requirements.

:contentReference[oaicite:0]{index=0}

---

## 🧩 Lab Objectives
- Analyze network requirements  
- Design a VLSM-based IP addressing scheme  
- Configure routers, switches, and PCs  
- Implement serial connections between routers  
- Test and troubleshoot network connectivity  

---

## 🌐 Network Topology
Devices used:
- Multiple routers (HQ, BR1, BR2)  
- Multiple PCs (PC-A to PC-F)  
- Switches connecting LAN segments  

---

## 🔢 Network Design

### 🔹 Base Network
- **172.16.128.0/17**

### 🔹 Key Requirement
- Allocate subnets based on different host needs:
  - 16,000 hosts  
  - 8,000 hosts  
  - 4,000 hosts  
  - 2,000 hosts  
  - 1,000 hosts  
  - 500 hosts  
  - Serial links (2 hosts each)  

---

## ⚙️ Key Concepts Implemented

### 🔹 VLSM (Variable Length Subnet Masking)
- Subnetted network based on **actual host requirements**  
- Allocated larger subnets first  
- Minimized IP address wastage  

---

### 🔹 Router Configuration
- Configured multiple routers:
  - HQ  
  - BR1  
  - BR2  

- Configured:
  - Gigabit Ethernet interfaces  
  - Serial interfaces (DCE/DTE)  
- Assigned IP addresses based on VLSM design  
- Enabled interfaces using `no shutdown`  

---

### 🔹 Serial Communication
- Installed serial modules (HWIC-2T)  
- Configured DCE and DTE connections  
- Verified interface status  

---

### 🔹 PC Configuration
- Assigned IP addresses using VLSM scheme  
- Configured default gateways  

---

## 🧪 Verification & Testing
- Tested connectivity within directly connected networks  
- Verified router interfaces using:
  - `show ip interface brief`  
- Observed routing limitations (no dynamic/static routing configured)  
- Performed troubleshooting for addressing issues  

---

## 🛠 Tools Used
- Cisco Packet Tracer (v8.2.2)  
- Cisco IOS CLI  

---

## 🎯 Learning Outcome
This lab helped me understand:
- VLSM and efficient IP address allocation  
- Network design based on varying host requirements  
- Multi-router network configuration  
- Serial communication between routers  
- Real-world IP planning strategies  

---

## 🚀 Key Takeaway
This lab demonstrates the ability to design scalable and efficient networks using VLSM, a critical skill in real-world networking environments where IP address optimization is essential.

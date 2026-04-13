# Week 6 Lab – EtherChannel (PAgP & LACP)

## 📌 Overview
This lab focuses on configuring EtherChannel (link aggregation) to combine multiple physical links into a single logical connection. It includes configuration using both Cisco proprietary PAgP and industry-standard LACP protocols.

:contentReference[oaicite:0]{index=0}

---

## 🧩 Lab Objectives
- Configure VLANs and assign switch ports  
- Configure EtherChannel using PAgP  
- Configure EtherChannel using LACP  
- Configure trunking over EtherChannel links  
- Verify connectivity and redundancy  

---

## 🌐 Network Topology
Devices used:
- 3 PCs (PC-A, PC-B, PC-C)  
- 3 Switches (S1, S2, S3)  

---

## 🔢 IP Addressing

| Device | Interface | IP Address     | Subnet Mask       |
|--------|----------|---------------|-------------------|
| S1     | VLAN 99  | 192.168.99.11 | 255.255.255.0     |
| S2     | VLAN 99  | 192.168.99.12 | 255.255.255.0     |
| S3     | VLAN 99  | 192.168.99.13 | 255.255.255.0     |
| PC-A   | NIC      | 192.168.10.1  | 255.255.255.0     |
| PC-B   | NIC      | 192.168.10.2  | 255.255.255.0     |
| PC-C   | NIC      | 192.168.10.3  | 255.255.255.0     |

---

## ⚙️ Key Configurations

### 🔹 VLAN & Port Configuration
- Created VLANs:
  - VLAN 10 → Staff  
  - VLAN 99 → Management  
  - VLAN 555 → Parking Lot  
  - VLAN 1000 → Native  
- Assigned ports to VLANs  
- Disabled unused ports for security  

---

### 🔹 EtherChannel using PAgP
- Configured EtherChannel between **S1 and S3**  
- Used:
  - `mode desirable` (active negotiation)  
  - `mode auto` (passive)  
- Created Port-Channel interface (Po1)  

---

### 🔹 EtherChannel using LACP
- Configured EtherChannel between:
  - S1 ↔ S2 (Po2)  
  - S2 ↔ S3 (Po3)  
- Used:
  - `active` mode  
  - `passive` mode  
- Implemented IEEE 802.3ad standard  

---

### 🔹 Trunking over EtherChannel
- Configured trunking on Port-Channel interfaces  
- Allowed VLANs:
  - 10, 99, 1000  
- Set native VLAN to 1000  

---

## 🧪 Verification
- Verified EtherChannel formation using:
  - `show etherchannel summary`  
- Verified trunk configuration:
  - `show interfaces trunk`  
- Tested end-to-end connectivity between PCs  
- Verified redundancy and link aggregation  

---

## 🛠 Tools Used
- Cisco Packet Tracer (v8.2.2+)  
- Cisco IOS CLI  

---

## 🎯 Learning Outcome
This lab helped me understand:
- Link aggregation and redundancy concepts  
- EtherChannel configuration (PAgP & LACP)  
- Load balancing across multiple links  
- High availability in network design  
- Differences between Cisco proprietary and standard protocols  

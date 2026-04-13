# Week 3 Lab – Configuring a Small Network with SVI and SSH

## 📌 Overview
This lab focuses on configuring a small multi-switch network using Cisco Packet Tracer. It includes basic device configuration, IP addressing, and implementing secure remote access using SSH.

---

## 🧩 Lab Objectives
- Configure basic network devices (PCs and switches)  
- Assign IP addresses to hosts and switches  
- Configure Switch Virtual Interfaces (SVIs) for management  
- Enable secure remote access using SSH  
- Verify and test network connectivity  

---

## 🌐 Network Topology
Devices used:
- 3 PCs (PC-A, PC-B, PC-C)  
- 3 Switches (S1, S2, S3)  

---

## 🔢 IP Addressing

| Device | Interface | IP Address     | Subnet Mask       |
|--------|----------|---------------|-------------------|
| PC-A   | NIC      | 192.168.1.33  | 255.255.255.0     |
| PC-B   | NIC      | 192.168.1.65  | 255.255.255.0     |
| PC-C   | NIC      | 192.168.1.97  | 255.255.255.0     |
| S1     | VLAN 1   | 192.168.1.1   | 255.255.255.0     |
| S2     | VLAN 1   | 192.168.1.2   | 255.255.255.0     |
| S3     | VLAN 1   | 192.168.1.3   | 255.255.255.0     |

---

## ⚙️ Key Configurations

### 🔹 PC Configuration
- Assigned static IP addresses to all PCs  
- Verified connectivity between hosts  

### 🔹 Switch Configuration
- Configured basic switch settings (hostname, passwords, etc.)  
- Configured **Switch Virtual Interface (SVI)** for management access  
- Assigned management IP addresses to each switch  

### 🔹 Remote Access Configuration
- Enabled **SSH (Secure Shell)** for remote management  
- Configured:
  - RSA keys  
  - Local user authentication  
  - VTY line access  
- Disabled insecure Telnet access  

---

## 🧪 Verification
- Tested connectivity between PCs using ping  
- Verified switch management IP reachability  
- Confirmed successful SSH login to switches  

---

## 🛠 Tools Used
- Cisco Packet Tracer (v8.2.2)  
- Cisco IOS CLI  

---

## 🎯 Learning Outcome
This lab helped me understand:
- Switch Virtual Interface (SVI) for management  
- Secure remote access using SSH  
- Multi-device network configuration  
- Basic network troubleshooting and verification  

# Week 8 Lab – Subnetting and IPv4 Network Design

## 📌 Overview
This lab focuses on designing and implementing a subnetted IPv4 addressing scheme based on network requirements. It includes subnet calculation, IP allocation, and configuring devices to achieve full connectivity.

:contentReference[oaicite:0]{index=0}

---

## 🧩 Lab Objectives
- Design a subnetting scheme from a given network  
- Allocate IP addresses based on host requirements  
- Configure router, switch, and PC devices  
- Implement loopback interfaces to simulate additional networks  
- Test and troubleshoot network connectivity  

---

## 🌐 Network Design
Base network:
- **192.168.0.0/24**

Requirements:
- Employee network (≥ 25 hosts)  
- Administration network (≥ 10 hosts)  
- 2 loopback networks (simulated LANs)  
- Additional subnets for future expansion  

---

## 🔢 Subnetting Implementation

- Used fixed-length subnetting (FLSM)  
- Selected subnet mask to meet:
  - Required number of hosts  
  - Required number of subnets  

- Created multiple subnets from the original /24 network  
- Assigned:
  - Router interfaces → first usable IP  
  - Switch → second usable IP  
  - PCs → subsequent usable IPs  

---

## ⚙️ Key Configurations

### 🔹 Router Configuration
- Configured interfaces:
  - `G0/0`  
  - `G0/1`  
  - `Loopback 0`  
  - `Loopback 1`  
- Assigned IP addresses based on subnet design  
- Enabled all interfaces  

---

### 🔹 Switch Configuration
- Configured management VLAN interface  
- Assigned IP address and default gateway  
- Applied standard security configurations  

---

### 🔹 PC Configuration
- Assigned static IP addresses  
- Configured subnet masks and default gateways  

---

## 🧪 Verification & Testing
- Tested connectivity using:
  - `ping` between PCs  
  - PC → Router interfaces  
  - PC → Loopback networks  

- Performed troubleshooting:
  - Incorrect gateway configuration  
  - IP/subnet mismatches  

---

## 🛠 Tools Used
- Cisco Packet Tracer (v8.2.2)  
- Cisco IOS CLI  

---

## 🎯 Learning Outcome
This lab helped me understand:
- Subnetting and IP address planning  
- Fixed-length subnet masking (FLSM)  
- Network design based on requirements  
- Router interface configuration  
- Troubleshooting IP addressing issues  

---

## 🚀 Key Takeaway
This lab demonstrates the ability to design scalable and structured IP addressing schemes, which is essential for real-world network planning and deployment.

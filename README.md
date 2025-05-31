# OSPF-Area-Types-Virtual-link-Lab
“Lab exploring OSPF stub, NSSA, and virtual link configurations”
# 🚀 OSPF Advanced Area Types Lab | Stub, Totally Stubby, NSSA, Totally NSSA & Virtual Link

Welcome to my deep-dive lab on **OSPF (Open Shortest Path First)** area types! This project focuses on understanding and implementing different OSPF area configurations using Cisco routers, highlighting how they impact LSA (Link-State Advertisement) propagation and routing behavior.

---

## 🧠 What I Explored

🔹 **Stub Area**  
🔹 **Totally Stubby Area**  
🔹 **NSSA (Not-So-Stubby Area)**  
🔹 **Totally NSSA**  
🔹 **Virtual Link** for non-backbone area connectivity to Area 0

This lab simulates real-world scenarios where different area types help reduce overhead, optimize LSA flooding, and maintain OSPF scalability.

---

## 🔍 Key Takeaways

✅ Understanding the suppression of LSA Types 3, 4, 5, and 7 based on area types  
✅ Practical usage of `area [id] stub`, `nssa`, and `no-summary` commands  
✅ Impact of each area on the OSPF database and routing table  
✅ Virtual link configuration to connect discontiguous Area 0

---

## 🗺️ Lab Topology

> https://github.com/amarasrinivas0055/OSPF-Area-Types-Virtual-link-Lab/tree/main/topology%20images


---

## ⚙️ Config Files

Configuration snippets for stub, nssa, virual link enabled router are available under the [`/configs`](./configs) directory:
- `R9`, `R10`, `R11`, etc.
- Configs before and after stub/NSSA implementation
- Output screenshots of LSA database and routing table

---

## 📚 Commands Highlighted

```bash
# Stub area
area 10 stub

# Totally Stubby area
area 20 stub no-summary

# NSSA
area 30 nssa

# Totally NSSA
area 1 nssa no-summary

# Virtual Link
area 70 virtual-link <6.6.6.6>

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

> ## 🗺️ Lab Topology

![OSPF Topology](topology%20images/OSPF-AREA-VIRTUAL%20LINK.PNG)




---

## ⚙️ Config Files

Configuration snippets for stub, nssa, virual link enabled router are mentioned below
- `R9`, `R10`, `R11`, etc.
- Configs before and after stub/NSSA implementation
- Output screenshots of LSA database 
- 
- R9-BEFORE-STUB-AREA -LSA-4, LSA-5

![Image](https://github.com/user-attachments/assets/a14019fe-ce3b-47ee-b69a-fe5e146fe91a)


R9-AFTER-STUB-AREA -LSA-4, LSA-5

![Image](https://github.com/user-attachments/assets/baf1df7b-2668-4dea-a068-acba6729dc37)

R10-BEFORE-TOTALLY-STUB LSA-3,LSA-4,LSA-5

![Image](https://github.com/user-attachments/assets/a1c8123e-a932-4f87-a0ce-a7483c266dcd)

R10-AFTER-TOTALLY-STUB LSA-3,LSA-4,LSA-5

![Image](https://github.com/user-attachments/assets/b96d7f5d-984f-4c4e-8f86-0efa0992a1a3)

R11-POST-NSSA-LSA-7, No LSA-4, NO LSA-5

![Image](https://github.com/user-attachments/assets/3ef9b0d5-838a-45ad-abf9-2cec3ebf3b41)


R11-POST-FULL-NSSA-LSA-7, No LSA-3, LSA-4, NO LSA-5

![Image](https://github.com/user-attachments/assets/ac8be406-94e1-46aa-af37-b98947ed8c78)

R15-END-TO-END REACHABILITY VIA VIRTUAL LINK 

![Image](https://github.com/user-attachments/assets/7e73e55e-f8c5-4c70-8fc3-381ecdc9b424)

AREA-7 ROUTES VIA VIRTUAL LINK ON R1

![Image](https://github.com/user-attachments/assets/a6054958-575c-4511-aace-7150475d372a)

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
area 10 virtual-link <6.6.6.6> on router 14
area 10 virtual-link <14.14.14.14> on router 6


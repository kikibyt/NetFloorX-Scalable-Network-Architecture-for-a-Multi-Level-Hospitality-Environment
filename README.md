# NetFloorX-Scalable-Network-Architecture-for-a-Multi-Level-Hospitality-Environment


**NetFloorX** is a simulated multi-floor network infrastructure project designed for a modern hotel environment using Cisco Packet Tracer. The project showcases the planning, segmentation, and secure implementation of a hierarchical network system across three floors with distinct departmental needs. It's ideal for showcasing hands-on networking skills in routing, VLANs, IP addressing, DHCP, SSH, OSPF, port security, and wireless access configuration.

![network visual topology](https://github.com/user-attachments/assets/6232f9d4-ccc9-4e85-bf04-ae39527cadb5)



## 🏨 Project Overview

**NetFloorX** models the end-to-end design and deployment of a scalable, segmented network for *Vic Modern Hotel*, structured across three floors. Each floor houses different departments, requiring tailored VLAN setups, inter-router communication, and security policies.

Key components of this implementation include:

- VLAN segmentation by department
- Inter-router communication via serial DCE links
- OSPF dynamic routing protocol
- DHCP configuration per floor
- SSH for secure remote access
- Port security for critical access points
- Wireless access on each floor

---

## 🧾 Case Study: Hotel Network Layout

| Floor      | Departments                          |
|------------|--------------------------------------|
| 1st Floor  | Reception, Store, Logistics          |
| 2nd Floor  | Finance, HR, Sales & Marketing       |
| 3rd Floor  | IT, Administration                   |

---

## 📐 Network Design Highlights

- **Router Placement:** 3 routers (one per floor), all physically located in the 3rd-floor server room.
- **VLAN Allocation:** Each department gets a unique VLAN and subnet.
- **Wireless Connectivity:** Access points configured on all floors for Wi-Fi.
- **Printer Integration:** One networked printer per department VLAN.
- **Inter-Router Links:** Subnetted serial connections using:
  - `10.10.10.0/30`
  - `10.10.10.4/30`
  - `10.10.10.8/30`

---

## 🧭 VLAN and IP Scheme

| Floor     | Department     | VLAN ID | Network Address     |
|-----------|----------------|---------|---------------------|
| 1st       | Reception       | 80      | 192.168.8.0/24      |
|           | Store           | 70      | 192.168.7.0/24      |
|           | Logistics       | 60      | 192.168.6.0/24      |
| 2nd       | Finance         | 50      | 192.168.5.0/24      |
|           | HR              | 40      | 192.168.4.0/24      |
|           | Sales/Marketing | 30      | 192.168.3.0/24      |
| 3rd       | Admin           | 20      | 192.168.2.0/24      |
|           | IT              | 10      | 192.168.1.0/24      |

---

## 🔧 Key Configurations

- **Routing:** OSPF used for efficient and dynamic route distribution.
- **DHCP:** Each floor router acts as a DHCP server for its respective VLANs.
- **SSH:** Secure router management enabled on all routers.
- **Port Security:** Strict control on Fa0/1 in the IT VLAN; only Test-PC is authorized.
- **Wireless:** Wi-Fi APs available on all floors for mobile device connectivity.

---

## 🔍 Addressing Summary

| Floor     | VLANs        | Subnets            |
|-----------|--------------|--------------------|
| 1st       | 60, 70, 80    | 192.168.6-8.0/24   |
| 2nd       | 30, 40, 50    | 192.168.3-5.0/24   |
| 3rd       | 10, 20        | 192.168.1-2.0/24   |

---

## 🧪 Testing and Verification

- ✅ **Inter-VLAN Communication** across routers via OSPF
- ✅ **Dynamic IP Assignment** via DHCP
- ✅ **SSH Access** verified from the IT department
- ✅ **Port Security** tested with violation shutdown on unauthorized devices
- ✅ **Wireless Access** tested successfully for mobile connectivity

---

## 🛠 Technologies Used

- **Cisco Packet Tracer** – Network simulation
- **Hierarchical Network Design** – Core, distribution, access layers
- **VLANs/Subnetting** – Logical segmentation
- **Router-on-a-Stick** – Inter-VLAN routing
- **DHCP/SSH/Port Security** – IP allocation & security
- **Wireless Access Point Setup**

---

## 📂 Repository Structure

```
NetFloorX/
├── Network Topology Diagram.png
├── VicHotel_Network.pkt
├── VLAN_Configurations.txt
├── OSPF_Settings.txt
├── DHCP_Script.txt
├── SSH_Config.txt
└── README.md
```

---

## 💡 Future Enhancements

- Integration with cloud-based remote access simulation
- Advanced threat detection via ACLs and IDS simulation
- SNMP/NetFlow traffic monitoring
- Redundant topology for failover scenarios

---

## 📜 License

This project is licensed under the MIT License.

---

## 🙌 Acknowledgments

- Cisco Networking Academy – foundational concepts
- Packet Tracer – network design and simulation tool
- Online communities for troubleshooting and advice

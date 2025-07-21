
# 🏨 Hotel Management System — Cisco Packet Tracer Network Project

<div align="center">
  <img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&pause=1000&color=00D4AA&center=true&vCenter=true&width=700&lines=Smart+Hotel+Network+Infrastructure;Inter-VLAN+%7C+Email+%7C+Web+%7C+IoT+%7C+FTP+%7C+DHCP;Designed+using+Cisco+Packet+Tracer+v8%2B" alt="Typing SVG" />
</div>

<div align="center">

![Platform](https://img.shields.io/badge/Platform-Cisco%20Packet%20Tracer-0092BF?style=for-the-badge&logo=cisco&logoColor=white)
![VLAN](https://img.shields.io/badge/VLANs-Enabled-purple?style=for-the-badge)
![IoT](https://img.shields.io/badge/IoT-Simulation%20Ready-orange?style=for-the-badge)
![DHCP](https://img.shields.io/badge/DHCP-Dynamic%20IP%20Assign-green?style=for-the-badge)
![FTP](https://img.shields.io/badge/FTP-Server-blue?style=for-the-badge)
![Web](https://img.shields.io/badge/Web-Hosted-green?style=for-the-badge)
![Email](https://img.shields.io/badge/Email-Internal%20Mail%20System-yellow?style=for-the-badge)

</div>

---

## 🌐 Project Overview

This network simulates a **multi-branch hotel management system** with secure communications between managers and directors, reliable infrastructure for 60+ employees, hosted services (email, web, FTP), and smart IoT device integration.

---

## 🏗️ Hotel Network Architecture

### 🏢 Hotel Branches (x3)
Each branch contains:
- Local staff PCs
- IoT devices (e.g., smart doors, thermostats)
- A managed switch and DHCP relay
- Internet access via router

### 🎯 Central HQ
- Director & Manager VLANs
- Centralized Web, Email, FTP, DNS, and DHCP servers
- Inter-VLAN routing between Manager ↔ Director
- ACLs for controlled access

---

## 🔧 Technical Configuration

| Feature                | Description                                                                 |
|------------------------|-----------------------------------------------------------------------------|
| 🟪 **VLANs**           | Separate VLANs for Manager, Director, Workers, IoT, and Guests              |
| 🔀 **Inter-VLAN Routing** | Router-on-a-stick setup using sub-interfaces for manager ↔ director          |
| 🧠 **DHCP Server**     | Dynamic IPs assigned to all VLANs with helper addresses                     |
| 🧭 **DNS Server**      | Resolves `hotel.local`, `ftp.hotel.local`, `mail.hotel.local`               |
| 🌐 **Web Server**      | Hosts a responsive hotel website accessible to all clients                  |
| 📧 **Email Server**    | Internal email exchange among the 60 staff members                          |
| 📁 **FTP Server**      | Used to share hotel policy documents, staff files                           |
| 📡 **IoT Devices**     | Smart devices simulate real-time data collection                            |
| 🔐 **ACL Rules**       | - Guests can’t access internal services  
                           - Only Directors can access sensitive files  
                           - Workers limited to Web + Email |

---

## 💡 VLAN Assignment

| Department        | VLAN ID | Devices           |
|------------------|---------|-------------------|
| Director         | 10      | 3 PCs (HQ Only)   |
| Manager          | 20      | 3 PCs (Per Branch)|
| Staff (Workers)  | 30      | 60 PCs            |
| IoT Devices      | 40      | Smart Sensors     |
| Guest            | 50      | Laptops / Mobile  |

---

## 🧪 Testing & Verification

You can test the network using the following:

```bash
# On any PC
ping 192.168.x.x
tracert mail.hotel.local
ipconfig /all

# On router
show ip interface brief
show ip route
show access-lists

# On FTP client
ftp ftp.hotel.local
````

✅ Try sending emails between workers
✅ Access hotel website using internal DNS
✅ Test inter-VLAN routing between Director and Manager
✅ Verify IoT sensors pushing simulated data
✅ Check FTP upload/download permission

---

## 📂 Tools & Requirements

* **Cisco Packet Tracer 8.x or higher**
* Layer 2 and Layer 3 switches
* 3 branch routers
* 1 centralized HQ router and servers

---

## 👤 Author

**Saad Khan**
📧 Email: [saado652004@gmail.com](mailto:saado652004@gmail.com)
🐙 GitHub: [@saadoxyz](https://github.com/saadoxyz)

---

## 🧠 Pro Tip

> “In this project, VLANs ensure secure segmentation between roles like managers, directors, and staff. The DHCP and DNS automate IP resolution, while IoT and Web services simulate a real hotel’s infrastructure. ACLs act like firewalls to limit who can access what.”

---

<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&height=100&section=footer&customColorList=11,17,23" />
</div>
```

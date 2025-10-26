# 🏦 Secure Enterprise Banking Network Simulation

A **comprehensive enterprise banking network simulation** built and configured using **Cisco Packet Tracer**.  
This project demonstrates advanced **network engineering**, **security**, and **enterprise service integration** — from VLAN segmentation to centralized server management and WAN connectivity.

---

## 🚀 Highlights

- 🧩 **VLAN Segmentation** – Logical separation of devices into VLANs (Employees, Servers, Management, Branch) for enhanced performance and security.  
- 🔁 **Inter-VLAN Routing** – Router-on-a-Stick configuration ensures seamless communication between VLANs.  
- 🌐 **Dynamic Routing (EIGRP)** – Enables efficient and fault-tolerant routing across HQ and branch offices.  
- 🔒 **Access Control (ACLs)** – Extended ACLs restrict external access, allowing only DNS and Web services from outside.  
- 🖥️ **Secure Remote Management** – SSH access and console line passwords enforce strict management security.  
- 🧭 **Centralized Services** – DHCP, DNS, Web, FTP, Email, and Syslog servers deliver enterprise-grade infrastructure.  
- 🏗️ **Hierarchical Topology** – HQ and branch offices connected via a simulated WAN following best-practice design principles.

---

## 🗺️ Network Topology Overview

**Headquarters (HQ):**
- Core router and multilayer switch
- Centralized enterprise servers (DNS, DHCP, FTP, Web, Email, Syslog)

**Branch Office:**
- Local switches and user endpoints
- Integrated routing via EIGRP

**WAN / Internet Simulation:**
- External router emulating internet access
- ACL boundaries for traffic control and testing

---

## 🛠️ Technologies & Protocols

| Category        | Protocol / Tool                     | Purpose                                       |
|-----------------|-------------------------------------|-----------------------------------------------|
| **Simulation**  | Cisco Packet Tracer                 | Network design, configuration, and testing    |
| **Routing**     | EIGRP, Static Routing               | Dynamic internal routing and default gateway  |
| **Security**    | ACLs, SSH, Console Line Protection  | Secure access and traffic filtering           |
| **Addressing**  | DHCP, VLAN Tagging (802.1Q)         | IP management and logical segmentation        |
| **Application** | HTTP, DNS, SMTP, POP3, FTP          | Web, email, file sharing, and name resolution |

---

## ⚙️ How to Run & Test

### 🧾 Prerequisites
- **Cisco Packet Tracer** (latest version recommended)

### 🧪 Steps
1. **Open the Project**  
   Load the provided `.pkt` file in Cisco Packet Tracer.

2. **Verify Internal Connectivity**  
   - Ping across VLANs (e.g., HQ PC ↔ Branch PC) to confirm Inter-VLAN and EIGRP routing.

3. **Test ACLs**  
   - ✅ *Expected Success:* HQ PCs can access Web, FTP, and Email servers internally.  
   - ❌ *Expected Block:* External clients (via OUTSIDE-Router) can **only** reach Web and DNS servers.  
     Other services (FTP, Email, SSH) are **denied by ACLs**.

4. **Check DHCP Operation**  
   - Confirm that PCs automatically receive IP configurations.

5. **Validate Email Flow**  
   - Test sending and receiving internal emails (e.g., `admin@gmail.com` ↔ `emp@gmail.com`).

---

## 💬 Feedback & Contributions

💡 Found an issue or have suggestions?  
Open an **[issue](../../issues)** or start a **[discussion](../../discussions)** to contribute.

---

### 🧠 Author Notes

This project is ideal for:
- Networking students and professionals studying **Cisco enterprise design**  
- Learners preparing for **CCNA/CCNP** practical labs  
- Simulation of **real-world secure enterprise environments**

---

### 📜 License

This project is distributed under the **MIT License**.  
Feel free to use and modify with proper attribution.

---

⭐ **If you found this project useful, consider starring the repo!**  
Your support helps grow the open-source networking community.

---

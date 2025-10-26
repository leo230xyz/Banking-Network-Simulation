🏦 Secure Enterprise Banking Network Simulation

This project is a detailed simulation of a multi-branch enterprise banking network, built and configured using Cisco Packet Tracer. It demonstrates expertise in modern network design, including VLAN segmentation, dynamic routing protocols (EIGRP), secure remote access (SSH), centralized services, and robust security policies (Access Control Lists).

🚀 Key Features and Implemented Services

This simulation integrates critical networking functions and services to represent a functional enterprise environment:

1. Network Segmentation & Routing

VLAN Implementation: The network is logically segmented into multiple VLANs (e.g., Employees, Servers, Management, Branch) to improve performance, security, and broadcast domain management.

Inter-VLAN Routing: Achieved using a Router-on-a-Stick configuration on the core router, enabling seamless communication between different VLANs.

EIGRP (Enhanced Interior Gateway Routing Protocol): Used as the primary routing protocol within the bank's internal network to ensure dynamic and efficient path discovery and fault tolerance.

Default Routing: A static default route is configured on the edge router to direct all traffic destined for unknown external networks (the internet/WAN) to the correct gateway.

2. Security and Access Control (ACL)

The project includes a critical Extended Access Control List (ACL) implementation on the edge router (HQ-Router) to enforce a security boundary:

Source Network

Destination Access

Rationale

Internal Bank Networks (Trusted)

Full Access (Any/Any)

Employees require unrestricted access to all internal and external services.

External/Unknown Networks (Untrusted)

Restricted Access (DNS & Web only)

Limits external exposure; prevents unauthorized access to sensitive services like FTP, SSH, or Syslog.

SSH Configuration: Devices are configured for SSH access (in preference to Telnet) for secure, encrypted remote management by IT staff.

Console Line Security: Console access is secured with robust passwords to prevent unauthorized physical access to network devices.

3. Infrastructure and Application Services

DHCP (Dynamic Host Configuration Protocol): Configured to automatically assign IP addresses, subnet masks, and default gateway information to end devices within specific VLANs.

DNS Server: Maps domain names (e.g., bank.com, mail.bank.com) to their corresponding IP addresses.

Web Server (HTTP/HTTPS): Hosts the bank's external-facing website, accessible to the public (as governed by the ACL).

FTP Server (File Transfer Protocol): Configured for internal employee use to manage and share files securely within the network.

Email Server (SMTP/POP3): Allows employees to send and receive internal communications (user@bank.com).

Syslog Server: Centralizes logging and monitoring of network device events and errors, crucial for operational troubleshooting and security auditing.

🗺️ Network Topology

The network design follows a standard hierarchical model, connecting a central Headquarters (HQ) to a Branch Office over a simulated WAN link.

The topology is divided into functional areas:

Headquarters (HQ): Houses the core router, multi-layer switch, and all centralized servers (DNS, Web, Mail, FTP, Syslog).

Branch: Includes its own switch infrastructure and user devices, connected via the EIGRP routing domain.

WAN / External: The connection to the "internet" through a separate router to test the Default Route and the ACL security policy.

🛠️ Technologies & Protocols Used

Category

Protocol / Tool

Purpose

Simulation

Cisco Packet Tracer

Network design, configuration, and testing.

Routing

EIGRP, Static Routing

Dynamic internal routing and external gateway configuration.

Security

Access Control Lists (ACL), SSH, Console Line Security

Filtering traffic, restricting access, and secure device management.

Addressing

DHCP, VLAN Tagging (802.1Q)

Dynamic IP distribution and logical network separation.

Application

HTTP, DNS, SMTP, POP3, FTP

Providing web services, name resolution, email, and file sharing.

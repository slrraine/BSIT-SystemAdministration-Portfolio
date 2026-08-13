# Week 2 – Enterprise Infrastructure Planning

## Student Information

* **Name:** Sofia Lorraine Gonzaga
* **Course:** Bachelor of Science in Information Technology (BSIT)
* **Section:** BSIT-4A
* **Date:** August 13, 2026

---

# Project Overview

This project focuses on planning the initial IT infrastructure of a newly established software development company from the ground up. It covers workstation hardware and enterprise software requirements, networking equipment, an enterprise network topology design, system administration role definitions, security and backup strategies, infrastructure expansion plans, and a reflective analysis.
The proposed infrastructure was designed for **ABC Startup Solutions**, a fictional software development and digital solutions startup with 20 employees operating on a single office floor.

---

# Learning Objectives

* Analyze the foundational IT requirements of a small enterprise software startup.
* Formulate itemized inventories for hardware, software, and networking assets with realistic specifications.
* Establish structured asset tracking mechanisms using standardized Markdown tables.
* Design an enterprise network topology using standard diagramming symbols and logical segmentation.
* Understand key System Administration roles, common tools, industry certifications, and cross-functional operational workflows.
* Develop actionable infrastructure recommendations spanning ISP redundancy, network security, backup strategies, and physical expansion.
* Practice professional technical documentation and version control utilizing GitHub Markdown formats.

---

# Company Scenario

**ABC Startup Solutions** is a startup software development and digital solutions company located in San Pablo City, Laguna, Philippines. The company develops web applications, mobile applications, business management systems, and cloud-based solutions.
The company operates on a single office floor with **20 employees** distributed across four primary departments:

| Department | Employees |
| :--- | ---: |
| Information Technology | 5 |
| Human Resources | 4 |
| Finance | 5 |
| Sales | 6 |
| **Total** | **20** |

The company initially lacks computers, servers, network infrastructure, internet connectivity, and security policies. The following documentation details the complete end-to-end IT infrastructure deployment plan prepared before equipment procurement.

---

# Company Profile

### Company Name
ABC Startup Solutions

### Nature of Business
Software Development and Digital Solutions Startup

### Company Vision
To become a trusted market leader in digital transformation by delivering innovative, scalable, and secure software solutions globally.

### Company Mission
To design, build, and deploy high-performing software products using modern technologies while adhering to strict security, operational efficiency, and system reliability standards.

### Office Location (Fictional)
Suite 502, 5th Floor, Innovation Tech Tower, Barangay San Rafael, San Pablo City, Laguna, Philippines

### Organizational Structure
* **Chief Executive Officer (CEO)**
  * **IT Department Head**
    * Junior System Administrator
    * Lead Software Developer
    * Full-Stack Developers (3)
  * **Human Resources Manager**
    * HR Specialists / Recruiter (3)
  * **Finance Manager**
    * Senior Accountant / Financial Analysts (4)
  * **Sales & Marketing Director**
    * Account Executives / Marketing Representatives (5)

### Employee Distribution

| Department | Number of Employees |
| :--- | :--- |
| Information Technology | 5 |
| Human Resources | 4 |
| Finance | 5 |
| Sales | 6 |
| **TOTAL** | **20** |

---

# Enterprise Hardware Inventory

| Asset ID | Hardware | Quantity | Department | Purpose |
| :--- | :--- | :--- | :--- | :--- |
| **HW-DEV-01 to 05** | Developer Desktop Computer | 5 | Information Technology | High-performance workstation (Core i7 / 32GB RAM) for coding, compilation, and dockerized test environments. |
| **HW-OFF-01 to 09** | Office Standard Desktop | 9 | HR (4), Finance (5) | Standard workstation (Core i5 / 16GB RAM) for accounting software, HR management, and document processing. |
| **HW-LAP-01 to 06** | Business Laptop | 6 | Sales | Portable ultrabook (Core i5 / 16GB RAM) for sales presentations, client visits, and remote communications. |
| **HW-SRV-01** | Rackmount Server | 1 | Shared (IT Core) | On-premise server (Intel Xeon / 64GB RAM) hosting local Active Directory, DNS, local git repositories, and databases. |
| **HW-RTR-01** | Enterprise Router | 1 | IT / Network Rack | Manages high-speed routing between external ISPs, internal subnets, and local network gateways. |
| **HW-SWT-01** | 48-Port Managed Switch | 1 | IT / Network Rack | Delivers high-speed wired Ethernet connectivity and VLAN isolation across all office departments. |
| **HW-PRN-01 to 02** | Multifunction Network Printer | 2 | Shared (HR / Finance) | Network-attached laser printer/scanner for heavy office documentation, contracts, and financial reporting. |
| **HW-UPS-01 to 03** | Smart UPS Battery Backup | 3 | Server / Network Rack | Provides clean power filtering and battery runtime to prevent data loss during unexpected power outages. |
| **HW-WAP-01 to 02** | Wireless Access Point | 2 | Office Floor | Provides encrypted Wi-Fi 6 wireless coverage across the floor for laptops, mobile devices, and guests. |
| **HW-NAS-01** | NAS Storage Device | 1 | IT / Network Rack | 4-bay high-capacity storage array for centralized local data retention and daily incremental backups. |
| **HW-EXT-01 to 02** | External Backup Drive | 2 | IT Department | Portable 4TB encrypted external hard drives used for physical offsite backup rotation schemes. |
| **HW-MON-01 to 25** | 27-inch FHD Monitor | 25 | All Departments | Dual-monitor setups for IT/Finance and single display setups for HR/Sales standard workstations. |

---

# Enterprise Software Inventory

| Software | Version | License | Purpose |
| :--- | :--- | :--- | :--- |
| **Windows 11 Pro** | 23H2 | Commercial Volume | Client operating system required for domain joining, BitLocker encryption, and Active Directory group management. |
| **Ubuntu Server** | 24.04 LTS | Open Source (Free) | Stable Linux operating system for hosting staging servers, internal databases, and developer pipelines. |
| **Microsoft Office / Microsoft 365** | Business Premium | Commercial Subscription | Core office productivity tools (Word, Excel, PowerPoint) and cloud service connectivity (Teams, Exchange email). |
| **VS Code** | Latest | Open Source (Free) | Primary lightweight Integrated Development Environment (IDE) utilized by developers for software programming. |
| **Git** | 2.x | Open Source (Free) | Distributed version control system tracking local software source code updates across developer workstations. |
| **GitHub Desktop** | Latest | Open Source (Free) | Graphical user interface facilitating visual version control operations and repository synchronization. |
| **VirtualBox** | 7.x | Open Source (GPL v3) | Hypervisor software for creating isolated virtual environments to test system updates and multi-OS scenarios safely. |
| **Google Chrome** | Latest | Freeware | Enterprise-managed web browser used across all departments for SaaS applications and general research. |
| **Microsoft Defender** | Enterprise | Included with OS / M365 | Integrated endpoint security suite providing real-time malware protection, system scans, and firewall controls. |
| **AnyDesk** | Professional | Commercial License | Secure remote desktop administration utility for IT staff to troubleshoot remote employee issues. |
| **7-Zip** | 24.x | Open Source (GNU LGPL) | Archival tool for compressing files, reducing attachment sizes, and securing archives with AES-256 encryption. |

---

# Enterprise Network Inventory

| Equipment Name | Quantity | Specifications / Standards | Purpose |
| :--- | :--- | :--- | :--- |
| **ISP Fiber Modem** | 1 | GPON Optical Network Terminal | Connects the company directly to the Internet Service Provider's fiber network backbone. |
| **Enterprise Router** | 1 | Gigabit WAN/LAN, NAT, Stateful DHCP | Performs core IP routing, DHCP lease generation, and WAN connection management. |
| **Hardware Firewall** | 1 | Next-Generation Firewall (NGFW) | Provides perimeter inspection, intrusion detection, packet filtering, and corporate VPN termination. |
| **48-Port Managed Switch** | 1 | Layer 2/3 Managed, 802.1Q VLAN | Connects all wired clients, segmenting department traffic logically via distinct VLANs. |
| **Wireless Access Point (AP)** | 2 | Wi-Fi 6 (802.11ax), Ceiling Mount | Delivers high-speed encrypted wireless coverage throughout the single office layout. |
| **24-Port Patch Panel** | 2 | Cat6 Unshielded 1U Rackmount | Terminates structured Ethernet cabling originating from office wall drops into the server rack. |
| **CAT6 Cables** | 1000 ft | Category 6 UTP Solid Copper 23AWG | Backbone cabling infrastructure supplying high-speed gigabit throughput across the office. |
| **RJ45 Connectors** | 100 pcs | Cat6 Pass-Through Modular Plugs | Crimp connectors used to terminate CAT6 ethernet cabling drops and custom patch leads. |

---

# Enterprise Network Diagram

The network topology utilizes a structured edge-to-access layer architecture. Incoming internet traffic enters through the ISP Modem, passes through the Enterprise Router and Hardware Firewall, and flows into a central 48-port managed switch. The switch routes traffic to isolated departmental VLANs, server infrastructure, and network access points.

System Administration Roles

### 1. Helpdesk Technician

* **Responsibilities:**
  * Serves as the primary Tier 1/Tier 2 point of contact for internal staff reporting hardware, software, network, or account issues.
  * Logs, categorizes, prioritizes, and resolves incoming service tickets within target Service Level Agreements (SLAs).
  * Provisions, configures, and deploys workstation hardware, peripherals, operating systems, and client software.
  * Manages user access lifecycle operations, including onboarding, offboarding, group policy adjustments, and password resets.
  * Escalates specialized hardware failures, infrastructure outages, or security threats to Tier 3 administrators.

* **Skills:**
  * Operating system diagnostics across Windows 11, Linux distributions, and macOS.
  * Desktop hardware maintenance, component replacement, and peripheral troubleshooting.
  * Active listening, customer service skills, and non-technical communication.
  * Fundamental networking knowledge (TCP/IP, DHCP, DNS, wireless configuration).

* **Common Tools:**
  * **Ticketing & ITSM:** Jira Service Management, Freshdesk, Zendesk.
  * **Remote Desktop Utility:** AnyDesk, TeamViewer, Windows Remote Desktop (RDP).
  * **Directory Services:** Microsoft Active Directory, Microsoft 365 Admin Center, Microsoft Intune.
  * **System Diagnostics:** Windows Sysinternals, Command Prompt / PowerShell network tools (`ping`, `ipconfig`, `tracert`).

* **Certifications:**
  * **CompTIA A+**
  * **Microsoft Certified: Modern Desktop Administrator Associate** (MD-102)
  * **ITIL 4 Foundation**

---

### 2. Network Administrator

* **Responsibilities:**
  * Configures, deploys, and maintains enterprise routers, managed switches, hardware firewalls, and wireless access points.
  * Manages IP addressing, subnetting schemes, and 802.1Q VLAN configurations to isolate departmental network traffic.
  * Monitors network health, bandwidth utilization, packet latency, and uptime using SNMP monitoring platforms.
  * Establishes and manages site-to-site and client-based Virtual Private Network (VPN) tunnels for secure remote operations.
  * Enforces perimeter security rules, access control lists (ACLs), firewall policies, and firmware maintenance.

* **Skills:**
  * Expertise in routing protocols (OSPF, BGP) and switching technologies (VLAN trunking, Spanning Tree Protocol).
  * Hands-on proficiency with firewall configuration, NAT/PAT, and intrusion detection system (IDS/IPS) management.
  * Deep understanding of OSI layers, packet header analysis, and network security standards.
  * Structured cabling management, patch panel termination, and hardware rack organization.

* **Common Tools:**
  * **Packet & Traffic Analysis:** Wireshark, tcpdump.
  * **Simulation & Lab Tools:** Cisco Packet Tracer, GNS3, EVE-NG.
  * **Network Monitoring:** SolarWinds Network Performance Monitor, PRTG, Zabbix.
  * **Terminal & Configuration:** PuTTY, Tera Term, SecureCRT.

* **Certifications:**
  * **Cisco Certified Network Associate (CCNA)**
  * **CompTIA Network+**
  * **Juniper Networks Certified Associate - Junos (JNCIA-Junos)**

---

### 3. Linux System Administrator

* **Responsibilities:**
  * Provisions, updates, and maintains Linux-based server infrastructure (e.g., Ubuntu Server, RHEL).
  * Configures web servers (Nginx/Apache), database systems (MySQL/PostgreSQL), and container runtimes (Docker).
  * Writes and maintains shell scripts to automate system maintenance, routine backup routines, and log rotations.
  * Enforces system security standards, SSH key management, user file permissions, and software security patches.
  * Monitors system performance metrics (CPU, RAM usage, storage I/O) to prevent service downtime.

* **Skills:**
  * Command-line interface (CLI) mastery and shell scripting (Bash, Python).
  * Advanced Linux file system hierarchy, privilege management (`sudo`, POSIX/ACLs), and process management.
  * Containerization technologies and basic configuration management tools.
  * System logging and kernel-level troubleshooting.

* **Common Tools:**
  * **Remote Shell & Utilities:** OpenSSH, tmux, htop, Netdata.
  * **Automation & Orchestration:** Ansible, Docker, Systemd, Cron.
  * **Web & Database Services:** Nginx, Apache, MySQL, PostgreSQL.

* **Certifications:**
  * **Red Hat Certified System Administrator (RHCSA)**
  * **Linux Foundation Certified System Administrator (LFCS)**
  * **CompTIA Linux+**

---

### 4. Cloud Administrator

* **Responsibilities:**
  * Deploys, configures, and oversees cloud environments (AWS, Azure, Google Cloud Platform).
  * Configures identity access, policies, and privileges using Identity and Access Management (IAM).
  * Monitors cloud expenditure, optimizes resource allocation, and sets up automated billing alerts.
  * Implements automated cloud backup policies, storage lifecycle management, and disaster recovery architectures.
  * Ensures cloud infrastructure aligns with enterprise cybersecurity compliance frameworks.

* **Skills:**
  * Deep understanding of cloud service models (IaaS, PaaS, SaaS) and serverless architectures.
  * Infrastructure as Code (IaC) provisioning and configuration.
  * Cloud network design (Virtual Private Clouds, Security Groups, Load Balancers).
  * Cloud monitoring, logging, and cost optimization.

* **Common Tools:**
  * **Cloud Portals:** AWS Management Console, Microsoft Azure Portal.
  * **Infrastructure as Code:** Terraform, AWS CloudFormation.
  * **CLI & Monitoring:** AWS CLI, Azure CLI, Amazon CloudWatch, Azure Monitor.

* **Certifications:**
  * **AWS Certified SysOps Administrator – Associate**
  * **Microsoft Certified: Azure Administrator Associate** (AZ-104)

---
Infrastructure Recommendations

### Internet Provider
* **Recommendation:** Primary connection with PLDT Enterprise Fiber (500 Mbps) backed up by a secondary Converge ICT Business Fiber line (200 Mbps).
* **Justification:** Software development demands uninterrupted network availability for cloud commits and client communication. Dual ISPs connected to a router with automatic failover prevent complete outages.

### Server Specifications
* **Recommendation:** Dell PowerEdge R450 Rack Server (Intel Xeon Silver 4310, 64GB DDR4 ECC RAM, 4x 1.2TB SAS HDDs in RAID 10 configuration, Dual Hot-Plug Power Supplies).
* **Justification:** RAID 10 yields optimal drive performance and data redundancy. ECC RAM protects against memory-level corruptions, and dual power supplies safeguard against hardware power failures.

### Backup Strategy
* **Recommendation:** Implementation of the **3-2-1 Backup Strategy**.
* **Justification:** Three copies of data are maintained across two media types (on-premise server RAID and local Synology NAS), with one copy stored offsite using encrypted cloud backups (AWS S3 Glacier).

### Security Recommendations
* **Recommendation:** Implement Role-Based Access Control (RBAC), multi-factor authentication (MFA) on all domain accounts, and VLAN isolation between internal departments and guest Wi-Fi.
* **Justification:** Segregating network access prevents lateral movement across subnets if a workstation is compromised.

### Antivirus
* **Recommendation:** Centralized deployment of Microsoft Defender for Business managed through Microsoft Intune.
* **Justification:** Offers native operating system integration, low host performance overhead, real-time threat prevention, and single-pane administrative monitoring.

### Password Policy
* **Recommendation:** Enforce 12-character minimum passwords containing uppercase, lowercase, numbers, and symbols; require 90-day rotations; enforce MFA globally; block standard password dictionaries.
* **Justification:** Mitigates risk from brute-force attempts and credential-stuffing exploits.

### Expansion Plan
* **Recommendation:** Install 48-port switch and patch panel infrastructure with ~50% spare port capacity; utilize standardized cable management in server racks; adopt cloud-scalable deployment architectures.
* **Justification:** Allows the organization to double its physical headcount on the current floor without requiring complete network hardware replacement.

---

# PART 8: Personal Reflection

Completing this enterprise infrastructure planning project provided hands-on experience in evaluating organizational workflows from an IT management perspective. I learned that system administration involves far more than configuring software applications or assembling PC components; it requires structured analysis of enterprise operations, security controls, hardware budgeting, and future growth planning.
Designing the enterprise network topology was one of the most practical learning experiences in this project. It clarified how routing gateways, firewalls, managed switches, and VLAN segmentation operate synchronously to maintain data security and optimized packet routing across separate business departments.
Overall, this activity demonstrated the absolute necessity of detailed technical documentation prior to physical deployment. Developing a structured infrastructure roadmap upfront prevents costly procurement mistakes, streamlines system installation, minimizes security risks, and establishes an expandable foundation for scalable software startup operations.

---



# Week 2 – Enterprise Infrastructure Planning

## Student Information

* **Name:** Sofia Lorraine Gonzaga
* **Course:** Bachelor of Science in Information Technology (BSIT)
* **Section:** BSIT-4A
* **Date:** August 13, 2026

---
# Project Scenario

You have recently been hired as the **Junior System Administrator** of **ABC Startup Solutions**, a newly established software development company. The company currently has **20 employees** and occupies a single office floor. 
Management has requested that you prepare a complete **IT Infrastructure Plan** before purchasing any equipment.

# Project Overview

This project focuses on planning the initial IT infrastructure of a newly established software development company from the ground up. It covers workstation hardware and enterprise software requirements, networking equipment, an enterprise network topology design, system administration role definitions, security and backup strategies, infrastructure expansion plans, and a reflective analysis.
The proposed infrastructure was designed for **ABC Startup Solutions**, a fictional software development and digital solutions startup with 20 employees operating on a single office floor.

---

# Learning Objectives

Upon completion of this enterprise infrastructure planning activity, the student will be able to:

* **Assess Enterprise Technical Requirements:** Analyze hardware, software, and networking requirements to support a 20-employee software startup across four operational departments.
* **Architect a Secure Network Topology:** Design a professional network diagram using Draw.io featuring perimeter defense, enterprise routing, core switching, and wireless integration.
* **Formulate Enterprise Asset Inventories:** Develop structured, itemized inventory lists for hardware components, software licenses, and network equipment using standardized Markdown tables.
* **Delineate System Administration Operations:** Map core IT administration roles—Helpdesk, Network, Linux, and Cloud—to specific responsibilities, toolsets, certifications, and cross-functional workflows.
* **Establish Disaster Recovery & Security Policies:** Develop a multi-tiered 3-2-1 backup scheme, dual-ISP redundancy, password governance, and physical expansion strategies.
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

The professional hierarchical enterprise network topology was designed for **ABC Startup Solutions**. The architectural layout secures external edge connectivity before distributing network traffic to the core switch layer and individual departmental endpoints.

![Enterprise Network Topology Diagram](diagrams/network-topology.png "ABC Startup Solutions - Enterprise Network Topology")
---

# Technical Stack & Portfolio Overview

<details>
<summary><b>🛠️ Technologies & Tools Used</b></summary>

### **Hardware Infrastructure**
* **Workstations & Laptops:** Intel Core i7 / i5 Systems, Business Class Ultrabooks
* **Server & Storage:** Intel Xeon Rackmount Server, 4-Bay NAS Array, Encrypted External Drives
* **Networking Equipment:** GPON Fiber Modem, Enterprise Gigabit Router, Next-Generation Firewall (NGFW), 48-Port Managed Switch (802.1Q VLAN), Wi-Fi 6 Access Points (802.11ax)
* **Power & Cabling:** Smart UPS Battery Backups, Cat6 UTP Cabling, 24-Port Patch Panels

### **Software & Operating Systems**
* **Operating Systems:** Windows 11 Pro, Ubuntu Server 24.04 LTS
* **Productivity & Communication:** Microsoft 365 Business Premium, Google Chrome
* **Development & Virtualization:** VS Code, Git, GitHub Desktop, Oracle VirtualBox
* **Security & System Utilities:** Microsoft Defender Enterprise, AnyDesk Professional, 7-Zip

### **Diagramming & Documentation**
* **Diagramming Tool:** Draw.io (diagrams.net)
* **Documentation Standard:** GitHub Flavored Markdown (GFM)
</details>


<details>
<summary><b>⚠️ Challenges Encountered & Solutions</b></summary>

### 1. **Balancing Budget Constraints with High Hardware Demands**
* **Challenge:** Software development workloads (compilation, running Docker containers) require heavy compute specs, but startup budgets are tight.
* **Solution:** Implemented role-based hardware tiering—allocating high-performance Core i7/32GB RAM desktops exclusively to developers while standardizing Core i5/16GB setups for HR, Finance, and Sales.

### 2. **Ensuring Network Security in an Open Office Environment**
* **Challenge:** Preventing unauthorized traffic between departments (e.g., Sales or Guest Wi-Fi access reaching sensitive Finance and HR records).
* **Solution:** Designed a network topology centered around managed switch 802.1Q VLAN segmentation, backed by Next-Generation Firewall rules to strictly isolate traffic across departmental zones.

### 3. **Designing for Business Continuity on a Single Floor**
* **Challenge:** Protecting local source code repositories and corporate data against sudden power failures, local hardware failures, or catastrophic data loss.
* **Solution:** Formulated a complete 3-2-1 backup strategy incorporating local RAID NAS storage, physical encrypted offsite hard drives, and cloud backups, backed by rackmount UPS battery systems to handle power outages gracefully.

### 4. **Planning Physical Cable Layout and Port Scalability**
* **Challenge:** Designing a patch panel and switch arrangement that meets current office needs without becoming obsolete when the startup expands.
* **Solution:** Deployed a 48-port managed switch and 24-port patch panel setup with approximately 50% unused port capacity, allowing the company to double headcount on the same floor without replacing core network switches.
</details>

# PART 8: Personal Reflection

Completing this enterprise infrastructure planning project provided hands-on experience in evaluating organizational workflows from an IT management perspective. I learned that system administration involves far more than configuring software applications or assembling PC components; it requires structured analysis of enterprise operations, security controls, hardware budgeting, and future growth planning.
Designing the enterprise network topology was one of the most practical learning experiences in this project. It clarified how routing gateways, firewalls, managed switches, and VLAN segmentation operate synchronously to maintain data security and optimized packet routing across separate business departments.
Overall, this activity demonstrated the absolute necessity of detailed technical documentation prior to physical deployment. Developing a structured infrastructure roadmap upfront prevents costly procurement mistakes, streamlines system installation, minimizes security risks, and establishes an expandable foundation for scalable software startup operations.

---
# References

* **Amazon Web Services.** (n.d.). *AWS Cloud Architecture Center*. Amazon Web Services, Inc. Retrieved August 13, 2026, from https://aws.amazon.com/architecture/
* **Cisco Systems.** (2023). *Small and Medium Business Network Design Guide*. Cisco Systems, Inc. https://www.cisco.com/c/en/us/solutions/small-business/networking.html
* **CompTIA.** (2024). *CompTIA Network+ N10-008 & Security+ SY0-701 Certification Roadmap*. CompTIA Properties, LLC. https://www.comptia.org/
* **Cybersecurity and Infrastructure Security Agency.** (2023). *Capacity Enhancement Guide: Vol. 1 - Enterprise Backup Strategies (3-2-1 Rule)*. CISA. https://www.cisa.gov/resources-tools/guides
* **Dell Technologies.** (2024). *Dell PowerEdge R450 Rack Server Spec Sheet*. Dell Inc. https://www.dell.com/en-us/shop/povw/poweredge-r450
* **Diagrams.net.** (n.d.). *Draw.io Flowcharting and Network Diagramming Software*. JGraph Ltd. https://www.draw.io/
* **Microsoft.** (2024). *Microsoft 365 Business Premium Architecture & Security Documentation*. Microsoft Learn. https://learn.microsoft.com/en-us/microsoft-365/business-premium/
* **Microsoft.** (2024). *Windows 11 Pro Enterprise Deployment and Active Directory Integration*. Microsoft Learn. https://learn.microsoft.com/en-us/windows/deployment/
* **PLDT Enterprise.** (2025). *Enterprise Managed Fiber & Corporate Internet Solutions*. PLDT Inc. https://pldtenterprise.com/
* **Canonical Ltd.** (2024). *Ubuntu Server 24.04 LTS Documentation*. Canonical Ltd. https://ubuntu.com/server/docs


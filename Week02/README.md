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


# Week 3: Enterprise Server Deployment and Operating System Installation

**Course / Subject:** System Administration and Maintenance  
**Prepared by:** Sofia Lorraine Gonzaga  
**Hostname:** `server01`  
**Date:** August 14, 2026  

---

## 1. Project Overview

This project documents the step-by-step deployment, configuration, and verification of an **Ubuntu Server 26.04 LTS** virtual machine using Oracle VM VirtualBox. It covers virtual machine creation, guided LVM disk partitioning, OpenSSH network configuration, post-installation system verification via CLI, and an architectural analysis comparing low-level system firmware (BIOS vs. UEFI) and enterprise server operating systems.

---

## 2. Learning Objectives

* Deploy a fully functional Linux server environment using Oracle VM VirtualBox.
* Configure non-root administrative credentials (`sofialorraine`) and domain hostname (`server01`).
* Practice storage partition planning using standard LVM file system schemas.
* Enable secure remote administration protocols via OpenSSH Server.
* Validate core networking, system updates, and service statuses using Linux terminal commands.
* Compare low-level hardware firmware standards (BIOS vs. UEFI) and analyze system boot sequences.

---

## 3. Virtual Machine Specifications

| Parameter | Specification |
| :--- | :--- |
| **VM Name** | `Ubuntu-Server-Week03` |
| **Guest OS Type** | Linux / Ubuntu (64-bit) |
| **Base Memory (RAM)** | 2048 MB (2 GB) |
| **Processors** | 1 vCPU |
| **Virtual Disk Type** | VDI (VirtualBox Disk Image) |
| **Storage Allocation** | 40.00 GB (Dynamically Allocated) |
| **Network Adapter 1** | NAT (Network Address Translation) |

---

## 4. Installation Summary

1. **Media Attachment & Booting:** Attached the Ubuntu Server ISO to the VirtualBox optical drive and powered on the VM.
2. **Language & Keyboard Setup:** Selected **English** as the primary installer language and set keyboard layout to **English (US)**.
3. **Network & Mirror Selection:** Applied automatic IPv4 DHCP configuration on adapter `enp0s3`, left proxy settings blank, and accepted the default mirror (`ph.archive.ubuntu.com`).
4. **Storage Partitioning:** Configured **Guided - Use An Entire Disk** on the 40 GB virtual drive (`VBOX_HARDDISK`) with a guided LVM partition scheme (`ubuntu-vg`).
5. **Profile & Identity Setup:** Configured user `sofialorraine` and assigned system hostname `server01`.
6. **SSH Setup & Completion:** Enabled **`[X] Install OpenSSH Server`**, skipped optional snap packages, executed installation, completed security updates, and rebooted the system.

---

## 5. Configuration Summary

| Parameter | Assigned Value / Setting |
| :--- | :--- |
| **Hostname** | `server01` |
| **Administrative User** | `sofialorraine` |
| **Partition Scheme** | Guided LVM (`ubuntu-vg`) |
| **Root File System** | `ext4` (18.996 GB Volume) |
| **Boot Partition** | `/boot` (`ext4`, 2.00 GB) |
| **Active Network Interface** | `enp0s3` (NAT Mode) |
| **Assigned IPv4 Address** | `10.0.2.15/24` |
| **Enabled Services** | OpenSSH Server (`sshd`) |
---

## 6. Verification Results

### Task 1 – System Login
Logged into the server using created administrative credentials (`sofialorraine`).
* **Command:** `server01 login: sofialorraine`

![Task 1 - System Login](images/W3task1_login.png)

---

### Task 2 – Verify Hostname
Verified that the server hostname accurately matches assignment specifications.
* **Command:** `hostname`
* **Output:** `server01`

![Task 2 - Verify Hostname](images/W3task2_hostname.png)

---

### Task 3 – Verify IP Address
Checked network interface configuration and active IP allocation.
* **Command:** `ip addr`
* **Output:** Interface `enp0s3` inet `10.0.2.15/24`

![Task 3 - Verify IP Address](images/W3task3_ipaddr.png)

---

### Task 4 – Test Internet Connectivity
Verified DNS resolution and outbound packet transfer via NAT interface.
* **Command:** `ping -c 4 google.com`
* **Output:** `4 packets transmitted, 4 received, 0% packet loss`

![Task 4 - Test Internet Connectivity](images/W3task4_testinternetconnectivity.png)

---
### Task 5 – Update the Server
Refreshed repository index and updated installed system packages.
* **Commands:**
  ```bash
  sudo apt update
  sudo apt upgrade -y
![Task 5 - Test Internet Connectivity](images/W3task5_update.png)


### Task 6 – Verify SSH Service
Confirmed that the OpenSSH daemon is active and listening for incoming remote connections.

* **Commands:**
  ```bash
  systemctl status ssh
  Output: Active: active (running)

![Task 6 - Verify SSH Service](images/W3task6_verifySSH.png)

## 7. BIOS vs UEFI Highlights
### Comparison Table

| Feature | Legacy BIOS | UEFI |
| :--- | :--- | :--- |
| **Definition** | Legacy firmware initializing hardware during startup. | Modern firmware architecture replacing BIOS. |
| **Boot Process** | Loads 16-bit code from Master Boot Record (MBR). | Executes 32/64-bit `.efi` binaries from EFI Partition. |
| **Max Disk Support** | Up to **2 TB** | Up to **9.4 ZB** |
| **Partition Scheme** | MBR (max 4 primary partitions) | GPT (up to 128 primary partitions) |
| **Security** | Basic password check; vulnerable to bootkits. | **Secure Boot** cryptographic verification. |
| **Speed** | Slower sequential device testing. | Fast parallel hardware initialization. |

## 8. Challenges Encountered

### Challenge 1: `watchdog: BUG: soft lockup - CPU#0 stuck!` Warnings
* **Issue:** Soft lockup warnings appeared in the console during package mirror updates.
* **Resolution:** Recognized this as temporary CPU resource queuing under VirtualBox single-vCPU constraints and allowed the installation process to finalize without interrupting the virtual machine.

### Challenge 2: Package Mirror Fetch Errors
* **Issue:** Running `sudo apt upgrade -y` produced temporary HTTP fetch errors when retrieving specific Linux firmware archives.
* **Resolution:** Refreshed source lists and executed missing file flags:
  ```bash
  sudo apt update
  sudo apt upgrade --fix-missing -y

## 9. Reflection
Building and verifying a headless Linux server environment within Oracle VM VirtualBox provided critical practical insight into real-world system administration. Transitioning from desktop-oriented graphical user interfaces to a pure command-line interface highlights the fundamental trade-offs between user convenience and enterprise system efficiency. Without a GUI overhead, Ubuntu Server operates with minimal system memory utilization, leaving maximum host computing resources available for core services, application containers, and background processing.

Understanding virtual hardware configuration was equally valuable during this activity. Setting up VirtualBox NAT mode demonstrated how guest virtual machines interact with host networking through virtual DHCP and router abstractions. Evaluating partition schemes reinforced the necessity of Logical Volume Management (LVM) in production environments. Unlike legacy static disk partitioning, LVM abstracts physical storage into logical volumes, providing the flexibility to resize file systems dynamically as server storage requirements scale over time.

Additionally, analyzing low-level boot procedures—from initial hardware handoff in UEFI firmware to kernel initialization and systemd target management—demystified how modern operating systems transition from raw power delivery to operational user prompts. Secure Boot mechanisms and GPT partition standards clearly demonstrate why UEFI has replaced legacy BIOS in modern server deployments.

Ultimately, this lab exercise reinforced the core discipline of system administration: precise configuration execution, structured troubleshooting, and empirical verification through CLI utilities like `ip`, `ping`, `systemctl`, and `apt`. These skills serve as the foundational bedrock for managing enterprise cloud infrastructure, containerized deployments, and remote server environments.

---

## 10. References

* Canonical Ltd. (2026). *Ubuntu Server Guide*. Ubuntu Documentation. https://help.ubuntu.com/
* Oracle Corporation. (2026). *Oracle VM VirtualBox User Manual*. https://www.virtualbox.org/manual/
* Tanenbaum, A. S., & Bos, H. (2015). *Modern Operating Systems* (4th ed.). Pearson.

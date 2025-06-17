# 🖥️ Windows 10 Client Setup & Domain Join – Home Lab Project

This section documents the setup of two Windows 10 virtual machines configured as client endpoints in an enterprise-like domain environment. These systems will be joined to the Active Directory Domain hosted on the Windows Server 2019 Domain Controller. The goal is to simulate realistic enterprise environments for Blue Team and Red Team practices.

---

## 🎯 Project Goal

To deploy and configure two Windows 10 desktops as domain-joined workstations to:
- Complete the Active Directory lab environment
- Facilitate attacker/defender simulations
- Practice Group Policy deployment, user/group management, and endpoint security

---

## 🖥️ Environment Setup

- **Virtualization Software**: VMware Workstation Pro
- **ISO Download**: [Windows 10 Evaluation ISO](https://www.microsoft.com/en-us/evalcenter/evaluate-windows-10-enterprise)

---

## 🔧 Installation Instructions

### 🔹 Step 1: Prepare Windows 10 VM (Repeat for Both Desktops)

1. Launch VMware and create a new virtual machine.
2. Use typical settings and attach the Windows 10 ISO.
3. Skip the product key entry; click **Next**.
4. Choose the edition that matches your environment (e.g., Windows 10 Pro or Enterprise).
5. Accept the license terms and proceed.

### 🔹 Step 2: Disk Configuration

1. Choose **Custom Install**.
2. Click **New**, then **Apply**, and confirm with **OK**.
3. Click **Next** and continue installation.

---

### 🔹 Step 3: Post-Installation Configuration

1. Choose **"Continue with limited setup"** when prompted.
2. Set the first user (must match a user created in AD
Set the security answers
3. Uncheck ALL the privacy settings then select Accept
   
<img width="554" alt="Screenshot 2025-06-17 182215" src="https://github.com/user-attachments/assets/e74c0835-95c4-492e-a98b-bd8753c2ea7c" />

** Choose "Not Now" for Cortana

While you wait set up the second desktop with the second user account credentials but the same configurations.


Search "pc name" and change the PC Name according to the designated users

Restart the PC
   

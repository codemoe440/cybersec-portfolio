# 🐉 Kali Linux Installation – Home Lab Project

This section documents the setup of Kali Linux as the **attacker machine** in the cybersecurity home lab. Kali Linux will be used to simulate offensive actions such as vulnerability scanning, brute-force attacks, and exploit testing against the Windows Domain Controller and other machines in the network.

## 📌 Purpose
To simulate real-world attack scenarios within a controlled environment for learning and practicing penetration testing, red teaming, and ethical hacking methodologies.

## 🖥️ Environment Setup

- **Host Machine:** Windows Laptop  
- **Virtualization Software:** VMware Workstation Pro  
- **Network Configuration:**  
  - **Network Adapter:** Custom `VMnet2` (isolated lab environment)  
  - **Memory:** 4GB RAM (minimum)

## 🔧 Installation Steps

1. **Download Kali Linux**
   - Download the Kali Linux ISO or prebuilt VM image from the official source:  
     👉 [https://www.kali.org/get-kali/#kali-virtual-machines](https://www.kali.org/get-kali/#kali-virtual-machines)

2. **Load the Kali VM**
   - After downloading the `.7z` Kali VM archive, extract it.
   - Open the `.vmx` file in VMware Workstation to load the Kali Linux virtual machine.

3. **Configure VM Settings**
   - Before powering on:
     - Change the **Network Adapter** to `VMnet2` for lab segmentation.
     - Increase **Memory** to at least **4GB**.
     - (Optional) Adjust CPU and disk settings if needed.

     
       <img width="549" alt="Screenshot 2025-06-16 180639" src="https://github.com/user-attachments/assets/1897f2a9-6e84-44b8-8592-ea22d8eaa619" />


4. **Power On and Login**
   - Power on the Kali Linux VM.
   - Use the **default login credentials**:
     - **Username:** `kali`  
     - **Password:** `kali`


5. **Change the Default Password**
   To improve security, change the default password with the following command in the terminal:
   ```bash
   passwd

  
<img width="638" alt="Screenshot 2025-06-16 180503" src="https://github.com/user-attachments/assets/48c8f9e6-2c56-4023-a9bd-efecf20bb57e" />

## 🧠 Skills Demonstrated
Virtual machine management and configuration

Network segmentation using VMware

Password hardening and initial system setup

Preparing an attacker machine for red team simulations

## 📁 Next Steps
Configure Metasploit, Nmap, and other offensive tools

Connect Kali to the same VMnet as the Windows Server (Domain Controller)

Launch simulated attacks to test your lab's IDS/IPS (Security Onion) setup

# 🧑‍💻 Ubuntu Desktop Installation – Home Lab Project

This section outlines the setup of **Ubuntu Desktop** to simulate a Security Operations Center (SOC) Analyst's workstation. This machine will be used to access **Security Onion's web interface**, analyze alerts, and monitor logs from within the isolated cybersecurity home lab environment.

## 📌 Purpose

To serve as the analyst’s machine used for accessing Security Onion’s **SIEM dashboard**, investigating alerts, and conducting threat analysis within the lab environment.

## 🖥️ Environment Setup

- **Host Machine:** Windows Laptop  
- **Virtualization Software:** VMware Workstation Pro  
- **Network Adapter:** Custom VMnet (same VMnet as Security Onion)  
- **Memory:** 4GB (minimum recommended)

## 🔧 Installation Steps

1. **Download Ubuntu Desktop**
   - Get the latest version from the official Ubuntu website:  
     👉 [https://ubuntu.com/download/desktop](https://ubuntu.com/download/desktop)

2. **Create a New Virtual Machine in VMware**
   - Select "Typical (recommended)" for the configuration
   - Attach the downloaded Ubuntu ISO as the installer disk
   - Choose **Linux → Ubuntu 64-bit** as the guest operating system
   - Allocate at least **4GB RAM** and **2 CPUs**
  
     <img width="549" alt="Screenshot 2025-06-16 180639" src="https://github.com/user-attachments/assets/497562ae-31aa-4059-901d-c6012daac7fa" />
     

3. **Install Ubuntu**
   - Power on the VM and follow the installation wizard
   - Accept all **default settings** for simplicity
   - Set up a username and password for login

4. **Configure Networking**
   - Ensure that the **Network Adapter** is connected to the **same custom VMnet** as Security Onion
   - After installation and reboot, open the terminal and run:
     ```bash
     ifconfig
     ```
   - Note the **IP address** of the Ubuntu Desktop to verify that it’s in the same subnet as the Security Onion instance

  <img width="408" alt="Screenshot 2025-06-16 182605" src="https://github.com/user-attachments/assets/269126eb-0106-4b33-b733-7d3e4402e59b" />

     
5. **Access Security Onion Web Interface**
   - Open a browser and enter the IP address of the Security Onion server (e.g., `https://192.168.116.130`)
   - Log in using the analyst credentials you configured during the Security Onion setup

## 🧠 Skills Demonstrated

- VM creation and OS installation
- Network segmentation for lab environments
- IP address verification
- Browser-based SIEM access and interaction

## 📁 Next Steps

- Perform event analysis using Security Onion tools such as **Kibana**, **Squert**, or **Hunt**
- Launch controlled attacks from the **Kali Linux** machine and analyze the alerts generated
- Document findings and integrate into your cybersecurity portfolio

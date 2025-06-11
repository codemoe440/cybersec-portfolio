## 🔍 Security Onion Installation & Configuration – Home Lab Project

This project documents the **installation and configuration of Security Onion** in my cyber-security home lab. Security Onion serves as the **Network Security Monitoring (NSM)** and **IDS/analysis** layer, allowing the simulation of real-world detection, log management, and threat-hunting workflows.

### 📌 Project Goal
Deploy a fully functional Security Onion standalone sensor to monitor lab traffic, capture and analyze suspicious activity, and gain experience with open-source SOC tooling.

---

### 🖥️ Environment Setup

- **Host Machine:** Windows Laptop  
- **Virtualization Software:** VMware Workstation Pro  
- **Network Configuration:**  

---

### 🔧 Installation Steps

1. **Download Security Onion ISO**  
   Obtain the latest version (e.g., v2.4.70) from <https://securityonionsolutions.com/download/> *(verify the SHA‑256 hash)*

2. **Create VM in VMware**  
   - OS: Ubuntu 64-bit  
   - CPU: 4 cores  
   - RAM: 8–12 GB (16 GB+ ideal)  
   - Disk: ≥ 200 GB  
   - Add two network adapters
     
   <img width="559" alt="Screenshot 2025-06-10 183134" src="https://github.com/user-attachments/assets/63d61988-1817-4d25-918f-87150aeeaf29" />

     
3. **Install the OS & Security Onion**  
   - Boot from ISO  
   - At prompt, type **yes** to erase disk and install
     
     <img width="558" alt="Screenshot 2025-06-10 184115" src="https://github.com/user-attachments/assets/21fde087-b2b3-4ab7-8143-4a467fe6f624" />
   - Choose **Evaluation** mode
   - Configure management interface via DHCP
     
     <img width="586" alt="Screenshot 2025-06-08 203819" src="https://github.com/user-attachments/assets/f1bd7f3e-9825-4ea0-a974-8214d3228419" />
  
     <img width="614" alt="Screenshot 2025-06-08 203847" src="https://github.com/user-attachments/assets/f3a14117-745c-469b-b40a-7e5f5bd750b8" />

   - Select the Monitor interface
     
     <img width="566" alt="Screenshot 2025-06-08 203919" src="https://github.com/user-attachments/assets/33e1bf39-3a89-4b62-8cda-3b1fbeff3086" />

   - Create admin user and password
     
     <img width="569" alt="Screenshot 2025-06-08 203958" src="https://github.com/user-attachments/assets/0150286b-d1b2-49c9-8231-d2c72b626f09" />
     
     <img width="564" alt="Screenshot 2025-06-08 204014" src="https://github.com/user-attachments/assets/9bd39dc8-2020-4735-84a3-72163c3f2c28" />

   - Choose how you want to access the web interface
     
     <img width="504" alt="Screenshot 2025-06-09 122443" src="https://github.com/user-attachments/assets/46354580-695c-43b1-bceb-fbb6e653b2c7" />

   - Allow Access to web interface
     
     <img width="603" alt="Screenshot 2025-06-09 122513" src="https://github.com/user-attachments/assets/512af308-d324-4a93-841e-77ece0e9ae97" />

   - Add Ubuntu IP address to access the web interface
     
     <img width="486" alt="Screenshot 2025-06-09 122546" src="https://github.com/user-attachments/assets/250d2937-d72a-40a9-a4c8-100dfcb80c58" />
     
   - Finalize and wait for complete installation
     
     <img width="508" alt="Screenshot 2025-06-09 122602" src="https://github.com/user-attachments/assets/0d2361e2-27ab-443c-9144-55d9f1501b06" />

   - Installation Completed successfully
     
    <img width="521" alt="Screenshot 2025-06-09 130837" src="https://github.com/user-attachments/assets/0a4f08ff-1776-4aa1-bb95-237cca918a6e" />


   - Allow VM to reboot automatically


     <img width="657" alt="Screenshot 2025-06-11 154006" src="https://github.com/user-attachments/assets/e5ea11e8-642d-4ee1-9399-f5273530f432" />

   
  

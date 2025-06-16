# 🔧 pfSense Interfaces & Firewall Rules Configuration – Home Lab Project

After setting up the Kali Linux machine and verifying connectivity to the pfSense LAN interface (`192.168.1.1`), we proceed to configure the pfSense **WebConfigurator** and define custom interfaces to reflect the segmented home lab network. This section documents the step-by-step changes made via the pfSense web interface.

## 🌐 Accessing the WebConfigurator

1. Launch a web browser on your **Kali Linux** machine.
2. Navigate to https://192.168.1.1
   
<img width="556" alt="Screenshot 2025-06-16 184543" src="https://github.com/user-attachments/assets/f61f7ed4-14b0-40a6-a9b5-ea05b536ca43" />

   3. At the browser warning screen, select:
Advanced... → Proceed to 192.168.1.1 (unsafe)


---

## 🧙 pfSense Setup Wizard

Upon successful login, the **pfSense Setup Wizard** will appear. Proceed as follows:

<img width="559" alt="Screenshot 2025-06-16 212448" src="https://github.com/user-attachments/assets/a75b2637-77a4-4ee1-bd21-d69f11b65afc" />


### 🔹 Step-by-Step Wizard Configuration

- **Step 1:** Welcome – Click `Next`
- **Step 2:** Configure General Information  
- Primary DNS Server: `8.8.8.8`  
- Secondary DNS Server: `4.4.4.4`
-  Click `Next`

    <img width="551" alt="Screenshot 2025-06-16 212551" src="https://github.com/user-attachments/assets/02004f43-c220-444d-9a43-7a5f517d568d" />

- **Step 3:** Select Time Zone  
- Choose your local time zone (e.g., `Europe/London`)  
- Click `Next`
  
<img width="555" alt="Screenshot 2025-06-16 212632" src="https://github.com/user-attachments/assets/3f431762-dd27-4ead-b52a-f09802bf0ebb" />

  
- **Step 4:** WAN Interface Configuration  
- Leave as default  
- Uncheck the last two options  
- Click `Next`

  <img width="556" alt="Screenshot 2025-06-16 212841" src="https://github.com/user-attachments/assets/d76d9710-bf65-40be-b94d-0601d417143f" />


- **Step 5:** LAN Interface Configuration – Click `Next`
- **Step 6:** Admin Password  
- Set a strong admin password  
- Click `Next`

  <img width="572" alt="Screenshot 2025-06-16 213103" src="https://github.com/user-attachments/assets/b1061f24-c5ae-4dda-9386-02bd961c6594" />

- **Step 7:** Reload Configuration


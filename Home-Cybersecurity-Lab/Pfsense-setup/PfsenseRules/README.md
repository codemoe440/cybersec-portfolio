<<<<<<< HEAD
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

  <img width="366" alt="Screenshot 2025-06-16 213103" src="https://github.com/user-attachments/assets/d52917a1-1468-43e0-afb0-475ea3abdcbd" />


- **For OPT3 Be sure to Enable Interface as shown below

  <img width="554" alt="Screenshot 2025-06-16 220338" src="https://github.com/user-attachments/assets/8e7d6e4e-0733-4e1f-84bc-894411f8fa04" />

**Back at Interfaces Assignment select Bridges

Click Add

<img width="554" alt="Screenshot 2025-06-16 220502" src="https://github.com/user-attachments/assets/bb78b3f6-dabe-417c-81c2-c82aea3e5db9" />

- **Select VictimNetwork as the Member Interface

  <img width="557" alt="Screenshot 2025-06-16 220622" src="https://github.com/user-attachments/assets/ce2c5c16-510a-4322-90f7-50c8f320c603" />

  - **Then select Display Advanced

Under Advanced Configuration for Span Port, select "SPANPORT"

Scroll all the way down and Click Save

<img width="558" alt="Screenshot 2025-06-16 220747" src="https://github.com/user-attachments/assets/5aa82497-c2d3-4478-beac-44e15e96eb3a" />

- **Click Firewall >> Rules
- 
<img width="552" alt="Screenshot 2025-06-16 220949" src="https://github.com/user-attachments/assets/30c3ecff-8ccf-4a16-bfef-b8c818a54a00" />

- **Select the Add button with the arrow pointed downward

 ~ Under "edit Firewall Rule" for Protocol select ANY 

 ~ Scroll all the way down and SAVE

 
  <img width="557" alt="Screenshot 2025-06-16 221047" src="https://github.com/user-attachments/assets/0b4ca766-c996-4983-a307-15c339b349ce" />



=======
# Pfsense Interface and Rules

THis is pfsense rinterface and rules configuration
>>>>>>> 806e8d0 (Homelab-Log-Analysis)

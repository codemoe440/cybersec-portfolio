# 🛡️ Installing Splunk Universal Forwarder on Domain Controller (Windows)

This guide outlines the step-by-step process to install and configure the **Splunk Universal Forwarder (UF)** on a Windows **Domain Controller** and set up your **Splunk instance** to receive and index logs.

---

## 📋 Table of Contents

- [Objective](#objective)
- [Step 1: Configure Receiving on Splunk](#step-1-configure-receiving-on-splunk)
- [Step 2: Create a New Index (winlogevent)](#step-2-create-a-new-index-winlogevent)
- [Step 3: Download & Install Splunk Universal Forwarder on Domain Controller](#step-3-download--install-splunk-universal-forwarder-on-domain-controller)
- [Step 4: Configure the Universal Forwarder](#step-4-configure-the-universal-forwarder)
- [Step 5: Verify Connection in Splunk](#step-5-verify-connection-in-splunk)
- [Why This Matters](#why-this-matters)

---

## 🎯 Objective

Install Splunk Universal Forwarder on a Domain Controller and configure it to forward Windows event logs to a central Splunk instance for monitoring and analysis.

---

## 🔌 Step 1: Configure Receiving on Splunk

1. On your **Splunk Enterprise** instance, go to:
   - **Settings** → **Forwarding and Receiving** → **Receive data**
2. Click **Add New**.
3. Enter port `9997` (default port for UF data).
4. Save the configuration.
   
   <img width="680" alt="Forwarding and receiving" src="https://github.com/user-attachments/assets/9f0c79c7-3c17-408c-b4b8-94f9c08d54ff" />

   <img width="713" alt="Add receiving" src="https://github.com/user-attachments/assets/05dfef87-c4d0-4a2b-b557-55bcc945008e" />

   <img width="717" alt="Screenshot 2025-06-26 173205" src="https://github.com/user-attachments/assets/1a5cfc24-e403-410a-8bc2-30267e80cc37" />

   

---

## 📂 Step 2: Create a New Index (`winlogevent`)

1. Navigate to:
   - **Settings** → **Indexes** → **New Index**
2. Enter:
   - **Index Name**: `winlogevent`
   - Leave other settings default or customize as needed.
3. Save.


<img width="783" alt="index" src="https://github.com/user-attachments/assets/8c22c40f-6d98-4ee3-a3c7-226aa9c2b02f" />

<img width="788" alt="new index" src="https://github.com/user-attachments/assets/a03bf715-9749-4f01-8762-0f8e053abdbf" />

---

## 💻 Step 3: Download & Install Splunk Universal Forwarder on Domain Controller

1. Visit [Splunk Universal Forwarder Downloads](https://www.splunk.com/en_us/download/universal-forwarder.html).
2. Download the **Windows 64-bit MSI** installer.
3. On the Domain Controller, run the installer as Administrator.
4. During installation


   
    **Accept License Agreement**


     
      <img width="313" alt="Screenshot 2025-06-26 191224" src="https://github.com/user-attachments/assets/a0a2da1a-bb26-4970-837e-b067cd6011c8" /> 


 
   Set **Username and password**



     <img width="310" alt="Screenshot 2025-06-26 191245" src="https://github.com/user-attachments/assets/edf57566-fc56-4c6c-b816-4e2084b20182" />



   - Set the **Splunk Enterprise IP** as:

  
     
      **Deployment Server**
  

   
     <img width="311" alt="Screenshot 2025-06-26 191336" src="https://github.com/user-attachments/assets/9b3904f7-381e-460f-8c3c-bc6be5654bc7" />
  

   
      **Receiving Indexer**

  
       
     <img width="309" alt="Screenshot 2025-06-26 191534" src="https://github.com/user-attachments/assets/42340505-d3d2-4153-b572-16ca25fc81f0" />


   - Complete installation.

     

---

## ⚙️ Step 4: Configure the Universal Forwarder

The UF will automatically start as a service.

Ensure the following:
- The forwarder sends logs to port `9997`.
- Input configurations forward logs to the `winlogevent` index (this may be managed by the deployment server or manually via `inputs.conf`).

---

## ✅ Step 5: Verify Connection in Splunk

1. On the Splunk instance, go to:



   **Settings** → **Add Data** → **Forward**
     


     <img width="648" alt="forward" src="https://github.com/user-attachments/assets/b62d02bb-11a7-4c85-bb52-7958d3c7f1f6" />



2. You should now see your **Domain Controller hostname** listed.
   
   - select the DC
   - input server class name and next



     <img width="559" alt="select server" src="https://github.com/user-attachments/assets/2d926e17-7d59-4ca8-96e9-078210b7e97b" />

     

4. Choose local event logs


   - select the event logs you'll like to visualise and next

   

     <img width="576" alt="Screenshot 2025-06-26 201053" src="https://github.com/user-attachments/assets/537569c7-47ca-4743-a5f6-15fc7a64a330" />




6.  Input settings

   - select the index we created, "wineventlogs"



     <img width="709" alt="winevent logs" src="https://github.com/user-attachments/assets/9d7f7824-2318-478a-8cc8-19b491e40dd9" />



     

     <img width="793" alt="Screenshot 2025-06-26 203531" src="https://github.com/user-attachments/assets/d7b782e6-0621-431d-b29d-a8bb236aeee3" />



     
---


## 📘 Lessons Learned

- Gained hands-on experience with **endpoint log forwarding** using Splunk UF.
- Learned the importance of **indexing and categorizing logs** for efficient searching.
- Understood how to set up **Splunk as a central log receiver** using port `9997`.
- Improved understanding of **domain controller log sources**, particularly for user authentication and system events.
- Identified how **forwarded logs** can support real-time security monitoring, incident detection, and audit compliance.


  

## 🔍 Why This Matters


Installing the Universal Forwarder on a Domain Controller enables:
- Collection of critical logs: logon attempts, user/group changes, and policy modifications.
- Centralized security monitoring.
- Detection of anomalies and security events via Splunk dashboards and alerts.
- Compliance with security and audit regulations (e.g., PCI-DSS, HIPAA, NIST).


---



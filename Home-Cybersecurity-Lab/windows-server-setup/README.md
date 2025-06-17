# 🧱 Windows Server Domain Controller – Home Lab Project

This section of the repository details how I installed and configured Windows Server 2019 as a **Domain Controller (DC)** for my cybersecurity home lab environment. The goal is to simulate an enterprise Active Directory (AD) setup with a Windows Server DC and two Windows 10 client machines for group policy, user management, and attacker/defender scenarios.

---

## 🎯 Project Goal

To deploy a centralized identity and authentication system using Active Directory with Windows Server 2019 as the Domain Controller and integrate it with other machines in the lab for real-world simulation of enterprise environments.

---

## 🖥️ Environment Setup

- **Host Machine**: Windows Laptop
- **Virtualization Software**: VMware Workstation Pro
- **Windows Server ISO**: Windows Server 2019 Standard (Evaluation)


## ⚙️ Installation Instructions

### 🔹 Step 1: Install Windows Server 2019

## Launch VMware and create a new virtual machine.



** Important Details for Windows Server Installation 

(Please read the below before installing the Windows Server on VMware)

* Install in VMware as usual with defaults

* Do not worry about a product key, simply click Next

* At the end of the installation, be sure to change the Network Adapter to Vmnet3

* Make sure to UNCHECK "Power on this virtual machine after creation".
* After the VM has been installed, click "Edit virtual machine settings" and remove the Floppy drive.
  
<img width="554" alt="Screenshot 2025-06-17 155416" src="https://github.com/user-attachments/assets/d229c97d-7036-42bd-be5e-c3f6c769a6c1" />


** Power on the Virtual Machine and immediately click any key. 

Click Next

Click Install Now

<img width="522" alt="Screenshot 2025-06-17 160117" src="https://github.com/user-attachments/assets/b0a3cfb6-cfd2-492b-ab02-8c06a3ee874e" />

** Select the Windows Server 2019 standard Evaluation (Desktop Experience)

Accept the License Terms

Click Next

Select the Custom Install

<img width="526" alt="Screenshot 2025-06-17 160214" src="https://github.com/user-attachments/assets/d785e747-9c6b-447d-aa66-2ad535d1c91a" />

** Click New

Click Apply

Click OK

Click Next

You should have this screen now

<img width="553" alt="Screenshot 2025-06-17 160321" src="https://github.com/user-attachments/assets/8e9c0767-27c3-470f-9778-5ec21e9e18ab" />

** When that is complete, create a password

<img width="558" alt="Screenshot 2025-06-17 160418" src="https://github.com/user-attachments/assets/52ba7e31-b3b9-4c68-9dc2-2c9dce4feb5b" />

** After the installation, you should end up with this screen

<img width="556" alt="Screenshot 2025-06-17 160510" src="https://github.com/user-attachments/assets/52293158-1628-4521-a839-ac299a965300" />

#### ✅ Rename the Machine

 ~ Navigate to Settings in the search bar

 ~ Search for settings in the search bar 

 ~ Search for "pc name" in the settings search

 ~ Select Rename PC and rename the PC your choice name

 ~ Select Restart Now


 ** After the reboot, on the Server Manager Dashboard, Click Manage >> Add Roles and Features 
 
<img width="722" alt="Screenshot 2025-06-17 161045" src="https://github.com/user-attachments/assets/55bb3a1d-8a00-4946-915f-1979bf79bd4a" />

** Keep clicking Next till you get to the Server Roles menu

Select Active Directory Domain Services

Select "Add Features"

<img width="556" alt="Screenshot 2025-06-17 162047" src="https://github.com/user-attachments/assets/19978744-3627-49c3-af9d-cb85977e6e4d" />

** Click on Next till you get to the Confirmation menu, then click Install

** After the Install, Click Close

** Click on the flag with the yellow caution triangle

* Select "Promote this server to  a domain controller"

* Select Add a new forest

* Specify a domain name

* Click Next

* Set a Password
Click Next till you get to the Prerequisites Check Menu

<img width="556" alt="Screenshot 2025-06-17 162047" src="https://github.com/user-attachments/assets/411967a9-b416-478c-a1c3-8b2b45556178" />



Click Install

Wait for the Reboot

<img width="557" alt="Screenshot 2025-06-17 163705" src="https://github.com/user-attachments/assets/94e4863f-0ebc-49b3-bf21-051905ee9103" />

** After the Reboot, Log back in

Select Manage >> Add Roles & Features again on the Server Manager

Click Next till you get to Server Roles

<img width="722" alt="Screenshot 2025-06-17 161045" src="https://github.com/user-attachments/assets/44295bb5-ac8d-4189-ad5f-47ee30e1e46a" />

** Select Active Directory Certificate Services

Select Add Features

<img width="545" alt="Screenshot 2025-06-17 163926" src="https://github.com/user-attachments/assets/ab4c6b0c-935b-4a19-a34a-77c4ac8dc19a" />

** Click Next till you get to the "Confirmation" menu

Check "Restart the destination server automatically if required"

Select Yes

Select Install

After the Installation, Click Close

<img width="550" alt="Screenshot 2025-06-17 164027" src="https://github.com/user-attachments/assets/c25cdccd-3ef2-4fa1-8a25-f84529c7fe25" />

** Click on the flag with the yellow caution triangle

Select "Configure Active Directory Certificate Services on the destination server"

** Click Next on Credentials

On the Role Services menu, check Certification Authority

<img width="551" alt="Screenshot 2025-06-17 164143" src="https://github.com/user-attachments/assets/573effea-4415-4137-9682-e0c992891779" />

** Click Next till you get to the Validity period menu and change it to 99 years

Click Next till you get to the Confirmation menu

Then select Configure

<img width="554" alt="Screenshot 2025-06-17 164218" src="https://github.com/user-attachments/assets/c584792b-6ece-47c9-83f6-b2f1c662c0df" />

** Manually restart the server in order for all the settings to take effect.

Now add some Users:

## ~ Back at the Server Manager Select Tools > Active Directory Users and Computers

<img width="275" alt="Screenshot 2025-06-17 164608" src="https://github.com/user-attachments/assets/3c2d5664-15c6-4e8b-9885-ae8669a4f8ae" />

** Select your Domain Name CODEMOE.local) > Users, Right Click & Select New > User 

	~ Enter a First, Last & User logon name for the user (Disregard the "WIN10" and just set a preferred logon name).

 <img width="369" alt="Screenshot 2025-06-17 164813" src="https://github.com/user-attachments/assets/e1cb02de-dd46-4d79-b8bf-d2bc9a86907f" />

 ** Set a password that never expires. Select Finish.

 <img width="388" alt="Screenshot 2025-06-17 165022" src="https://github.com/user-attachments/assets/366b40bb-2a0f-451f-962d-5fe8ad21b2cb" />

## Use pfsense as the default gateway for the Domain Controller
** Navigate to Control Panel > Network and Internet > Network Connections

 ~ Enter the following configuration


<img width="476" alt="Screenshot 2025-06-17 165628" src="https://github.com/user-attachments/assets/21873895-db03-4b2d-a93e-da6becca81b5" />


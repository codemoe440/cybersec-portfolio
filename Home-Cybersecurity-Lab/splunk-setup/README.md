## Splunk set up on Ubuntu server

---
Splunk is one of the most widely adopted Security Information and Event Management (SIEM) platforms in the cybersecurity industry. It collects and aggregates logs and data from multiple sources, allowing security teams to efficiently search, parse, and index events for monitoring, detection, and analysis.

In this lab, I’ll walk through the process of installing Ubuntu Server and setting up Splunk, preparing the environment for centralized log collection and security event analysis.

---

## Step 1: Installing Ubuntu Server for the Splunk Instance
- Download ubuntu server https://ubuntu.com/download/server
---
Begin by downloading the latest Ubuntu Server ISO from the official Ubuntu website.

Once the download is complete, create a new virtual machine using your preferred virtualization platform (e.g., VMware or VirtualBox) with the recommended settings. After configuring the VM, start the virtual machine to begin the Ubuntu Server installation process.


<img width="538" alt="Screenshot 2025-06-23 180849" src="https://github.com/user-attachments/assets/973d79fd-8d1f-4f88-b896-5e41bbb721b9" />


---
---
Before powering on the machine, enter the Virtual Machine Settings and remove the CD/DVD drive with the file named autoinst.iso, as well as the Floppy drive with the file autoinst.flp


Install the server using all the default settings and create a profile

---
---

Installing an OpenSSH server is based on your preference but I recommend installing it.
You can also add any services you want but it's not necessary for this lab.


During the installation, you'll be prompted to remove the CD(ISO) remove it and then reboot the VM. 


After the VM has rebooted, your sign-in screen should look something similar to this.

---


Installing an OpenSSH server is based on your preference but I recommend installing it.
You can also add any services you want but it's not necessary for this lab.


During the installation, you'll be prompted to remove the CD(ISO) remove it and then reboot the VM. 


After the VM has rebooted, your sign-in screen should look something similar to this.


<img width="771" alt="Screenshot 2025-06-23 150847" src="https://github.com/user-attachments/assets/3306c2ab-04aa-4df5-ae00-9d420b715bb8" />

---
##  you have one of two options

- Accessing it with the AnalystVM using SSH

- Installing a GUI (Ubuntu Desktop) on the Ubuntu Server


I'll be installing a GUI on the Ubuntu Server for this lab using the following steps:

- Install tasksel

sudo apt install tasksel
- Install the ubuntu desktop GUI but note that there are a variety of options to choose from 

sudo  tasksel
---

<img width="628" alt="Screenshot 2025-06-23 155920" src="https://github.com/user-attachments/assets/95c3f12f-994d-473d-8474-f3e7836e4259" />


<img width="650" alt="Screenshot 2025-06-23 162056" src="https://github.com/user-attachments/assets/56c63e7b-75e8-4fa4-862c-0ae08a0a91c7" />


- Reboot the VM with the "reboot" command

reboot
After rebooting, you should have your GUI.


<img width="717" alt="Screenshot 2025-06-23 163629" src="https://github.com/user-attachments/assets/90a9083f-79d4-4858-bf29-97a37c03c611" />

## Installing Splunk

- On your Ubuntu Server, Navigate to Splunk.com 

- Click on "Free Splunk"

- Create an account or login

- Under "Splunk Core Products" >> Splunk Enterprise >> Download Free 60-Day Trial

- Select the Linux package and download the .tgz file


Open the terminal and navigate to the downloads directory

- Untar the file

- Navigate to the ~/splunk/bin directory

- Use the command ./splunk start to start the splunk instance. 

- Enter an admin username and password  of your choice 

- Navigate to http://splunk:8000 your browser 

<img width="396" alt="Screenshot 2025-06-23 171152" src="https://github.com/user-attachments/assets/5179b490-25e6-4ee0-b2a8-6239c93808bd" />


- Log in with the username and the password you configured in the previous step

<img width="568" alt="Screenshot 2025-06-23 171254" src="https://github.com/user-attachments/assets/49ae79f7-a7f0-458f-89c2-8340dd74a09d" />


<img width="834" alt="Screenshot 2025-06-23 171345" src="https://github.com/user-attachments/assets/7c08b801-2a0c-4056-ab54-cd223a009759" />





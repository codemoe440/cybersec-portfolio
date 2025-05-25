Home Cybersecurity Lab – Networked Enterprise Simulation
                     Project Overview
                         
This project simulates a small enterprise environment for cybersecurity training, including network segmentation, monitoring, domain control, and endpoint systems. It provides a hands-on platform for testing detection, incident response, and pentesting techniques


Netwwork Design and Topology



<img width="590" alt="Network Design and Topology" src="https://github.com/user-attachments/assets/b8bb0e47-22f9-496d-b59f-7fe83d3b3a21" />






Infrastructure Setup

| Role              | OS/Tool             |
| ----------------- | ------------------- |
| Firewall / Router | pfSense             |
| IDS / NSM         | Security Onion      |
| Workstation       | Ubuntu              |
| Attacker Machine  | Kali Linux          |
| Domain Controller | Windows Server 2019 |
| Client Machine    | Windows 10          |


Key Implementations

🔐 pfSense

pfSense is configured as the firewall for our private homelab, isolating each subnet and ensuring that only the Kali Linux host can access its management interface. This is accomplished by assigning dedicated virtual network adapters to pfSense and linking them to the appropriate VLANs.

<img width="617" alt="Pfsense-setup" src="https://github.com/user-attachments/assets/378202b8-b4f8-449c-bf96-a89a4b7e37bd" />


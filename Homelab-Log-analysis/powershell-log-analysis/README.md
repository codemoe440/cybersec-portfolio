## Introduction to Log Analysis
**Objective**:

The objective of this lab is to introduce students to the basics of log analysis and demonstrate how logs from different systems can be collected, analyzed, and used for security monitoring. Students will learn how to generate simple logs on both Windows and Linux systems and how SOC Analysts use logs to detect security incidents.


**What is a Log?**

A log is a record of events in a system that captures important actions like errors, warnings, or user activities. These logs contain key information such as:


## Timestamp
- Event Description
- Severity (Critical, Error, Warning, Information)
- Source (User, Process, Service)

  
## Logs are essential for understanding system behavior, detecting security incidents, and conducting forensic investigations.



## Example logs

🐧Linux auth.log Example

## Apr  7 10:42:15 ubuntu sshd[12345]: Failed password for invalid user admin from 192.168.1.100 port 54321 ssh2


## Explanation:

- Apr 7 10:42:15 — Timestamp
- ubuntu — Hostname
- sshd[12345] — Service name and process ID
- Failed password for invalid user admin — Failed login attempt
- from 192.168.1.100 — Source IP address
- port 54321 — Source port
- ssh2 — Protocol version


## Log Sources on Linux:

- System Logs: Stored in /var/log/, including files like syslog (system messages)
- auth.log (authentication attempts)
- kern.log (kernel-related logs).
  

## Application Logs: 

- Application-specific logs like Apache (/var/log/apache2/access.log) or
- MySQL (/var/log/mysql/error.log).


## Log Sources on Windows:

**Event Viewer**: Provides access to logs such as: 

- System Logs: Logs related to operating system events.
- Security Logs: Logs related to login attempts, permission changes, etc.
- Application Logs: Logs for system applications.
- PowerShell Logs: Logs for PowerShell commands, including suspicious execution.
  

## How Does a Cybersecurity Analyst Use Log Analysis?


- Incident Detection: Cybersecurity Analysts review logs to detect unusual or unauthorized activities, such as failed login attempts or suspicious processes.
- Forensics: Logs are used to trace back the actions taken by an attacker during or after an incident.
- Security Monitoring: Continuous log analysis helps detect potential security threats in real-time.
- Compliance: Logs assist in maintaining compliance with regulatory standards (e.g., GDPR, HIPAA).


## Popular Tools for Log Analysis:


- ELK Stack (Elasticsearch, Logstash, Kibana): A powerful suite for log collection, storage, and visualization.
- Splunk: A leading tool for searching, analyzing, and visualizing machine-generated data.
- Graylog: An open-source log management solution.
- Wazuh: An open-source security monitoring platform that integrates well with ELK for log analysis and threat detection.


## Lab Task: Simulating and Detecting Windows Powershell events


**Lab Setup**


**Requirements**:


- Systems: Windows 10/11 or Windows Server 2019/2022, Linux (Ubuntu or CentOS)



**Tools**:

  
- Windows Event Viewer
- PowerShell (Pre-installed on Windows)

  
**Preparation:**


For this lab, you will need to set up log collection on both Windows and Linux systems. Follow these steps to ensure everything is ready:


**On Windows:**


- Open Group Policy Editor (gpedit.msc):
- Navigate to Computer Configuration > Administrative Templates > Windows Components > Windows PowerShell.
- Ensure that Module Logging, Script Block Logging, and Script Execution are enabled.

**Open Event Viewer:**


<img width="435" alt="Screenshot 2025-06-18 183136" src="https://github.com/user-attachments/assets/e343849d-0dfa-450a-8213-e6628abec842" />

<img width="552" alt="Screenshot 2025-06-18 183156" src="https://github.com/user-attachments/assets/145b6dee-ee3e-4905-8d4b-f2ed979ad79c" />

<img width="604" alt="Screenshot 2025-06-18 183444" src="https://github.com/user-attachments/assets/8602a34c-c384-4d1d-b806-c8d8821e45ea" />

<img width="610" alt="Screenshot 2025-06-18 183631" src="https://github.com/user-attachments/assets/9de3102b-5e8a-4e71-bf34-ed1797589756" />



- Go to Applications and Services Logs → Microsoft → Windows → PowerShell → Operational.

  
## Step 1: Simulate a Suspicious PowerShell Command


To simulate a suspicious activity, open an elevated PowerShell session and run the following command:


- Get-LocalUser | Select-Object Name, Enabled
  
This command lists all local user accounts on the system, which could be used by attackers to enumerate users post-exploitation.

<img width="486" alt="Screenshot 2025-06-18 192410" src="https://github.com/user-attachments/assets/e2ee2d7b-0063-4c66-923e-773eb2f1865e" />



## Step 2: Detect the Log in Windows Event Viewer


- Press Win + R, type eventvwr.msc, and press Enter.

- Navigate to: Applications and Services Logs → Microsoft → Windows → PowerShell → Operational.

- Click Filter Current Log, and filter for Event ID 4104 (which logs PowerShell script execution).

- Look for an entry that shows the execution of the Get-LocalUser command.

- you will see the detials of the command that you run


<img width="692" alt="Screenshot 2025-06-18 193751" src="https://github.com/user-attachments/assets/535fbb2e-16a6-49be-acbc-34e0d066ac37" />


Conclusion:
Understanding Log Analysis: Logs are crucial for detecting, investigating, and responding to security incidents. Through the use of Windows Event Viewer and Linux log files, you can monitor system activity and identify potential security issues.

Cybersecurity Analyst Role: Cybersecurity Analysts use log analysis to detect threats, investigate incidents, and ensure system compliance.

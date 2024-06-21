# SIEM-Lab

## Objective

The VM Lab project is aimed to establish a controlled environment for detecting, prioritizing and remediating vulnerabilities. The primary focus was to setup a virtual machine running Metapsloitable 2.0 and running a credentialed scan for vulnerabilities using Nessus Essentials. After the scan is completed, we then gathered the information from the Vulnerability Report to do further prioritization and reporting for remediation. This hands-on experience was designed to deepen understanding of Vulnerability Management and its life cycle.

### Skills Learned

- Advanced understanding of SIEM concepts and practical application.
- Proficiency in analyzing and interpreting network logs.
- Ability to generate and recognize attack signatures and patterns.
- Enhanced knowledge of network protocols and security vulnerabilities.
- Development of critical thinking and problem-solving skills in cybersecurity.

### Tools Used

- Security Information and Event Management (SIEM) system for log ingestion and analysis.
- Network analysis tools (such as Nmap) for capturing and examining network traffic.
- Telemetry generation tools to create realistic network traffic and attack scenarios.

## Steps

STEP I. Create Elastic Defend and Add Agents
![Screenshot 2024-06-13 194510](https://github.com/Matike-Beseke/SIEM-Lab/assets/172703140/443ce52f-5ab2-4e9f-96c8-76669bf6a4ca)

First you go into elastic and create an Elastic Defend Integration. You should get a link to install Elastic Agent to host. Copy the link and paste it in your Kali Linux VM terminal



STEP II. Open terminal on external device to ping target host

The purpose of pinging the host is to see if it's able to communicate with external devices before the scan. With this in mind, I open terminal on our PC and we ping the host by typing "ping 192.168.1.203"

![Screenshot 2024-06-12 162431](https://github.com/Matike-Beseke/Vulnerability-Management-Lab/assets/172703140/393c4ed1-b6ba-4e36-a458-ac40d3d01adc)

As you can see, the ping was successful and my PC was able to communicate with the target host, indicating it's alive.

STEP III. Create a Credentialed Scan on Nessus

Now here is where this gets most exciting. Now it's time to have to make the credentialed scan using Nessus. First click on "Create new scan" tab on the top right corner of the Nessus menu then click on "Basic Scan" and it should take you to the screen attached below. After that, in the "Targets" tab enter the host IP Address which will be "192.168.1.203". Then name the rest as as needed to, then click "credentials".

![Screenshot 2024-06-12 162557](https://github.com/Matike-Beseke/Vulnerability-Management-Lab/assets/172703140/9fa7a78d-71a8-4f8f-8067-501008e5f6e5)

Next up is the credentials. Since this is a Linux based host, we set it on SSH. After that, ensure the Authentication method is set to "password". After that is set, enter in the admin user and password. After that is set click "Save" and run the scan.

![Screenshot 2024-06-12 162625](https://github.com/Matike-Beseke/Vulnerability-Management-Lab/assets/172703140/7ebfab69-38d3-4f83-9811-b495d8437f24)

WHY CREDENTIALS?
- Credentialed scanning involves using privileged credentials to conduct comprehensive vulnerability analysis and obtain accurate results by assessing systems and applications that are typically inaccessible without authentication.
- Uncredentialed scanning offers less precision but can still identify basic vulnerabilities that may be exploitable.

STEP IV. Analyze Vulnerability Data and Create Report

Now the final stages of the initial cycle is coming to an end. As seen below, there are 29 critical, 95 high and 138 medium vulnerabilities. Most of these vulnerabilities stem from simple passwords, out of date pluging, open ports and more.

![Screenshot 2024-06-12 162648](https://github.com/Matike-Beseke/Vulnerability-Management-Lab/assets/172703140/11eb4314-81cc-4d75-81fd-d98ad1aafca3)

Next step is to create a report on Excel or Google Sheets and you're done. You have free range of how you can filter and prioritize data according to your needs. Here are some examples below

![Screenshot 2024-06-13 134621](https://github.com/Matike-Beseke/Vulnerability-Management-Lab/assets/172703140/ca93b3f4-5972-4a3a-a00d-001c05cf0b90)

![Screenshot 2024-06-13 134732](https://github.com/Matike-Beseke/Vulnerability-Management-Lab/assets/172703140/c2924cea-e18c-4c76-a9cb-e5cb712068be)

![Screenshot 2024-06-13 135052](https://github.com/Matike-Beseke/Vulnerability-Management-Lab/assets/172703140/7930a0c6-6461-4de6-b7d0-7d2e83f1cf5e)

Now that we have made the report we are done with the lab.

# SIEM-Lab

## Objective

The Detection Lab project aimed to establish a controlled environment for simulating and detecting cyber attacks. The primary focus was to ingest and analyze logs within a Security Information and Event Management (SIEM) system, generating test telemetry to mimic real-world attack scenarios. This hands-on experience was designed to deepen understanding of network security, attack patterns, and defensive strategies.

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

First I went into elastic and created an Elastic Defend Integration. There's a link provided to install Elastic Agent to host. I then copied the link and pasted it in my Kali Linux VM terminal and proceed with commands to download.


STEP II. Run Nmap Scan and Check for Scan in Logs

Next I checked the logs to confirm the nmap scans were successful. In the command prompt i entered "nmap -p- localhost" to do a scan. 
![Screenshot 2024-06-13 194533](https://github.com/Matike-Beseke/SIEM-Lab/assets/172703140/6b13d39d-43d5-4a46-af17-f06d221c4494)

After the scan was completed I went in the logs and confirmed 

![Screenshot 2024-06-13 194912](https://github.com/Matike-Beseke/SIEM-Lab/assets/172703140/a67be7a7-1095-4b6f-b5e4-2c2cced54f27)

Here are the logs for the environment

STEP III. Create a Dashboard and Alert System for Events

This Dashboard allows me to visualize the time and frequency of the events
![Screenshot 2024-06-13 204319](https://github.com/Matike-Beseke/SIEM-Lab/assets/172703140/5847aa51-ad97-43e7-a468-bf7ea670dee3)

This is a new rule set in the alert system that allows me to get an alert through Email every time my envirnment gets scanned. 
![Screenshot 2024-06-13 202006](https://github.com/Matike-Beseke/SIEM-Lab/assets/172703140/bcc9a0a0-06c5-4041-a955-26f506a816e7)

After the rule is set, I go back in my command prompt to make another scan with "nmap -p- localhost". After that is done, I should get an alert displaying "NMAP SCAN DETECTED"

![en8nh0p6](https://github.com/Matike-Beseke/SIEM-Lab/assets/172703140/94e7e06a-61df-4eb6-999f-88805dbb1d79)



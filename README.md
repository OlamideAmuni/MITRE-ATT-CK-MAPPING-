## MITRE ATT&CK Alert Mapping – SOC Analyst Practice Project

## Project Overview
This repository contains hands-on SOC analyst practice tasks focused on analyzing simulated security alerts and mapping them to the MITRE ATT&CK framework.
Each task represents a common real-world detection scenario where an analyst must:
- Understand the alert.
- Identify attacker behavior.
- Map the activity to MITRE ATT&CK tactics and techniques.
- Identify relevant log sources.
- Define simple, actionable detection rules.

This project is designed for beginners in Security Operations (SOC) who want to strengthen their detection and triage skills.

## Project Objectives
• Practice mapping alerts to MITRE ATT&CK.
• Improve understanding of attacker Tactics, Techniques, and Procedures (TTPs)
• Learn how Windows logs and Sysmon support detection
• Build analyst thinking beyond just alert descriptions
• Document investigations clearly and professionally

## Skills Demonstrated
• SOC alert analysis
• MITRE ATT&CK mapping
• Windows Security log analysis
• Sysmon process monitoring
• Basic detection rule creation
• Analyst reasoning and documentation

## Tools & Data Sources
- MITRE ATT&CK Framework
- Windows Security Event Logs
- Sysmon
- Simulated alerts from a SOC training platform

## Task Breakdown
• Task 1 – PowerShell Base64 Encoded Command
Defense Evasion using command obfuscation
Detection of encoded PowerShell execution

  [Task1 powershell base64 encoded command](Task1/README.md)
  
• Task 2 – Brute-Force Attack with Successful Login
Initial Access via valid domain account
Detection of multiple failed logons followed by success

 [Task2 brute-force attack with successful logon](Task2/README.md)
 
 • Task 3 – Certutil Abuse (Living-off-the-Land)
Command and Control via Ingress Tool Transfer
Detection of suspicious certutil usage

 [Task3 certutil.exe abuse](Task3/README.md)
 
## Conclusion
This project focuses on understanding attacker intent, not just alert labels.
Each task demonstrates how a SOC analyst can move from alert → analysis → MITRE mapping → detection logic.

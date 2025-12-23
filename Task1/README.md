## Task 1: MITRE ATT&CK Mapping – PowerShell Base64 Encoded Command.

## Alert Description
PowerShell executed with Base64-encoded command-line arguments.
Example:
powershell.exe -EncodedCommand <Base64_String>

## MITRE ATT&CK Mapping
• Tactic:
Defense Evasion
ID: TA0005

• Technique:
Obfuscated Files or Information
ID: T1027

• Sub-Technique:
Command Obfuscation
ID: T1027.010

• Log Sources
Windows Security Log
Event ID 4688 (Process Creation)
Sysmon
Event ID 1 (Process Creation)

• Detection Rule (Simple)
Alert when PowerShell executes with Base64-encoded command-line arguments.
Examples:
powershell.exe -EncodedCommand
powershell.exe -enc
powershell.exe -ec

## Why This Is Suspicious
Attackers use Base64 encoding to obfuscate commands and evade security detection.

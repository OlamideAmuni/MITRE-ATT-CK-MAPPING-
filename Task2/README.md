## TASK 2: MITRE ATT&CK Mapping – Brute Force Followed by Successful Login

# Alert Description
Multiple failed login attempts from a single IP address followed by a successful login into a Domain Admin account within 5 minutes.

# My First Thought
This pattern strongly indicates a brute-force attack that resulted in valid account access, especially when the source IP is external.

## MITRE ATT&CK Mapping
• Tactic:
Initial Access
ID: TA0001

• Technique:
Valid Accounts
ID: T1078

• Sub-Technique:
Domain Accounts
ID: T1078.002

• Log Sources
Windows Security Log
Event ID 4625 – Failed Logon
Event ID 4624 – Successful Logon

• Detection Rules (Beginner-Friendly)
Rule 1 (Early Alert):
Alert when multiple Event ID 4625 (failed logons) occur from a single IP address within 5 minutes.
Rule 2 (Confirmed Access):
Alert when multiple Event ID 4625 are followed by Event ID 4624 from the same IP address within 5 minutes.

## Why This Matters
- This activity can lead to:
- Unauthorized access
- Privilege abuse
- Lateral movement
- Data exfiltration

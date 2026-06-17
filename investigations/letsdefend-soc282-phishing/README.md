# LetsDefend SOC282 — Simple Summary

**Case ID:** SOC282  
**Platform:** LetsDefend  
**Result:** True Positive (confirmed infection)  
**Severity:** High  
**Time to resolve:** ~30 minutes

## Short, Simple Summary

A user named Felix got a phishing email with a ZIP file named `free-coffee.zip`. The ZIP was password-protected with the password `infected`. Inside was `Coffee.exe`. VirusTotal showed the file as malicious (61/75 detections). The user ran the file, the endpoint showed `Coffee.exe` running, and we isolated the machine. We removed the email and documented the steps.

## Quick Facts
- Malware type: Backdoor (remote access)
- VirusTotal detections: 61/75
- User affected: Felix (anonymized)
- Device action: Allowed (email delivered)
- Action taken: Email deleted, device isolated

## What I Collected
- Attachment name: `free-coffee.zip` (password: `infected`)
- Executable: `Coffee.exe`
- VirusTotal detections: 61/75

## Steps I Did
1. Opened the alert in LetsDefend and documented the case
2. Reviewed the email and attachment details
3. Confirmed the ZIP was password-protected and opened the file report
4. Checked VirusTotal and confirmed the file was malicious
5. Verified the user received the email and executed the attachment
6. Checked endpoint data and saw `Coffee.exe` running
7. Removed the email from the user inbox
8. Isolated the affected machine
9. Documented the findings and next steps

## Tools used
- LetsDefend SIEM and EDR
- VirusTotal

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
- Hashes: (left as placeholders — replace with your VirusTotal values)

## Steps I Did (plain language)
1. Opened the alert in LetsDefend and created a case
2. Looked at the email headers to see who sent it
3. Found the password-protected ZIP and its password
4. Uploaded the file to VirusTotal and saw many vendors flagged it
5. Confirmed the email was delivered to the user
6. Checked the endpoint logs and saw `Coffee.exe` running
7. Deleted the email from the user's inbox to stop others
8. Isolated the user's machine to stop spread
9. Wrote this report and recommended next steps

## Tools used
- LetsDefend SIEM and EDR (built-in)
- VirusTotal for file reputation

## Notes
- All personal names and sensitive info are anonymized or removed. Replace hashes/times with your real values if you want to publish them.

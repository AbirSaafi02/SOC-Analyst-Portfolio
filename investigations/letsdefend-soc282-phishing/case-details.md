# SOC282 — phishing email investigation

## What happened (simple)
A phishing email arrived with a ZIP file called `free-coffee.zip`. The ZIP needed a password (`infected`). Inside was `Coffee.exe`. VirusTotal showed the file as malicious. The user ran the file, and the endpoint showed the program running. We removed the email and isolated the machine.

## Short timeline
- Alert opened in LetsDefend
- Found email and attachment in the Investigation channel
- Uploaded file to VirusTotal → many detections
- Checked endpoint logs → `Coffee.exe` seen running
- Deleted the email from inbox
- Isolated (contained) the host
- Documented and closed the case

## Why this was a confirmed infection
- The file was flagged by VirusTotal (61/75)
- Endpoint logs showed the exact file running
- Email was delivered and the user executed the file

## Easy prevention ideas
- Block password-protected ZIPs with EXEs at email gateway
- Teach users not to open unexpected attachments
- Monitor for EXEs running from `Downloads` folder
- Isolate devices quickly if you see suspicious processes

## What tools I used (simple list)
- LetsDefend SIEM (to find the alert and email)
- LetsDefend EDR (to check process execution and isolate)
- VirusTotal (to check file reputation)

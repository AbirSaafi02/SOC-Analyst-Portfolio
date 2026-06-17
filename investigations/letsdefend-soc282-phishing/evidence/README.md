Evidence for SOC282 (LetsDefend)

Files to add here (screenshots):
- `alert_overview.png`      — Alert summary from LetsDefend SIEM (redact email/IP)
- `email_listing.png`      — Email search showing delivery & action (Deleted)
- `virustotal_report.png`  — VirusTotal report showing 61/75 detections
- `alert_device_action.png` — Device action details (Allowed)
- `endpoint_info.png`      — Endpoint information and containment status

Notes:
- Please copy the screenshots you uploaded into this folder and name them as above.
- I recommend redacting any real email addresses, IP addresses, or usernames before committing.
- If you want, I can try to redact them automatically (I need the image files in the workspace to do that).

How to add images locally:
1. Save your screenshots into `investigations/letsdefend-soc282-phishing/evidence/`
2. Run:

```powershell
cd "c:\Users\Abir Saafi\soc-analyst-portfolio\SOC-Analyst-Portfolio"
git add investigations/letsdefend-soc282-phishing/evidence/*
git commit -m "chore: add evidence screenshots for SOC282 (redact before publishing)"
git push
```

If you want me to add and redact the images automatically, upload the PNG/JPG files into the workspace or tell me to fetch them from where you stored them.

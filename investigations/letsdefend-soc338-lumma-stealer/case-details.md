# SOC338 — Full Investigation Walkthrough

## Case Overview
- **Case ID:** SOC338
- **Title:** Lumma Stealer - DLL Side-Loading via Click Fix Phishing
- **Platform:** LetsDefend
- **Status:** True Positive
- **Severity:** High
- **Time to resolve:** ~35 minutes

## Incident Summary
A phishing campaign used a Click Fix/Windows Update-style lure to trick the user into executing a malicious payload. The payload leveraged DLL side-loading to load Lumma Stealer, a credential theft malware family. The malicious domain and process behavior matched known Lumma intelligence, making this a confirmed compromise.

## Timeline
1. Alert opened in LetsDefend
2. Email and web page content reviewed
3. Suspicious download domain `windows-update.site` identified
4. Raw network log confirmed HTTP 200 OK from Chrome
5. Endpoint detected DLL side-loading and process execution
6. Device isolated and malicious download quarantined
7. Findings documented and case closed

## Findings
### Phishing lure
- The email contained a Click Fix-style message instructing the user to apply an urgent fix.
- The landing page mimicked a Windows update/repair prompt.
- The download path included `windows-update.site`, which is not a legitimate Microsoft domain.

### Malicious execution
- The payload executed through DLL side-loading rather than a direct executable drop.
- Suspicious DLL file names were consistent with Lumma Stealer side-loading techniques.
- Process telemetry showed `chrome.exe` retrieving the malicious content and a follow-up loader executing the payload.

### Evidence collected
- Raw log screenshot showing:
  - URL: `https://windows-update.site/`
  - User-Agent: `Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:122.0) Gecko/20100101 Firefox/122.0`
  - Referrer: `https://mail.letsdefend.io/`
  - HTTP Status: `200 OK`
  - Process Name: `chrome.exe`
- Search filters screenshot showing the hash and tag:
  - `15c80b5be235bf2a8c38291eb697a702c07dde08...`
  - Tag: `Lumma,Lumma Stealer`

## Root Cause
The root cause was user interaction with a phishing web page that delivered a malicious download. The final payload used DLL side-loading to execute Lumma Stealer, enabling credential theft and data exfiltration.

## Containment and Remediation
- Isolated the impacted host from the network immediately.
- Quarantined the downloaded payload and related artifacts.
- Documented the attack chain and prepared IOC lists.
- Recommended credential reset for the affected user.

## Next steps
- Hunt for other instances of `windows-update.site` and `Lumma.Lumma Stealer` in the environment.
- Block the malicious domain at the network and email gateway.
- Review email filtering rules for similar Click Fix phishing lures.
- Confirm if any additional hosts accessed the same domain.
- Rebuild the impacted endpoint if persistence cannot be fully ruled out.
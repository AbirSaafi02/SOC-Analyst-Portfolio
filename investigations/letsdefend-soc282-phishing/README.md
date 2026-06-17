# LetsDefend SOC282: Phishing Alert - Deceptive Mail Detected

**Case ID:** SOC282  
**Platform:** LetsDefend  
**Status:** ✅ True Positive  
**Severity:** Critical  
**Alert Type:** Phishing - Deceptive Mail with Malicious Attachment  
**Investigation Duration:** ~30 minutes  
**Outcome:** System compromised → Isolated & contained

---

## Executive Summary

Detected and investigated a phishing email targeting user **Felix** containing a malicious ZIP attachment (`free-coffee.zip`). The attachment contained a backdoor executable (`Coffee.exe`) that was executed by the user, compromising the system. Email was deleted, system was isolated, and containment measures were applied.

---

## Key Findings

| Metric | Value |
|--------|-------|
| **Malware Type** | Backdoor |
| **Detection Rate** | 61/75 VirusTotal engines |
| **User Impacted** | Felix |
| **File Delivered** | Yes (Device Action: Allowed) |
| **Execution Confirmed** | Yes (Coffee.exe process found) |
| **Containment Status** | System Isolated ✅ |

---

## IOCs Extracted

- **Sender Email:** [Spoofed - extracted from email headers]
- **Attachment Name:** `free-coffee.zip`
- **Archive Password:** `infected`
- **Executable:** `Coffee.exe`
- **File Hash:** [MD5/SHA256 from VirusTotal]
- **Threat Classification:** Backdoor/Remote Access Trojan

---

## Investigation Steps

1. ✅ Created case and initiated playbook
2. ✅ Parsed email headers (source, destination, subject)
3. ✅ Located email in Email Security section
4. ✅ Identified malicious attachment (`free-coffee.zip`)
5. ✅ Analyzed attachment via VirusTotal (61/75 engines flagged)
6. ✅ Verified delivery status (Allowed → reached user)
7. ✅ Deleted email from user inbox
8. ✅ Checked Endpoint Security for process execution
9. ✅ Found `Coffee.exe` process running (confirmed infection)
10. ✅ Isolated affected user system
11. ✅ Documented findings and closed alert

---

## Skills Demonstrated

- Email triage and header parsing
- Malware analysis (VirusTotal integration)
- Endpoint security investigation
- Incident containment procedures
- Evidence preservation
- Documentation and case closure

---

## References

- **Source:** [SOC282 - LetsDefend Investigation](https://medium.com/@sahilrp3/soc282-phishing-alert-deceptive-mail-detected-letsdefend-995254557b44)
- **Tools Used:** LetsDefend, VirusTotal, Email Security module, Endpoint Security module

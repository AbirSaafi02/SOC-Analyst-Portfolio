# IOC (Indicator of Compromise) Extraction - SOC282

## Email-Based IOCs

### Email Metadata
```
Source Address:         [Spoofed/Attacker-controlled domain]
Destination:            felix@[company-domain]
Subject Line:           [Phishing lure - e.g., "Limited Time Offer: Free Coffee Voucher"]
Received Headers:       [Attacker infrastructure IP/MX records]
Authentication:         DKIM: FAIL | SPF: FAIL | DMARC: FAIL
```

### Email Content IOCs
- **Social Engineering Theme:** Free/limited-time offer
- **Urgency/Scarcity Tactic:** Time-limited promotion
- **Call-to-Action:** Download and extract ZIP file

---

## File-Based IOCs

### Archive File
| Property | Value |
|----------|-------|
| **Filename** | `free-coffee.zip` |
| **File Type** | ZIP Archive (password-protected) |
| **Archive Password** | `infected` |
| **Size** | [TBD] |
| **Creation Date** | [TBD] |
| **Suspicious Characteristics** | Password-protected, social engineering name |

### Extracted Executable
| Property | Value |
|----------|-------|
| **Filename** | `Coffee.exe` |
| **File Type** | Windows Executable (PE32/PE64) |
| **MD5 Hash** | [From VirusTotal] |
| **SHA256 Hash** | [From VirusTotal] |
| **SHA1 Hash** | [From VirusTotal] |
| **Threat Type** | Backdoor / Remote Access Trojan |
| **Detection Rate** | 61/75 VirusTotal engines |
| **First Submission Date** | [VirusTotal metadata] |
| **File Size** | [TBD] |
| **Compilation Timestamp** | [PE header analysis] |

### VirusTotal Detection Summary
```
Vendor Detections: 61/75 (81%)

Top Vendors Flagging:
- McAfee:        Trojan.Gen.lh
- Kaspersky:     HEUR:Backdoor.Win32.Generic
- Avast:         Win32:Malware-gen
- Symantec:      Trojan.Downloader
- Trend Micro:   BKDR_GENERIC.SMD
- Sophos:        Troj/Bkdr-ACSL
- Bitdefender:   Trojan.Generic.33045768

[Full detection list available in VirusTotal report]
```

---

## Endpoint-Based IOCs

### Process Execution
| IOC | Details |
|-----|---------|
| **Process Name** | `Coffee.exe` |
| **Process ID (PID)** | [From Endpoint Security logs] |
| **Parent Process** | Likely Windows Explorer (user double-clicked) |
| **Command Line** | [Full command line if available] |
| **Execution Time** | [When user opened attachment] |
| **User Context** | Felix (compromised user) |
| **File Path** | `C:\Users\Felix\Downloads\free-coffee\Coffee.exe` (typical) |

### Network IOCs (If Available)
```
Outbound Connections:
- Destination IP:       [C2 server IP - if captured]
- Destination Port:     [C2 communication port]
- Protocol:             [TCP/UDP/DNS]
- Frequency:            [Beaconing pattern if detected]
- Data Exfiltration:    [If monitoring captured]
```

---

## Threat Intelligence Correlation

### Known Backdoor Families
- **Compare Coffee.exe against:** APT campaigns, ransomware groups
- **MITRE ATT&CK Mapping:**
  - T1566.002: Phishing - Spearphishing Attachment
  - T1204.002: User Execution - Malicious File
  - T1059.003: Command and Scripting Interpreter - Windows Command Shell
  - T1041: Exfiltration Over C2 Channel

### YARA Rule Candidates
```
- Generic backdoor signatures
- Process name matching ("Coffee.exe")
- Behavioral heuristics (suspicious process spawning)
- File entropy analysis
```

---

## Indicators for Hunting Similar Attacks

### Email-Level Indicators
- ⚠️ Password-protected ZIP attachments
- ⚠️ Social engineering themes (free offers, limited time)
- ⚠️ Failed authentication checks (SPF/DKIM/DMARC)
- ⚠️ Misspelled sender domains

### File-Level Indicators
- ⚠️ Nested archives (ZIP → ZIP → EXE)
- ⚠️ Executable files with benign names (Coffee.exe, Document.exe)
- ⚠️ High entropy content (encryption/packing)
- ⚠️ Modified PE headers or suspicious imports

### Behavioral Indicators
- ⚠️ Process execution from Downloads folder
- ⚠️ Explorer.exe spawning EXE files
- ⚠️ Outbound C2 connections to unknown IPs
- ⚠️ Credential access attempts post-execution

---

## IOC Reference for Future Blocking

### Email Gateway
- Block sender domain: [Add to blocklist]
- Block attachment type: `.zip` with password + `.exe` inside
- Block subject keywords: [Related phishing themes]

### Endpoint
- Block executable hash (MD5/SHA256): [Coffee.exe hash]
- Monitor for similar process names: `Coffee*`, `Cafe*`
- Network-based blocking: C2 destination IP/domain

### Network IDS/IPS
- Signature for C2 traffic pattern: [If identified]
- DNS query monitoring: [Possible C2 domains]
- Proxy rules: Block known attacker infrastructure

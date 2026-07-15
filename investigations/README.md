# SOC Analyst Portfolio - Investigations Index

This folder contains detailed write-ups of security investigations from training platforms (LetsDefend, CyberDefenders, etc.) and practical labs.

Each investigation includes:
- **README.md** - Executive summary
- **case-details.md** - Full investigation walkthrough
- **analysis/** - Technical analysis artifacts
  - `ioc-extraction.md` - Indicators of Compromise
  - `detection-sigma.yml` - Detection rules (SIGMA, SIEM queries)
  - `threat-assessment.md` - Impact analysis & recommendations
- **evidence/** - Screenshots and supporting artifacts
- **resume-bullets.md** - 4 versions (Entry → CISO-path, kept locally and excluded from GitHub)

---

## Investigation Log

| Case ID | Title | Platform | Severity | Status | Date | Duration |
|---------|-------|----------|----------|--------|------|----------|
| SOC282 | Phishing - Deceptive Mail Detected | LetsDefend | Critical | TP ✅ | Aug 30, 2024 | 30 min |
| SOC338 | Lumma Stealer - DLL Side-Loading via Click Fix | LetsDefend | High | TP ✅ | Jun 18, 2026 | 35 min |

### When You Add a New Case
Update this page manually by:
- adding a new row to the Investigation Log table
- updating the Quick Stats totals for investigations, true positives, and any other relevant metrics
- changing the Last Updated date to the current date

---

## Quick Stats

- **Total Investigations:** 2
- **True Positives:** 2 (100%)
- **False Positives:** 0
- **Average Time to Investigate:** 30 min
- **Total IOCs Extracted:** 6+
- **Detection Rules Created:** 5

---

### Email Security
- ✅ Email header parsing
- ✅ Phishing pattern recognition
- ✅ Social engineering analysis

### Malware Analysis
- ✅ VirusTotal integration
- ✅ Archive extraction & analysis
- ✅ Executable classification
- ✅ Threat family identification

### Endpoint Forensics
- ✅ Process execution tracking
- ✅ Behavioral analysis
- ✅ Execution timeline reconstruction
- ✅ System isolation & containment

### Incident Response
- ✅ Triage & prioritization
- ✅ Evidence preservation
- ✅ Containment procedures
- ✅ Documentation & closure

### Threat Intelligence
- ✅ IOC extraction & correlation
- ✅ Threat actor infrastructure mapping
- ✅ Threat hunting

---

## Next Investigations to Add

Following SOC 2026 Roadmap:

### Foundation Projects (P1-P6)
- [ ] P1 - Live SOC Monitoring (Multiple alerts)
- [ ] P2 - Phishing Email Analysis (CyberDefenders CTF)
- [ ] P3 - Incident Response (SIEM investigation)
- [ ] P4 - Ransomware Forensics
- [ ] P5 - Threat Hunting Exercise
- [ ] P6 - Detection Engineering Lab

### Automation Projects (P7-P8)
- [ ] P7 - SOAR Automation Lab
- [ ] P8 - Threat Intelligence Platform

### Advanced Projects (P9-P14)
- [ ] P9 - AI-Assisted Threat Hunting
- [ ] P10 - Cloud Security Investigation
- [ ] P11 - AD Attack & Defense Lab
- [ ] P12 - Purple Team Exercise
- [ ] P13 - Malware Reverse Engineering
---

## Investigation Checklist Template

Use this for future investigations:

```markdown
# [Case ID] - [Title]

## Quick Facts
- **Platform:** [LetsDefend/CyberDefenders/etc]
- **Alert Type:** [Category]
- **Status:** [TP/FP]
- **Severity:** [Level]
- **Time to Resolution:** [Minutes]

## Analysis Files
- [ ] README.md (Executive summary)
- [ ] case-details.md (Full walkthrough)
- [ ] ioc-extraction.md (IOCs)
- [ ] detection-sigma.yml (Detection rules)
- [ ] threat-assessment.md (Impact analysis)
- [ ] resume-bullets.md (Interview prep)
- [ ] Evidence folder (Screenshots, logs)

## Key Achievements
- [ ] Alert triaged
- [ ] Root cause identified
- [ ] IOCs extracted
- [ ] Detection rule created
- [ ] Recommendations documented
- [ ] Case closed
- [ ] Resume bullet prepared
```

---

### Investigation Training Platforms
- **LetsDefend:** Live SOC monitoring labs
- **CyberDefenders:** CTF-style blue team challenges
- **TryHackMe:** SIEM & incident response rooms
- **HackTheBox:** Forensics challenges

### Detection & Threat Intelligence
- **VirusTotal:** Malware analysis & reputation
- **AlienVault OTX:** Open threat intelligence feeds
- **MITRE ATT&CK:** Threat actor tactics mapping
- **GitHub:** Sigma rules & detection sharing

### Documentation
- **NIST Cybersecurity Framework:** Incident response guidance
- **SANS Incident Handler's Handbook:** Investigation procedures
- **OWASP:** Top 10 security risks
- **CIS Controls:** Security best practices

---

**Last Updated:** July 15, 2026  
**Total Hours:** [1h]  
**Career Goal:** [Entry SOC Analyst]

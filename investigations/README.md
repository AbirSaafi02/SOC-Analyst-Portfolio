# SOC Analyst Portfolio - Investigations Index

This folder contains detailed write-ups of security investigations from training platforms (LetsDefend, CyberDefenders, etc.) and practical labs.

Each investigation includes:
- **README.md** - Executive summary
- **case-details.md** - Full investigation walkthrough
- **analysis/** - Technical analysis artifacts
  - `ioc-extraction.md` - Indicators of Compromise
  - `detection-sigma.yml` - Detection rules (YARA, Sigma)
  - `threat-assessment.md` - Impact analysis & recommendations
- **evidence/** - Screenshots and supporting artifacts
- **resume-bullets.md** - 4 versions (Entry → CISO-path)

---

## Investigation Log

| Case ID | Title | Platform | Severity | Status | Date | Duration |
|---------|-------|----------|----------|--------|------|----------|
| SOC282 | Phishing - Deceptive Mail Detected | LetsDefend | Critical | TP ✅ | Aug 30, 2024 | 30 min |

---

## Quick Stats

- **Total Investigations:** 1
- **True Positives:** 1 (100%)
- **False Positives:** 0
- **Average Time to Investigate:** 30 min
- **Total IOCs Extracted:** 5+
- **Detection Rules Created:** 5

---

## Skills Demonstrated

### Email Security
- ✅ Email header parsing
- ✅ Phishing pattern recognition
- ✅ Social engineering analysis
- ✅ SPF/DKIM/DMARC validation

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
- ✅ Detection rule development (Sigma/YARA)
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

## Portfolio Presentation Tips

### For Interviews
1. **Start with SOC282:** It's complete and demonstrates full investigation cycle
2. **Emphasize Methodology:** Show your systematic approach to analysis
3. **Highlight Speed:** 30-minute investigation shows efficiency
4. **Show Depth:** IOC extraction and detection rules show technical skills
5. **Discuss Impact:** Explain how findings prevent future attacks

### For GitHub
1. Create `investigations/` as public portfolio section
2. Keep sensitive data anonymized (real customer data excluded)
3. Add GitHub badges for "Completed Investigations" count
4. Link to Medium write-up for additional credibility
5. Include detection rules for community threat hunting

### For LinkedIn
1. Post individual investigation summaries
2. Highlight specific technical achievements
3. Include metrics (detection rates, time-to-resolution)
4. Link to full documentation in GitHub portfolio
5. Tag relevant security communities

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

## Resources for Continuous Learning

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

## Contribution History

| Date | Investigation | Action |
|------|---|---|
| Jun 17, 2024 | SOC282 | Created complete investigation package |
| TBD | [Next] | TBD |

---

**Last Updated:** June 17, 2024  
**Total Hours:** [Track your investigation hours here]  
**Career Goal:** [Entry SOC Analyst / Mid-level / Senior]

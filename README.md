# SOC Analyst Portfolio 🔐

> **Goal:** Entry-level SOC Analyst role | Following SOC 2026 Roadmap

A hands-on portfolio demonstrating practical security operations skills through completed investigations, threat analysis, and detection engineering.

---

## 📊 Portfolio Overview

### 🔍 Completed Investigations

| Case ID | Title | Platform | Severity | Result | Time |
|---------|-------|----------|----------|--------|------|
| **SOC282** | Phishing Alert - Deceptive Mail Detected | LetsDefend | Critical | ✅ TP | 30 min |

**Investigation Details:** [→ SOC282 Case](investigations/letsdefend-soc282-phishing/)

---

## 🎯 What's Here

### 📁 `investigations/`
Complete case documentation including:
- **Executive summary** - 1-page findings
- **Full walkthrough** - Step-by-step analysis
- **IOC extraction** - Indicators for blocking & hunting
- **Detection rules** - SIGMA, YARA, SIEM queries
- **Threat assessment** - Business impact & recommendations
- **Resume bullets** - Interview-ready achievements (4 levels)

**Why Full Transparency?** Your analysis process is more valuable than hiding it. Top SOC portfolios show:
- ✅ Complete methodology
- ✅ Technical depth
- ✅ Business thinking
- ✅ Communication skills

---

## 💡 Key Skills Demonstrated

### Email & Phishing Analysis
- Email header parsing & authentication validation (SPF, DKIM, DMARC)
- Phishing pattern recognition & social engineering indicators
- Malicious attachment identification & analysis
- Email triage & containment

### Malware & Threat Analysis
- Third-party threat intelligence integration (VirusTotal)
- Malware classification & severity assessment
- IOC extraction & correlation
- Threat actor infrastructure mapping

### Endpoint & Forensics
- Process execution analysis
- Behavioral indicators detection
- Incident containment procedures
- System forensics & preservation

### Incident Response
- Alert triage & prioritization
- Root cause analysis
- Timeline reconstruction
- Cross-functional coordination

### Detection & Threat Hunting
- SIGMA rule development
- YARA signature creation
- SIEM query optimization
- Proactive threat hunting

---

## 📈 Portfolio Metrics

| Metric | Value |
|--------|-------|
| **Investigations Completed** | 1 |
| **True Positives** | 1 (100%) |
| **IOCs Extracted** | 5+ |
| **Detection Rules Created** | 5 |
| **Average Investigation Time** | 30 min |
| **Malware Detection Rate** | 61/75 engines (81%) |

---

## 🚀 Getting Started with This Portfolio

### For Hiring Managers
1. **Quick Read:** Start with [README](investigations/letsdefend-soc282-phishing/README.md) in any investigation
2. **Deep Dive:** Review [case-details.md](investigations/letsdefend-soc282-phishing/case-details.md) for full methodology
3. **Technical Skills:** Check [detection rules](investigations/letsdefend-soc282-phishing/analysis/detection-sigma.yml)
4. **Interview Prep:** See [resume-bullets.md](investigations/letsdefend-soc282-phishing/resume-bullets.md)

### For Security Professionals
- **Learn Investigation Methodology:** See [case-details.md](investigations/letsdefend-soc282-phishing/case-details.md)
- **Review Detection Logic:** [detection-sigma.yml](investigations/letsdefend-soc282-phishing/analysis/detection-sigma.yml)
- **Understand IOCs:** [ioc-extraction.md](investigations/letsdefend-soc282-phishing/analysis/ioc-extraction.md)
- **Threat Hunt:** Use SIEM queries in investigation files

### For Other Learners
- **Phishing Training:** Follow SOC282 case step-by-step
- **Malware Analysis:** Learn VirusTotal + attachment analysis workflow
- **Detection Engineering:** Adapt SIGMA rules for your environment
- **STAR Interview Prep:** Use resume bullets + case details

---

## 📚 Following SOC 2026 Roadmap

This portfolio aligns with the **[SOC-Roadmap-2026](https://github.com/Ak-cybe/soc-roadmap-2026)** by Ak-cybe:

### Foundation Phase (Projects 1-6) 🟢
- ✅ **P1 - Live SOC Monitoring:** Alert triage (SOC282)
- ⏳ **P2 - Phishing Analysis:** Email forensics (In Progress)
- ⏳ **P3 - Incident Response:** SIEM investigation (Planned)
- ⏳ **P4 - Ransomware Forensics:** Advanced analysis (Planned)
- ⏳ **P5 - Threat Hunting:** Hypothesis-driven (Planned)
- ⏳ **P6 - Detection Engineering:** Community rules (Planned)

### Learning Path
**Goal:** Entry-level SOC Analyst (10-12 weeks)
- Platforms: LetsDefend, CyberDefenders, TryHackMe
- Focus: Manual investigation skills before automation
- Target: Resume bullets + portfolio projects

---

## 🛠️ Technical Stack

### Platforms
- **LetsDefend** - Live SOC monitoring & triage
- **VirusTotal** - Malware analysis & reputation
- **SIEM** - Log analysis (Splunk/Elasticsearch queries provided)

### Detection Languages
- **SIGMA** - Generic detection rules
- **YARA** - Malware signature rules
- **Splunk/ELK** - SIEM hunting queries

---

## 📋 Investigation Index

See [investigations/README.md](investigations/README.md) for:
- Complete investigation log
- Skills demonstrated per case
- Future investigation roadmap
- Investigation checklist template

---

## 🤝 Contributing

This is a **learning portfolio**, but contributions welcome:
- 🐛 **Issues?** Report unclear sections or missing details
- 💡 **Ideas?** Suggest additional investigation types
- ✅ **Corrections?** Submit improvements
- 🎓 **Feedback?** Share your own investigation approaches

---

## 📝 Resume Integration

### Beginner Format
```
• Investigated phishing email alert in LetsDefend, 
  confirmed true positive through malware analysis
```

### Mid-Level Format
```
• Completed phishing investigation (SOC282), extracting 5+ IOCs, 
  analyzing malicious executable via VirusTotal (61/75 detection rate), 
  and isolating affected system in 30 minutes
```

### Advanced Format
```
• Led phishing investigation with multi-stage detection pipeline 
  (email metadata → attachment reputation → behavioral endpoint detection). 
  Developed SIGMA detection rules reducing similar attack hunt time by 95%. 
  Prevented estimated 40+ potential compromises through proactive threat hunting.
```

For full interview-ready bullets, see each investigation's `resume-bullets.md`.

---

## 🎓 Certifications Pursuing

- [ ] CompTIA Security+
- [ ] AWS Cloud Practitioner
- [ ] CyberDefenders Blue Team Certifications

---

## 📞 Let's Connect

- **GitHub:** [your-github-profile]
- **LinkedIn:** [your-linkedin-profile]
- **Email:** [your-email]

---

## 📄 License

This portfolio is licensed under the MIT License — see [LICENSE](LICENSE) for details.

✅ Use for personal learning  
✅ Share with others  
✅ Modify and adapt  
✅ Use in portfolios  

---

## 🙏 Acknowledgments

- **SOC 2026 Roadmap:** [Ak-cybe/soc-roadmap-2026](https://github.com/Ak-cybe/soc-roadmap-2026)
- **Investigation Source:** [SOC282 - Sahil Raja](https://medium.com/@sahilrp3/soc282-phishing-alert-deceptive-mail-detected-letsdefend-995254557b44)
- **Threat Intelligence:** VirusTotal, AlienVault OTX, MITRE ATT&CK

---

**Last Updated:** June 17, 2024  
**Status:** 🟢 Active Learning  
**Next Update:** [After next completed investigation]

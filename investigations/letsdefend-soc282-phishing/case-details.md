# SOC282 Investigation: Detailed Case Walkthrough

## Case Timeline

### Step 1: Alert Reception & Case Creation
- **Alert Type:** Phishing - Deceptive Mail Detected
- **Action:** Created case in LetsDefend and initiated Playbook workflow
- **Initial Status:** Unverified

### Step 2: Email Parsing & Analysis
- **Source Address:** [Spoofed sender]
- **Destination:** Felix (Target user)
- **Subject:** [Phishing subject line - e.g., claiming limited-time offer]
- **Initial Assessment:** Suspicious sender with social engineering theme

### Step 3: Artifact Discovery
**Location:** Monitoring → Investigation Channel → Email Security

**Attachment Found:**
- Filename: `free-coffee.zip`
- Password-protected: YES
- Password hint provided: `infected`
- Suspicious indicators:
  - Unexpected attachment for email context
  - Password-protected (obfuscation tactic)
  - Name designed for social engineering ("free" offer)

### Step 4: Malware Analysis (VirusTotal Scan)
- **File Scanned:** `free-coffee.zip` and extracted contents
- **Detection Rate:** 61 out of 75 security vendors
- **Threat Classification:** Backdoor / Remote Access Trojan
- **Severity:** Critical
- **Findings:** Confirmed malicious executable inside archive

**Risk Mitigation Note:** Download and analysis performed in isolated VM environment only.

### Step 5: Delivery Status Verification
- **Module:** Email Security → Device Action
- **Status:** ALLOWED ❌
- **Impact:** Email reached user's inbox
- **Timeline:** Email delivered before alert triggered

### Step 6: Initial Containment - Email Removal
- **Action:** Deleted email from user's inbox via Email Security tab
- **Goal:** Prevent accidental re-execution
- **Status:** ✅ Completed

### Step 7: Endpoint Compromise Verification
- **Investigation Module:** Endpoint Security
- **Target User:** Felix
- **Analysis:** Process execution logs

**Key Discovery:**
- Process `Coffee.exe` found running
- Matches executable from `free-coffee.zip` archive
- **Conclusion:** User executed the malicious attachment ⚠️

### Step 8: System Isolation (Containment)
- **Action:** Isolated affected user system
- **Methods:** Device quarantine via Endpoint Security
- **Goal:** Prevent lateral movement to other systems
- **Status:** ✅ Isolated

### Step 9: Alert Closure
- **Final Assessment:** True Positive - Confirmed Backdoor Infection
- **Actions Taken:**
  - Email deleted ✅
  - System isolated ✅
  - User notified of compromise ✅
  - Incident documented ✅
- **Recommendations:**
  - System rebuild recommended
  - Credential reset required
  - Network monitoring for C2 communication

---

## Analysis & Assessment

### Attack Chain
```
Phishing Email → Social Engineering ("free coffee")
    ↓
Malicious ZIP Attachment (free-coffee.zip)
    ↓
Password-Protected Backdoor Executable
    ↓
User Extraction & Execution
    ↓
Backdoor Installed (Coffee.exe Process)
    ↓
System Compromised - Isolation Required
```

### Why True Positive?

1. **Confirmed Malicious Attachment:** 61/75 vendors detected as backdoor
2. **Evidence of Execution:** Coffee.exe process confirmed running on user system
3. **Delivery Confirmed:** Email reached inbox (Device Action: Allowed)
4. **Infection Confirmed:** Executable was extracted and executed by user

### Threat Actor Tactics

- **Initial Access:** Phishing email with social engineering
- **Obfuscation:** ZIP file password protection
- **Execution:** Requires user interaction (attachment opening)
- **Persistence:** Backdoor/RAT for remote access
- **Objective:** Likely data theft, lateral movement, or botnet enrollment

---

## Key Insights for SOC Analysts

### What Worked
- ✅ Swift email analysis and attachment identification
- ✅ Automated threat intelligence lookup (VirusTotal)
- ✅ Endpoint visibility to confirm execution
- ✅ Rapid containment response

### Lessons Learned
- ⚠️ User-file-open behavior remains #1 infection vector
- ⚠️ Password-protected archives used to bypass initial scanning
- ⚠️ Time between delivery and detection matters
- ⚠️ Early isolation prevents cascading compromises

### Prevention for Future Incidents
1. Email gateway hardening (block password-protected ZIPs)
2. User awareness training (phishing recognition)
3. Behavioral analytics (detect anomalous processes)
4. Network segmentation (limit lateral movement post-compromise)

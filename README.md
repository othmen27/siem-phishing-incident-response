# Phishing Incident Response – SIEM Project

## Overview
This project simulates detecting and responding to multiple phishing email alerts using a SIEM platform.  
During the investigation, a total of **5 alerts** were observed:  
- Some were classified as **False Positives** (legitimate activity flagged as suspicious).  
- At least one was confirmed as a **True Positive** phishing attempt.  

The project covers the full workflow: detection, classification, analysis of false positives and true positives, and remediation steps.  
This project was made using the website [TryHackMe](https://tryhackme.com/).

## Table of Contents
- [Detection](#step-1-detection)
- [Classification](#step-2-classification)
- [False Positive Analysis](#step-3-false-positive-analysis)
- [True Positive Analysis](#step-4-true-positive-analysis)
- [Remediation](#step-5-remediation)
- [Lessons Learned](#lessons-learned)

### Step 1: Detection
The SIEM triggered an alert for a suspicious email received by a user.

**Indicators Observed:**
- Subject: "Complete your final profile setup"
- Sender: onboarding@hrconnex.thm
- Alert type: Phishing detection
![Detection Screenshot](Screenshots/Screenshot%202025-09-27%20195024.png)

**Outcome:**  
This alert was later identified as a **False Positive** (benign email, no malicious activity).  
Proceeded to [False Positive Analysis](#step-3-false-positive-analysis).

### Step 2: Classification
After detecting the alerts in the SIEM, each alert was analyzed to determine whether it was a **True Positive (TP)** or a **False Positive (FP)**.

**Total Alerts Observed:** 5  
- **True Positives:** 3  
- **False Positives:** 2  

**Classification Process:**
1. **Email Header Analysis**
   - Verified sender domains for legitimacy.

2. **Content Inspection**
   - Reviewed email subject, body, and links.
   - Checked for suspicious or obfuscated URLs.

3. **Threat Intelligence & IOCs**
   - Cross-referenced sender IPs and URLs with known malicious indicators.
   - Confirmed phishing signatures where applicable.

4. **User Interaction**
   - Checked whether recipients clicked links or downloaded attachments.

**Outcome:**
- **False Positives (2 alerts):** Legitimate emails flagged by the SIEM. No malicious content detected.  
- **True Positives (3 alerts):** Confirmed phishing attempts with malicious links or attachments targeting users.

**Next Steps:**  
- Proceed to [False Positive Analysis](#step-3-false-positive-analysis) for the benign alerts.  
- Proceed to [True Positive Analysis](#step-4-true-positive-analysis) for the confirmed phishing attempts.

### Step 3: False Positive Analysis

**Subject:** Complete your final profile setup  
**Sender:** onboarding@hrconnex.thm  

**Why the alert was triggered:**  
- The email contained url like "https://hrconnex.thm/" that matched phishing detection rules.   
- The sender domain was new to the recipient, triggering caution rules.

**Analysis:**  
- Confirmed that links point to the official internal portal.
- Cross-checked with threat intelligence: no IOCs found.

**Screenshots:**

**1. SIEM Alert Overview:**  
Shows the alert triggered for the suspicious email.  
![FP Alert Overview](Screenshots/Screenshot%202025-09-27%20195024.png)

**2. Email Headers / Technical Details:**  
Displays SPF/DKIM/DMARC results and sender information. 
![FP Email Headers](Screenshots/Mail.png)
![Result](Screenshots/result.png)

**Summary Table:**
| Field               | Observation                      |
|--------------------|----------------------------------|
| Subject             | Complete your final profile setup |
| Sender              | onboarding@hrconnex.thm          |
| SPF/DKIM/DMARC      | ✅ Pass                           |
| URLs                 | Internal portal                  |
| Action Required      | None                             |

**Key Takeaway from this False Positive:**  
- Investigate alerts carefully before taking action; not all alerts are threats.

### Step 4: True Positive Analysis
*(To be filled in…)*

### Step 5: Remdiation
*(To be filled in…)*

### Step 6: Lessons Learned
- Always check SPF/DKIM/DMARC headers.
- User awareness is critical.
- Always check domains and sub-domains.
- SIEM tuning reduces false positives.

# Phishing Incident Response – SIEM Project

## Overview
This project simulates detecting and responding to a phishing email using a SIEM platform. 
It covers alert detection, classification, analysis of true positives and false positives, and remediation steps.
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
*(To be filled in…)*

### Step 3: False Positive Analysis
*(To be filled in…)*

### Step 4: True Positive Analysis
*(To be filled in…)*

### Step 5: Remdiation
*(To be filled in…)*

### Step6: Lessons Learned
- Always check SPF/DKIM/DMARC headers.
- User awareness is critical.
- Always check domains and sub-domains.
- SIEM tuning reduces false positives.

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

## Steps
1. [Detection](#step-1-detection) – Alert triggered in SIEM for suspicious email.
2. [Classification](#step-2-classification) – Determine if the alert is True Positive or False Positive.
3. [False Positive Analysis](#step-3-false-positive-analysis) – Investigate alerts that turned out to be harmless.
4. [True Positive Analysis](#step-4-true-positive-analysis) - Confirmed phishing (true positive).
5. [Remediation](#step-5-remediation) - Actions taken to contain and resolve the incident.
## Lessons Learned
- Always check SPF/DKIM/DMARC headers.
- User awareness is critical.
- Always check domains and sub-domains.
- SIEM tuning reduces false positives.
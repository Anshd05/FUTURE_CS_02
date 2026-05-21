# FUTURE_CS_02
Security Analyst-style phishing detection project using email analysis, sender verification, header inspection (SPF/DKIM/DMARC), URL investigation, and awareness reporting to identify and prevent phishing attacks

# Phishing Email Detection & Awareness System

<img width="1024" height="559" alt="image" src="https://github.com/user-attachments/assets/41cffa2b-2547-4b3a-8108-1b5a5ea93743" />

## 📌 Executive Summary

Phishing remains the primary initial access vector for enterprise-level cyber attacks. This repository showcases a comprehensive **Phishing Email Detection & Awareness System** modeled after real-world Security Operations Center (SOC) incident response triage. 

This project simulates how a Security Analyst investigates suspicious emails, performs static message analysis, inspects transport headers, correlates OSINT indicators, and converts raw threat data into digestible employee awareness guidelines. The entire pipeline emphasizes risk mitigation, early containment, and defensive engineering.

## 🎯 Project Objectives

*   **Email Forensics Execution:** Perform deep-dive header analysis to uncover spoofing, relay anomalies, and authentication alignment failures.
*   **Indicator Correlation:** Safely inspect, decode, and investigate suspicious domains and malicious URLs using non-intrusive OSINT utilities.
*   **Triage Automation:** Leverage custom Python scripts to parse elements and expedite initial risk classification.
*   **Corporate Defense & Training:** Translate highly technical forensic findings into high-impact employee awareness blueprints and prevention strategies.

## 🛠️ Tooling & Technical Ecosystem

The analysis and automation framework relies on a combination of enterprise tools and command-line utilities:

<img width="1024" height="559" alt="image" src="https://github.com/user-attachments/assets/91c17250-1082-4074-aa93-a87b5408d02b" />


## 🔍 Core Security Indicators Analyzed

The system evaluates incoming data points against specific forensic vectors to classify threat levels:

### 📨 1. Authentication & Integrity (Header Spoofing)
*   **SPF (Sender Policy Framework):** Verifying if the sending server is authorized by the domain's DNS records.
*   **DKIM (DomainKeys Identified Mail):** Validating the cryptographic signature to ensure message integrity.
*   **DMARC (Domain-based Message Authentication):** Checking policy enforcement alignment (Pass/Softfail/Reject).

### 🔗 2. Infrastructure & Payload Analysis
*   **Domain Reputation:** Inspecting the age, registrar data, and country of origin of the sending domain.
*   **URL Defanging & Inspection:** Decoding obfuscated links, tracking hidden redirects, and analyzing top-level domain (TLD) anomalies.

### ✍️ 3. Behavioral & Linguistic Analysis
*   **Heuristic Flags:** Catching urgency-inducing text patterns, financial/coercive pressure tactics, and generic placeholders in lieu of tailored names.



## 📊 Incident Triage Matrix

Emails are ingested, parsed, and assigned to one of three operational categories based on threat density:
[Ingested Mail] ──► [ Forensics / Header & URL Validation ]
│
├─► Zero Threat Flags ──────────────► [🟢 SAFE]
|
├─► Missing Auth / Out-of-Zone ─────► [🟡 SUSPICIOUS]
|
└─► Failed SPF/DKIM + Urgency Core ─► [🔴 PHISHING]

## 📈 Sample Triage Dashboard (Mock Findings)

<img width="1024" height="559" alt="image" src="https://github.com/user-attachments/assets/90736b50-0cf7-40de-acb7-e043e1ca4c7b" />

**Disclaimer**
This project is constructed exclusively for educational, academic, and enterprise threat awareness development purposes. No interactions with active malicious infrastructure or live command-and-control (C2) servers occurred during this analysis. All sample datasets have been fully sanitized, defanged, and reviewed inside isolated testing environments.

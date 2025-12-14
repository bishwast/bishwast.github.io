---
title: "SIEM Lab and Threat Detection Project"
excerpt: "Designed and deployed a Security Operations Center (SOC) pipeline using Splunk Enterprise and Linux to validate threat detection and incident response capabilities."
collection: portfolio
date: 2025-12-13
categories:
  - Cybersecurity
  - SOC
tags:
  - Splunk
  - SIEM
  - Threat Detection
  - Linux
---

## Project Overview

This project simulates a small-scale SOC environment to demonstrate proficiency in key blue team functions, including log aggregation, query language development (SPL), alert creation, and incident simulation.

### 1. SIEM Infrastructure Deployment
* **Platform:** Splunk Enterprise (Free License) deployed on a virtualized Ubuntu Linux server.
* **Log Ingestion:** Configured Universal Forwarders to collect system logs (syslog, security events) from a Windows Domain Controller and Linux endpoint.
* **Parsing & Indexing:** Created custom sourcetypes and performed initial field extraction to normalize key security data points (e.g., source IP, user, event ID).

### 2. Threat Detection Rule Creation
* **Use Cases:** Focused on common MITRE ATT&CK techniques, specifically brute-force attacks and privilege escalation attempts.
* **SPL Development:** Developed complex Search Processing Language (SPL) queries to create threshold-based alerts (e.g., "5 failed logins within 60 seconds from the same source IP").
* **Visualization:** Built a custom dashboard in Splunk to monitor real-time security events and provide a high-level overview of the environment's security posture.

### 3. Incident Simulation and Validation
* **Simulation:** Utilized Python and Bash scripts to simulate network traffic and logon failures that violate the defined alert thresholds.
* **Validation:** Verified that the Splunk alerts fired correctly and captured the necessary metadata for initial triage, validating the effectiveness of the security controls.
* **Documentation:** Maintained detailed documentation of the architecture, alert logic, and incident response procedures.

---

## Featured Case Study
### [Hybrid SIEM Architecture & Threat Hunting](/2025/12/10/hybrid-siem-architecture.html)
**Tech Stack:** Splunk Enterprise, NVIDIA DGX, Suricata

I designed a hybrid detection pipeline that integrates standard SIEM logging with GPU-accelerated anomaly detection. This project demonstrates advanced "Blue Team" management by reducing Mean Time to Detect (MTTD) for APT lateral movement.

[![Project Screenshot](/images/splunk-arch.png)](/2025/12/10/hybrid-siem-architecture.html)

[**Read the full Case Study →**](/2025/12/10/hybrid-siem-architecture.html)

---

### **[Link to Project Repository on GitHub](https://github.com/bishwast/splunk-siem-lab)**

---
layout: post
title: "Hybrid SIEM Architecture & Threat Hunting"
subtitle: "Detecting APT Lateral Movement with Splunk & Suricata"
tags: [Splunk, Blue Team, Threat Hunting, MITRE ATT&CK]
---

## Project Overview
**Role:** Security Analyst / Detection Engineer  
**Tech Stack:** Splunk Enterprise, Suricata IDS, Fortinet, Sysmon, Windows Server  

In this capstone project, I moved beyond standard "install and configure" labs to simulate a realistic **Security Operations Center (SOC)** environment. Using the **Splunk BOTS (Boss of the SOC)** dataset, I engineered a detection pipeline capable of identifying Advanced Persistent Threats (APTs) across multiple phases of the Cyber Kill Chain.

This project demonstrates my ability to ingest diverse telemetry, correlate network and endpoint logs, and reduce "Mean Time to Detect" (MTTD) for critical incidents.

---

## 1. Architecture & Data Ingestion
A managed SIEM requires more than just system logs. I architected the ingestion pipeline to normalize data from **Network Traffic (Stream)**, **Intrusion Detection Systems (Suricata)**, and **Endpoint Telemetry (Sysmon)**.

![Data Architecture Dashboard](/images/splunk-arch.png)
*Fig 1: Verified ingestion of diverse data sources (Suricata, HTTP Stream, WinEventLog) proving full visibility into the attack surface.*

---

## 2. Incident Timeline Analysis
Management relies on accurate dwell-time metrics. By analyzing the event distribution histogram, I identified the initial breach window occurring in **August 2016**. This capability allows for precise "Time-boxing" during Incident Response, filtering out millions of irrelevant logs to focus on the active breach.

![Attack Timeline](/images/splunk-timeline.jpg)
*Fig 2: Identifying the "Attack Spike" - separating normal baseline traffic from the anomaly.*

---

## 3. Deep Dive & Forensics
Finding the needle in the haystack. I utilized Splunk's Field Extractor to parse raw Fortinet Firewall logs (`fgt_traffic`). In this specific investigation, I traced a **Denied Connection** attempt from a suspicious external IP (Russian Federation) targeting internal assets, validating the effectiveness of the perimeter firewall policies.

![Log Forensics](/images/splunk-details.jpg)
*Fig 3: Granular analysis of Firewall traffic logs including Source IP, Destination Country, and Action taken.*

---

## Key Outcomes
* **Visibility Gaps Closed:** Achieved 100% visibility into network-to-endpoint correlation by integrating Sysmon and Suricata.
* **Detection Engineering:** Mapped 5 distinct attack behaviors (Scanning, Execution, C2) to **MITRE ATT&CK** IDs.
* **Operational Maturity:** Demonstrated the ability to manage high-volume datasets (900k+ events) efficiently.

---
title: "Advanced Hybrid SIEM: Splunk + NVIDIA DGX"
excerpt: "Architected a hybrid SOC pipeline integrating Splunk Enterprise with GPU-accelerated anomaly detection (NVIDIA RAPIDS) to detect APT lateral movement."
collection: portfolio
date: 2024-12-14
categories:
  - Detection Engineering
  - SIEM Architecture
  - Threat Hunting
tags:
  - Splunk
  - NVIDIA DGX
  - Suricata
  - PySpark
---

## 🚨 Project Executive Summary
This capstone project moves beyond standard SIEM deployment to simulate a **Next-Generation SOC**. I designed a hybrid detection pipeline that processes standard telemetry (Sysmon, Zeek) in **Splunk Enterprise** while offloading heavy behavioral analysis to an **NVIDIA DGX** GPU cluster.

**Key Outcome:** Reduced "Mean Time to Detect" (MTTD) for "low-and-slow" C2 beacons by utilizing unsupervised learning (Isolation Forest) on historical network datasets.

---

## 📸 Phase 1: Architecture & Visibility
A managed SIEM requires granular visibility. I architected the ingestion pipeline to normalize data from **Network Traffic (Stream)**, **Intrusion Detection Systems (Suricata)**, and **Endpoint Telemetry (Sysmon)**.

![Data Architecture Dashboard](/images/splunk-arch.png)
*Fig 1: Verified ingestion of diverse data sources (Suricata, HTTP Stream, WinEventLog) proving full visibility into the attack surface.*

---

## 📈 Phase 2: Threat Detection & Incident Timeline
Using the **Splunk BOTS (Boss of the SOC)** dataset, I validated the system's ability to handle high-volume event storms. By analyzing the event distribution histogram, I identified the initial breach window occurring in **August 2016**.

![Attack Timeline](/images/splunk-timeline.jpg)
*Fig 2: Identifying the "Attack Spike" - separating normal baseline traffic from the anomaly.*

---

## 🔍 Phase 3: Deep Dive Forensics
Finding the needle in the haystack. I utilized Splunk's Field Extractor to parse raw Fortinet Firewall logs. In this specific investigation, I traced a **Denied Connection** attempt from a suspicious external IP (Russian Federation) targeting internal assets.

![Log Forensics](/images/splunk-details.jpg)
*Fig 3: Granular analysis of Firewall traffic logs including Source IP, Destination Country, and Action taken.*

---

## 🛠 Technical Implementation Details

### 1. Infrastructure Deployment
* **Platform:** Splunk Enterprise deployed on Ubuntu Linux (Search Head/Indexer).
* **AI Integration:** NVIDIA DGX running Apache Spark (RAPIDS) for anomaly detection jobs.
* **Log Ingestion:** Configured Universal Forwarders to collect system logs from Windows Domain Controllers.

### 2. Detection Logic (SPL)
* **Use Cases:** Mapped 5 distinct attack behaviors (Scanning, Execution, C2) to **MITRE ATT&CK** IDs.
* **Alerting:** Developed custom SPL queries to create threshold-based alerts (e.g., "Process Injection in Temp folders").

### 3. Incident Simulation
* **Validation:** Verified detection efficacy using "Atomic Red Team" scripts to simulate credential dumping.
* **Response:** Maintained detailed documentation of the architecture, alert logic, and incident response procedures.

---

### **[View Source Code on GitHub](https://github.com/bishwast/splunk-siem-lab)**

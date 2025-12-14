---
layout: archive
title: "About Me"
permalink: /
author_profile: true
---

# The Modern Defender

I am a Cybersecurity Management Master’s candidate bridging the gap between traditional Security Operations and modern Data Science. Unlike the standard approach to Blue Teaming, I focus on building high-fidelity detection pipelines that leverage both rule-based SIEM logic and behavioral anomaly detection.

My core research focuses on designing a hybrid security architecture integrating **Splunk Enterprise** with **NVIDIA DGX** infrastructure. This unique setup allows me to simulate enterprise-scale threat hunting scenarios using **Apache Spark** and **RAPIDS**, moving beyond basic alert monitoring to focus on **Detection Engineering**—optimizing how threats are identified, triaged, and mitigated.

I am currently seeking opportunities in **Security Operations (SOC)** or **Detection Engineering** where I can apply data-driven strategies to defend critical infrastructure.

---

### Technical Arsenal

| Domain | Skills & Tools |
| :--- | :--- |
| **SIEM & Observability** | Splunk Enterprise (SPL), Sysmon, Zeek, Log Parsing, CIM |
| **Data & AI** | NVIDIA DGX, Apache Spark (PySpark), Anomaly Detection, NVIDIA RAPIDS |
| **Defense Frameworks** | MITRE ATT&CK, Cyber Kill Chain, NIST CSF |
| **Infrastructure** | Linux (Ubuntu/RHEL), Windows Server, Virtualization, Docker |

---

### 🟡 Current Research Capstone
**Project Title:** Hybrid SIEM Architecture: AI-Driven Threat Detection (Splunk + NVIDIA DGX)
<br>
**Status:** *Active Development / Research Phase*

Traditional SIEM deployments often struggle with "alert fatigue" and the inability to process massive historical datasets in real-time. This project explores a modern solution: offloading heavy anomaly detection to GPU-accelerated infrastructure.

**Key Architectures:**
* **Ingestion:** Pipeline ingests standard security logs (Sysmon/Zeek) into **Splunk Enterprise** for immediate triage.
* **Computation:** High-volume network capture data is routed to an **NVIDIA DGX** environment.
* **Detection:** Using **Apache Spark** and **RAPIDS**, the system applies unsupervised learning models (Isolation Forest) to detect "low-and-slow" beacons that static correlation rules miss.

**Targeted Outcomes:**
* Reduction in False Positives via Risk-Based Alerting (RBA).
* Utilizing GPU acceleration to reduce query time on historical datasets.

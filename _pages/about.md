---
layout: archive
title: "About Me"
permalink: /
author_profile: true
---

# The Autonomous Defender

I am a Cybersecurity Management Master’s candidate specializing in the intersection of **Security Operations (SOC)** and **Applied AI**. My work focuses on moving the industry from passive monitoring to **Autonomous Remediation**, building high-fidelity detection pipelines that leverage local LLMs and hardware-accelerated infrastructure.

My core expertise lies in designing privacy-first security architectures on **NVIDIA DGX (ARM64)** hardware. By integrating **Wazuh SIEM** with local **Llama 3.2** models, I have successfully engineered an end-to-end autonomous SOC loop that detects, analyzes, and mitigates threats—such as brute-force attacks—without cloud dependency or per-token costs.

I am currently seeking opportunities in **Security Operations (SOC)** or **Detection Engineering** where I can apply autonomous, data-driven strategies to defend critical infrastructure.

---

### Technical Arsenal

| Domain | Skills & Tools |
| :--- | :--- |
| **SIEM & Response** | Wazuh (AARCH64), Splunk Enterprise (SPL), Active Response Automation, Iptables |
| **AI & Automation** | Ollama (Llama 3.2), Python 3.12 (PEP 668), Apache Spark, NVIDIA RAPIDS |
| **Detection Engineering** | Custom PCRE2 Decoders, Correlation Rules, MITRE ATT&CK Mapping |
| **Infrastructure** | NVIDIA DGX (ARM64), Linux Network Namespaces, Docker, Virtualization |

---

### 🟢 Featured Project: AI-SOC Analyst (Phase 4)
**Status:** *Full Project Completion (Autonomous Defense Implemented)*

Traditional SOCs suffer from alert fatigue and manual response delays. I have engineered a modern solution: an autonomous security loop that handles the entire incident lifecycle on-premise.



**Core Accomplishments:**
* **Autonomous Remediation:** Developed a Python-based engine that extracts attacker IPs from Wazuh alerts and dynamically updates the Linux kernel firewall (`iptables`) to isolate threats in under 15 seconds.
* **Local LLM Integration:** Integrated **Llama 3.2** via the Ollama API to provide real-time, privacy-compliant executive summaries of security incidents without logs ever leaving the local network.
* **ARM64 Optimization:** Successfully deployed the entire stack natively on **NVIDIA DGX Spark**, bypassing Docker overhead to maximize unified memory performance for high-volume log parsing.

**Project Impact:**
* **Zero-Cost Intelligence:** Eliminated cloud API costs for log summarization.
* **Reduced MTTR:** Achieved near-instant Mean Time to Respond (MTTR) through automated network isolation.
* **Data Sovereignty:** Proved that enterprise-grade AI threat analysis can be performed in 100% air-gapped or restricted environments.
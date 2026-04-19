---
layout: archive
title: "About Me"
permalink: /
author_profile: true
feature_row: feature_row
---
{% include feature_row %}

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
**Status:** Full Project Completion (Autonomous Defense Implemented)

Traditional SOCs suffer from alert fatigue and manual response delays. I have engineered a modern solution: an autonomous security loop that handles the entire incident lifecycle on-premise using Multi-Agent AI Orchestration.

**Technical Milestones:**

* **Multi-Agent Orchestration:** Architected a dual-agent pipeline using CrewAI. A 'Senior SOC Analyst' performs deep reasoning against RAG-based playbooks, while a 'Security Auditor' verifies actions to eliminate false positives and ensure governance.

* **Resilience & Concurrency:** Validated system stability against 'Hydra-style' high-frequency brute-force simulations. Implemented an asynchronous idempotency layer that achieved a 99% latency reduction (from ~30s to <10ms) for recurring threats.

* **Supply Chain Hardening:** Navigated the March 2026 LiteLLM/Pydantic supply chain compromise. Performed environment auditing and version pinning to maintain 100% system integrity during the TeamPCP security incident.

* **Active Response Dispatcher:** Engineered a Python-based engine that extracts attacker context and triggers real-time firewall isolation `(iptables)` and MFA challenges based on AI-audited recommendations.

**Quantifiable Impact:**

* **Instant MTTR:** Reduced Mean Time to Respond (MTTR) to near-zero through automated network isolation.

* **Zero-Cost Intelligence:** Eliminated recurring cloud API costs by hosting the inference layer locally.

* **Hardware Optimization:** Optimized the stack for ARM64 architecture, leveraging unified memory for high-volume neural inference on NVIDIA DGX.

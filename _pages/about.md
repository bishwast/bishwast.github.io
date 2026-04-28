---
layout: archive
title: "About Me"
permalink: /
author_profile: true
feature_row: feature_row
---
{% include feature_row %}

# The Autonomous Defender

I am a Cybersecurity Management Master’s candidate specializing in the intersection of **Security Automation**, **Systems Integration**, and **Agentic AI**. My work focuses on bridging the gap between the cognitive power of generative AI and the strict, deterministic safety required in enterprise security.

My core expertise lies in architecting hybrid-inference pipelines on high-performance infrastructure like the **NVIDIA DGX**. By orchestrating localized edge models (Llama 3.2) alongside cloud intelligence (GPT-4o), I engineer end-to-end autonomous SOC loops that detect, analyze, and mitigate threats without human intervention—safeguarded by strict programmatic governance to prevent AI-driven outages.

I am currently seeking opportunities in **Security Automation**, **Detection Engineering**, or **Systems Integration** where I can apply autonomous, data-driven strategies to defend critical infrastructure.

---

### Technical Arsenal

| Domain | Skills & Tools |
| :--- | :--- |
| **Agentic AI & Orchestration** | CrewAI, LangChain, Hybrid-LLM Inference, Prompt Engineering, Llama 3.2, OpenAI GPT-4o |
| **Security Engineering** | Autonomous Incident Response, Active Defense, SIEM, Forensic Triage, Linux Kernel Networking (`iptables`) |
| **Systems Integration** | Python (FastAPI/Uvicorn), Docker Containerization, Regex Telemetry Pipelines, RESTful APIs |
| **Infrastructure** | NVIDIA DGX (ARM64), Azure (AZ-500 Candidate), Active Directory, PowerShell |

---

### 🟢 Featured Project: Hybrid-LLM Autonomous SOC & Active Defense Framework
**Status:** Architecture Complete & Validated

Traditional SOCs suffer from alert fatigue, while unconstrained "AI Security Agents" present massive operational risks to host infrastructure. I engineered a modern solution: an autonomous security loop that handles the entire incident lifecycle while enforcing strict deterministic governance over AI actions.

**Technical Milestones:**

* **Hybrid-LLM Orchestration:** Architected a multi-agent pipeline utilizing CrewAI. A local 'Senior SOC Analyst' (Llama 3.2) performs privacy-preserving behavioral triage on raw logs, while a 'Security Auditor' (GPT-4o) executes external CVE validation and policy compliance.
* **Ephemeral Telemetry Pipelines:** Integrated isolated Docker honeypots with a custom FastAPI backend, engineering regex-driven Python scripts to dynamically stream attacker IPs from ephemeral containers directly into the cognitive pipeline.
* **Deterministic Active Defense:** Solved the risk of AI-driven Self-Denial-of-Service (DoS) by engineering a hardcoded Python governance layer. This layer intercepts AI actuation commands and evaluates them against critical infrastructure whitelists before execution.
* **Autonomous Actuation:** Achieved zero-intervention threat containment by programmatically triggering dynamic `iptables` drop rules against validated, non-whitelisted malicious endpoints.

**Quantifiable Impact:**

* **Architectural Safety:** Proved that AI can be safely deployed for active network defense by separating cognitive reasoning from programmatic execution.
* **Instant MTTR:** Reduced Mean Time to Respond (MTTR) to near-zero through automated, dynamically governed network isolation.
* **Optimized Systems Integration:** Successfully unified containerized infrastructure, real-time API streaming, and hybrid AI inference into a single, stable deployment on NVIDIA DGX hardware.

[View Technical Repository](https://github.com/bishwast/Agentic-SOC)

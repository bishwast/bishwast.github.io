---
title: "Autonomous Threat Containment & Enforcement (ATCE) Engine"
excerpt: "Developing a deterministic enforcement layer for probabilistic agentic triage on NVIDIA DGX hardware."
header:
  teaser: /images/atce_teaser.png
sidebar:
  - title: "Role"
    text: "Lead Security Architect"
  - title: "Tech Stack"
    text: "Python (FastAPI), CrewAI, Llama 3.2, iptables, Splunk HEC"
---

### Project Overview
Built as the final phase of my MSCM research at the University of Utah, the **ATCE Engine** solves the 'Excessive Agency' problem in AI security. It uses a multi-agent "Chain of Thought" architecture to triage alerts and autonomously execute network containment.

### Key Technical Achievements
* **Dual-Agent Governance:** Implemented a system where a **Security Compliance Auditor** must validate the **SOC Analyst's** reasoning before any action is taken.
* **Policy-702 Heuristic Override:** Designed a fail-safe that identifies critical RCE signatures (CVE-2026-33827) to bypass LLM caution-bias and force immediate containment.
* **Deterministic Actuation:** Engineered a real-time bridge to Linux `iptables`, enabling the system to block malicious IPs in under 30 seconds from ingestion.
* **Recursive Revocation:** Developed an administrative cleanup protocol that purges duplicate firewall rules to maintain network health.

### Deployment Environment
The system is optimized for **NVIDIA DGX Spark** (AARCH64), utilizing local LLM inference via **Ollama** to ensure data sovereignty and low-latency incident response.
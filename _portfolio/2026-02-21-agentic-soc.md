---
title: "Agentic SOC: AI-Driven Incident Response Pipeline"
excerpt: "An automated SOAR pipeline built on NVIDIA DGX (ARM64) hardware using Llama 3.2 and CrewAI to eliminate alert fatigue."
collection: portfolio
---

## 🛡️ Project Overview
This project demonstrates an end-to-end autonomous incident response pipeline that reduces the Mean Time to Respond (MTTR) by performing deep forensics in under 30 seconds. 

### 🏗️ Technical Highlights
* **Agentic OODA Loop**: Automated the 'Observe, Orient, Decide, Act' cycle using **Llama 3.2** via **CrewAI**.
* **Infrastructure**: Ingests telemetry from **Wazuh SIEM** via secure **Tailscale** tunnels to a local **NVIDIA DGX** environment.
* **Engineering Maturity**: Implemented professional **log rotation** (50MB cap) to manage high-volume security data on **ARM64** architecture.
* **Clean Deployments**: Advanced Git history scrubbing to maintain repository efficiency and security.

### 🛠️ Tech Stack
Wazuh | CrewAI | Llama 3.2 | Streamlit | NVIDIA DGX | Azure | Python

---
[View the Repository on GitHub](https://github.com/bishwast/Agentic-SOC)

![Streamlit Dashboard](/images/dashboard_screenshot.png)
![Wazuh Alerts](/images/wazuh_alerts.png)
---
title: "Agentic SOC: Autonomous Incident Response on NVIDIA DGX"
excerpt: "Implementing a fully **Autonomous Agentic SOC** running on on-premise NVIDIA DGX infrastructure"
collection: portfolio
date: 2025-12-28
---

## **Project Overview**
This repository implements a fully **Autonomous Agentic SOC** (Phase 6) running on on-premise NVIDIA DGX infrastructure. The system utilizes a multi-agent AI architecture to ingest SIEM telemetry, perform threat reasoning, and execute response actions without human intervention. 

### **Technical Highlights**

1.  **Ingestion**: A Python-based `File Watcher` monitors `/var/ossec/logs/alerts/alerts.json`.
2.  **Filtering**: Pre-processing logic isolates High Severity alerts (Level ≥ 10).
3.  **Reasoning**: CrewAI orchestrates sequential hand-offs between agents.
4.  **Response**: The Commander generates a finalized JSON report containing the justification and mitigation action.



## **Evidence of Completion**

- Downtime: 0 minutes.

- Data Breach: Prevented.

- System Integrity: Maintained

* **GitHub Repository:** [agentic-soc-arm64](https://github.com/bishwast/Agentic-SOC)
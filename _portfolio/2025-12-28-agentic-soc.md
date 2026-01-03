---
title: "Agentic SOC: Event-Driven Autonomous Response on NVIDIA DGX"
excerpt: "Building an end-to-end Autonomous SOC with Real-time Detection, AI Investigation, and Human-in-the-Loop Governance on ARM64 hardware."
collection: portfolio
date: 2026-01-02
---

## **Project Overview**
This project establishes a fully operational **Agentic Security Operations Center (SOC)** running entirely on-premise using **NVIDIA DGX Spark** infrastructure. Moving beyond simple automation scripts, I architected an **Event-Driven System** that eliminates the latency between detection and response.

The system integrates **Wazuh** (SIEM) for telemetry, **Llama 3.2** (Local AI) for reasoning, and a custom **Streamlit Console** for governance—ensuring 100% data sovereignty with no cloud API dependencies.

---

## **The Architecture (Phase 9)**

The system operates on a military-grade **OODA Loop** (Observe, Orient, Decide, Act) implemented via a decoupled microservices architecture:

| Component | Technology | Role |
| :--- | :--- | :--- |
| **Nervous System** | Python Bridge | A real-time watchdog (`wazuh_bridge.py`) that monitors SIEM logs and triggers the AI instantly upon threat detection. |
| **The Brain** | CrewAI + Llama 3.2 | A multi-agent team (Researcher & Commander) that autonomously enriches data and assesses risk. |
| **The Governance** | Streamlit Dashboard | A "Single Pane of Glass" web console allowing human analysts to authorize AI-proposed blocks (NIST 800-53 Compliance). |

---

## **Technical Highlights**

### **1. Zero-Latency Detection**
I replaced standard polling mechanisms with an **Event-Driven Bridge**. The moment Wazuh detects a brute force attack (Rule ID 5716), the Python bridge intercepts the log stream and deploys the AI agents within milliseconds.

### **2. Autonomous Investigation**
The AI Crew performs tasks that usually take analysts 15-30 minutes:
* **Context:** Extracting Attacker IP and Usernames from JSON logs.
* **Enrichment:** Querying **AbuseIPDB** to validate reputation scores.
* **Decision:** Correlating findings to propose a **BLOCK** or **WATCH** action.

### **3. Human-in-the-Loop Governance**
To solve the "AI hallucinations" risk, I built a dedicated **Analyst Dashboard**. No firewall rule is applied blindly. The AI submits a formal **Request for Change (RFC)**, and the human operator uses the dashboard to approve or reject the action with a single click.

---

## **Evidence of Completion**

### **The Analyst Console**
*Figure 1: The custom dashboard displaying a real-time alert. The AI has analyzed the threat and is awaiting human authorization to execute the block.*

![Analyst Dashboard](images/phase9_dashboard_success.png)

### **Real-Time Detection Bridge**
*Figure 2: The backend bridge instantly detecting a live **Hydra Brute Force Attack** during adversary emulation testing.*

![Bridge Terminal](images/phase8_bridge_success.png)

---

## **Project Resources**

* **GitHub Repository:** [agentic-soc-arm64](https://github.com/bishwast/Agentic-SOC)
* **Technical Report:** [Download Full Architecture PDF](files/Agentic%20Soc%20Model%20Documentation.pdf)


---

## **Impact & Results**

* **Latency:** Reduced Triage & Analysis time from ~20 minutes to **<10 seconds**.
* **Privacy:** Achieved **100% Data Sovereignty** (No sensitive logs sent to Cloud APIs).
* **Reliability:** Successfully handled circular dependency conflicts on **ARM64/AARCH64** architecture.
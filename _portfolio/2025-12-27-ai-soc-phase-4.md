---
title: "AI SOC Analyst: Autonomous Active Response"
excerpt: "Implementing real-time, automated firewall remediation on NVIDIA DGX (ARM64) architecture."
collection: portfolio
date: 2025-12-27
---

## **Project Overview**
This project concludes active detection capability of the AI-SOC Analyst build. I moved the system from passive detection to **autonomous remediation**. 

### **Technical Highlights**

* **Engine:** Wazuh Active Response integrated with a custom Python logic.
* **Remediation:** Dynamic `iptables` DROP rules applied to malicious IPs.
* **Isolation:** Tested via Linux Network Namespaces to simulate external traffic.



## **Evidence of Completion**
The system successfully blocked a Hydra brute-force attack from `10.10.10.2` within 15 seconds.

* **GitHub Repository:** [ai-soc-analyst-arm64](https://github.com/bishwast/ai-soc-analyst-arm64)

* **Technical Report:** [Deep-Dive](https://github.com/bishwast/ai-soc-analyst-arm64/blob/main/ai-soc-analyst/docs/AI-SOC-Analyst-Phase-4.md)

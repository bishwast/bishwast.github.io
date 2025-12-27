---
title: "AI SOC Analyst Phase 4: Autonomous Active Response"
excerpt: "Implementing real-time, automated firewall remediation on NVIDIA DGX (ARM64) architecture."
collection: portfolio
---

## **Project Overview**
This project concludes Phase 4 of the AI-SOC Analyst build. I moved the system from passive detection to **autonomous remediation**. 

### **Technical Highlights**

* **Engine:** Wazuh Active Response integrated with a custom Python logic.
* **Remediation:** Dynamic `iptables` DROP rules applied to malicious IPs.
* **Isolation:** Tested via Linux Network Namespaces to simulate external traffic.



## **Evidence of Completion**
The system successfully blocked a Hydra brute-force attack from `10.10.10.2` within 15 seconds.

* **GitHub Repository:** [ai-soc-analyst-arm64](https://github.com/bishwast/ai-soc-analyst-arm64)
* **Technical Report:** [Phase 4 Deep-Dive](https://github.com/bishwast/ai-soc-analyst-arm64/blob/main/docs/AI-SOC-Analyst-Phase-4.md)


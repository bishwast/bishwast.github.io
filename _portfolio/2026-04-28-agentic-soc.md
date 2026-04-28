# Architecting a Hybrid-LLM Autonomous SOC with Active Defense Governance
*Bridging the gap between generative AI and deterministic enterprise security.*

### **The Challenge: The Danger of Autonomous AI**
As Security Operations Centers (SOCs) attempt to automate incident response, many rely heavily on Large Language Models (LLMs). But giving an AI unconstrained access to execute commands—like altering host firewalls—creates massive risk. 

If an AI hallucinates or misinterprets a threat, it can easily block critical infrastructure, causing a self-inflicted Denial of Service (DoS). For my Master's Capstone project, I set out to solve this by engineering an Autonomous SOC that leverages the reasoning power of AI, bounded by the safety of deterministic code.

### **The Architecture: Hybrid-LLM Orchestration**
To ensure both data privacy and high-level threat intelligence, I designed a hybrid-inference pipeline running on an NVIDIA DGX:

1. **The Honeypot:** A containerized Alpine Linux environment (`victim_ssh`) designed to safely absorb brute-force and CVE exploitation attempts.
2. **The Telemetry Bridge:** A custom Python script using regex to dynamically extract ephemeral attacker IPs from Docker logs and push them to a FastAPI backend.
3. **Local Edge Inference (Llama 3.2):** To maintain data sovereignty, raw SIEM logs are analyzed entirely locally by a "Senior Analyst" agent built with CrewAI, calculating behavioral Aggression Scores.
4. **Cloud Intelligence (GPT-4o):** Complex threat signatures are escalated to a cloud agent equipped with custom search tools to map the attack to known CVEs and advanced persistent threat (APT) groups.

### **The Breakthrough: The Active Defense Governance Layer**
The core innovation of this project wasn't just hooking an LLM to a firewall; it was teaching the system when *not* to fire. 

During early testing, the AI successfully identified an attack but attempted to block the local loopback interface (`127.0.0.1`), severing the host's DNS routing and taking the machine offline. 

To solve this, I engineered a **Deterministic Governance Layer** in Python. Before the AI’s decision reaches the `iptables` execution engine, the Python layer intercepts the command and evaluates it against a hardcoded infrastructure whitelist.

### **The Proof of Work: Single-Shot Execution**
In the final validation test, the pipeline was subjected to a targeted RCE payload from an ephemeral Docker IP. 

![test images1](images/uvicorn_final_sst-1.png)
![test images2](images/uvicorn_final_sst-2.png)

As shown in the execution trace:
* The Local Llama model successfully identified the high-frequency burst.
* The Cloud GPT-4o model validated the RCE signature and approved a `Policy-702` Immediate Block with 97% confidence.
* The Python Governance Layer verified the target IP was safe to block and successfully actuated the `iptables` drop rule, containing the threat with zero human intervention.

### **Business Impact**
This architecture demonstrates that AI can be safely deployed in active network defense. By separating cognitive reasoning (the LLMs) from programmatic execution (the Python governance), enterprises can reduce triage time by 90% without sacrificing infrastructure stability.

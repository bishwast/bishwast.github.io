---
title: "Agentic SOC: High-Concurrency Resilience & Stress Testing"
excerpt: "Validated system performance under 'Hydra-style' brute-force attacks, achieving a 99% latency reduction using local idempotency caching on NVIDIA DGX."
collection: portfolio
date: 2026-04-19
---

## Security Workflow Diagram

```mermaid
graph TD
    A[SIEM Alert] --> B{Cache Check}
    B -- Hit --> C[Return Stored Action]
    B -- Miss --> D[CrewAI: Specialist]
    D --> E[RAG: Playbook Context]
    E --> F[CrewAI: Auditor]
    F --> G{Keyword Check}
    G -- Match --> H[Firewall Log & Block]
    G -- No Match --> I[Manual Review Flag]
    H --> J[Return Response]
    I --> J

    classDef input fill:#1f77b4,color:#fff,stroke:#0d3b66,stroke-width:2px;
    classDef process fill:#2ca02c,color:#fff,stroke:#1b5e20,stroke-width:2px;
    classDef decision fill:#ff7f0e,color:#fff,stroke:#b45309,stroke-width:2px;
    classDef action fill:#d62728,color:#fff,stroke:#7f1d1d,stroke-width:2px;
    classDef output fill:#9467bd,color:#fff,stroke:#4c1d95,stroke-width:2px;

    class A input;
    class B,G decision;
    class C,D,E,F process;
    class H,I action;
    class J output;
```

### Project Milestone: Phase 10 - Resilience Engineering
On April 19, 2026, the Agentic SOC was subjected to high-frequency concurrency testing to simulate an active brute-force scenario.

#### **Technical Deep Dive**
* **Hydra Burst Simulation:** Processed 10 concurrent multi-agent triage requests (20+ LLM instances) on NVIDIA DGX hardware.
* **Latency Optimization:** Implemented an asynchronous caching layer that reduced processing time for recurring threats from ~30s to <10ms.
* **Supply Chain Hardening:** Successfully navigated the March 2026 LiteLLM/Pydantic dependency conflict, ensuring environment integrity during the TeamPCP security incident.

#### **Core Tech Stack**
* **Inference:** Llama 3.2 via Ollama
* **Orchestration:** CrewAI (Analyst & Auditor Agents)
* **Framework:** FastAPI / Async Python 3.12

[View Technical Repository](https://github.com/bishwast/Agentic-SOC)

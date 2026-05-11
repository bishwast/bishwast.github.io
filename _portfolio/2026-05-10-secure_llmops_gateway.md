---
title: "Secure LLMOps Gateway"
excerpt: "Stateless FastAPI DLP Gateway designed to sanitize PII from prompts before local LLM routing on NVIDIA DGX."
collection: portfolio
date: 2026-05-10
---

### Project Title: Secure LLMOps Gateway: Stateless DLP & Local Inference Proxy

#### Project Link: [View GitHub Repo](https://github.com/bishwast/secure-llmops-gateway)

**Description:**
Designed and engineered a production-ready, privacy-preserving security proxy to intercept, sanitize, and audit Generative AI prompt traffic. This gateway implements a Data Loss Prevention (DLP) layer to enforce data-in-motion compliance (supporting PCI-DSS and SOC 2 frameworks) before routing prompt payloads to an air-gapped, local inference engine.

**Key Engineering Achievements:**

    Active Data-in-Motion DLP: Developed high-precision regex engines to automatically detect and redact sensitive PII (Social Security Numbers and Credit Card details) on-the-fly.

    Compliance-Guaranteed Telemetry: Architected SIEM-compliant, single-line JSON logging to stdout. The logs record latency, performance metrics, and transaction UUIDs, while strictly preventing the leakage of raw, unredacted prompts to downstream log collectors.

    Context Preservation & Refusal Mitigation: Overrode standard LLM safety refusal triggers by injecting authoritative system prompt instructions, allowing local Llama 3.2 models to contextually process redacted tags without false-positive safety blocks.

    Hardened Containerization: Package-managed the application using a lightweight Docker multi-stage environment, configured to run as a dedicated non-root system user (appuser UID 10001) to eliminate container breakout risks.

**Tech Stack:** Python, FastAPI, Docker, Ollama (Llama 3.2), Regular Expressions, Uvicorn, Git.
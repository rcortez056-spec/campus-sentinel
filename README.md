# 🛡️ Campus Sentinel

> **Autonomous hazard intake, privacy-first PII redaction, and intelligent dispatch triage powered by Google Gemini and Relevance AI.**

[![Live Demo](https://img.shields.io/badge/Live_Demo-Netlify-00C7B7?style=flat&logo=netlify)](https://campus-sentinel.netlify.app)
[![Engine](https://img.shields.io/badge/AI_Engine-Google_Gemini-8E44AD?style=flat&logo=google)](https://ai.google.dev/)
[![Orchestration](https://img.shields.io/badge/Orchestration-Relevance_AI-3498DB)](https://relevanceai.com/)

---

## ⚡ Problem & Impact

Campus safety reporting often suffers from two major bottlenecks:
1. **Exposure of Sensitive Data:** Unprocessed hazard reports frequently contain Personally Identifiable Information (PII) such as student names, IDs, phone numbers, and private locations.
2. **Delayed Emergency Response:** Manual triage delays time-critical actions for physical hazards, infrastructure leaks, and medical emergencies.

**Campus Sentinel** bridges this gap by deploying an autonomous AI triage layer that strips sensitive PII in real time while structuring raw text into actionable dispatch summaries and severity levels.

---

## ✨ Key Features

* 🔐 **Privacy-First PII Redaction:** Automatically detects and strips names, student IDs, phone numbers, and sensitive contact info before routing data to public logs or dispatch teams.
* 🚦 **Instant Severity Classification:** Dynamically categorizes incoming incidents into **Critical**, **High**, or **Medium** priority tiers.
* 📋 **Dispatch-Ready Summaries:** Generates concise, structured operational summaries ready for campus safety and emergency personnel.
* 🔌 **Decoupled Webhook Architecture:** Built-in modal supporting custom backend endpoints or direct integration with **Relevance AI** agent workflows.
* 🎨 **Executive Operations UI:** Custom glassmorphic dashboard featuring live status badges, interactive sample templates, and processing feedback.

---

## 🛠️ Architecture Flow
### Architecture Flow

* 1. Ingest: Incoming text, dispatch data, and incident logs are captured via the executive UI interface or incoming webhook endpoints.
* 2. Redact & Process: The autonomous triage layer actively strips sensitive PII (names, student IDs, and phone numbers) in real-time before routing.
* 3. Classify & Structure: Incoming hazards and incidents are dynamically categorized into critical, high, or medium priority tiers, turning raw unstructured text into structured dispatch summaries.
* 4. Distribute: Processed data is routed through a decoupled webhook architecture directly to public logs, dispatch teams, or integrated Relevance AI agent workflows.

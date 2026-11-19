

[![Live Demo](https://img.shields.io/badge/Live_Demo-Netlify-00C7B7?style=flat&logo=netlify)](https://campus-sentinel.netlify.app)
[![Engine](https://img.shields.io/badge/AI_Engine-Google_Gemini-8E44AD?style=flat&logo=google)](https://ai.google.dev/)
[![Orchestration](https://img.shields.io/badge/Orchestration-Relevance_AI-3498DB)](https://relevanceai.com/?via=ramon)

---
# Campus Sentinel (Demo)

Hazard report intake and triage demo. Paste a report, and the demo removes personal details, assigns a severity, and writes a dispatch summary.

**Live demo:** https://campus-sentinel.netlify.app

## What the demo does

- Takes a hazard report as typed text or from one of four sample templates.
- Removes personal details (names, student IDs, phone numbers) before showing results. The feed shows which categories were removed, not the values.
- Assigns a severity of Critical, High, or Medium.
- Writes a short dispatch summary you can copy.
- Uses simulated sample reports only. Nothing in the demo is a real incident.

## Built with

- Local rules engine that runs in the browser
- Single HTML file

## Not built yet

- AI model classification (Google Gemini)
- Relevance AI agent integration
- Live delivery of summaries to dispatch teams


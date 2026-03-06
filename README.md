# n8n AI Content Pipeline — Ongoing Project

An automated AI content production pipeline built using **n8n orchestration** and multiple APIs to generate, render, and prepare short-form video content.

This project is being developed as a **real-world automation system** designed to demonstrate API integration, workflow orchestration, and scalable content pipelines.

**Status:** 🚧 Ongoing / Actively Improving

## Documentation

📐 [Architecture](docs/architecture.md)  
📄 Workflow examples coming soon
![Automation](https://img.shields.io/badge/focus-automation-blue)
![APIs](https://img.shields.io/badge/focus-api%20integration-green)
![Workflow](https://img.shields.io/badge/tool-n8n-orange)

---

## Project Goal

Build a scalable pipeline that automatically converts structured content ideas into finished short-form video assets using AI services and render APIs.

The pipeline focuses on:

* automation
* reliability
* API orchestration
* repeatable workflows
* scalable content generation

---

## High Level Workflow

1. Content backlog stored in **Google Sheets**
2. **n8n** orchestrates the pipeline
3. APIs generate script, voiceover, and captions
4. Render API creates final video
5. Metadata (title, hashtags, CTA) is packaged
6. Final assets are prepared for publishing

---

## Architecture

```
Content Backlog (Google Sheets)
          │
          ▼
     n8n Orchestrator
          │
 ┌────────┼─────────┐
 │        │         │
 ▼        ▼         ▼
LLM     TTS       Caption
API     API       Generator
 │        │         │
 └────────┴─────────┘
          │
          ▼
      Render API
          │
          ▼
     Final Video URL
          │
          ▼
 Metadata Packaging
 (title, hashtags, CTA)
```

---

## Tech Stack

* **n8n** – workflow automation
* **LLM APIs** – script generation
* **TTS APIs** – voiceover generation
* **Render API** – automated video composition
* **Google Sheets** – content backlog & metadata
* **SRT captions**
* **JSON payload pipelines**

---

## Current Features

* n8n workflow orchestration
* Google Sheets driven backlog
* automated voiceover generation
* caption generation
* render API integration
* metadata packaging

## Production-minded features

- Run-level tracking with `run_id`
- Idempotency protection to avoid duplicate renders
- Retry and backoff for external API failures
- Structured status lifecycle (`queued` → `generating` → `rendering` → `complete`)
- Error logging to Google Sheets
- Optional notification hooks for Discord / Slack / Email

---

## Roadmap

* [x] Core pipeline architecture
* [x] Render API template structure
* [ ] Retry and failure handling
* [ ] Cost optimization
* [ ] Multi-language pipeline support
* [ ] Automated publishing integration
* [ ] Analytics tracking

---

## Repository Structure (Planned)

```
docs/
    architecture.md
    setup-notes.md

n8n/
    workflow-exports/

examples/
    render-payload.example.json

scripts/
    helpers/
```

---

## Security

API keys and tokens are **never stored in this repository**.

All credentials are expected to be configured through:

* n8n credential manager
* environment variables
* secret managers

- Do not commit secrets. Use `.env` and your secret manager.
- Rotate any credential immediately if it is exposed.

---

## Why This Project Exists

This project demonstrates practical skills in:

* automation engineering
* API integration
* system orchestration
* scalable workflow design
* production-minded automation

---

## Author

Parker Bakken
GitHub: https://github.com/Parker-Bakken

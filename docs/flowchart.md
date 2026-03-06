# Architecture Overview

```mermaid
flowchart TD
  A[Content Backlog (Google Sheets)] --> B[n8n Orchestrator]
  B --> C[Script Generation API (LLM)]
  B --> D[Voiceover API (TTS)]
  B --> E[Captioning (SRT)]
  C --> F[Render API Template]
  D --> F
  E --> F
  F --> G[Final Video URL]
  B --> H[Metadata Packaging (Title/Hashtags/CTA)]
  G --> I[Publish/Upload Stage (manual or future automation)]
  B --> J[Logs + Error Handling + Retries]

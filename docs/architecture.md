# System Architecture

The pipeline uses **n8n as the orchestration layer** to coordinate multiple API services involved in automated content creation.

```mermaid
flowchart TD

A[Google Sheets Content Backlog]
B[n8n Orchestrator]
C[Script Generation API]
D[Voiceover API]
E[Caption Generator]
F[Render API Template]
G[Final Video Output]
H[Metadata Packaging]
I[Upload / Publish Stage]
J[Logs + Error Handling]

A --> B
B --> C
B --> D
B --> E

C --> F
D --> F
E --> F

F --> G
B --> H
G --> I

B --> J

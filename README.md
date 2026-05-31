---
title: deep_research.py
app_file: deep_research.py
sdk: gradio
sdk_version: 5.49.1
---

## Agentic Deep Research System  
https://replit.com/@harshithhs004/Agentic-Deep-Research-System

Build an automated “deep research” pipeline that takes a natural-language topic from a user, plans several targeted web searches, runs those searches in parallel, synthesizes a long-form markdown report, and delivers that report by email — with optional tracing and a simple web UI.

flowchart TB
    User[User query] --> UI[Notebook or Gradio UI]
    UI --> RM[ResearchManager]
    RM --> P[Planner Agent]
    P --> Plan[WebSearchPlan]
    Plan --> S1[Search Agent 1]
    Plan --> S2[Search Agent 2]
    Plan --> SN[Search Agent N]
    S1 --> Results[Summaries list]
    S2 --> Results
    SN --> Results
    Results --> W[Writer Agent]
    W --> Report[ReportData]
    Report --> E[Email Agent]
    E --> SG[SendGrid]
    Report --> UI


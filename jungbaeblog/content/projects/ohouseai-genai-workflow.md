---
title: "OHouseAI GenAI Workflow Systematization"
date: 2025-11-15
draft: false
tags: ["industrial", "genai", "langchain", "langgraph", "llm-evaluation", "interior-design", "bucketplace"]
categories: ["Industrial Projects"]
---

## Overview

OHouseAI is an AI-powered interior design generation service at Bucketplace (오늘의집). I led the systematization of the GenAI workflow, modularizing the architecture into a Pipeline Provider + Subgraph pattern using LangGraph. The service reached Korea #8 ranking in the Graphics/Design category.

![OHouseAI Architecture](/blog/images/projects/ohouseai_architecture.png)

## Key Achievements

- **Net Satisfaction Score (NSS)**: +253%
- **Positive-Negative Ratio (PN)**: +205%
- **User Engagement**: Requests per user increased by 2.3x
- **Retention**: Improved from 7% to 14%
- **Latency**: Reduced from 71.7s to 35.7s
- **Model Quality**: Outperformed GPT-IMAGE-1.5 and Gemini Nano (8.3/10 intent reflection, 8.1/10 context preservation)

## Technical Approach

### Pipeline Provider + Subgraph Architecture

Modularized the GenAI workflow into composable components using LangGraph:

- **Pipeline Provider**: Centralized orchestration layer managing the lifecycle of generation requests
- **Subgraph Pattern**: Each generation capability is implemented as an independent subgraph, enabling independent iteration

![OHouseAI Comparison](/blog/images/projects/ohouseai_comparison.png)

### LLM-as-a-Judge Evaluation Pipeline

Built a batch evaluation pipeline for data-driven model selection:

- **Scale**: 4 evaluation rounds x 99 test sets
- **Methodology**: Automated side-by-side comparisons with structured scoring:
  - **Intent Reflection**: How well the output matches the user's design intent
  - **Context Preservation**: How faithfully the output preserves the original context
- **Application**: Used to compare candidate models (including GPT-IMAGE-1.5 and Gemini Nano) for production model selection

![OHouseAI Judge Scores](/blog/images/projects/ohouseai_judge_scores.png)

### Monitoring and Observability

Production monitoring through LangFuse for end-to-end tracing of the generation pipeline.

![OHouseAI Dashboard](/blog/images/projects/ohouseai_dashboard.png)

## Tech Stack

- **Agent/Workflow Framework**: LangChain, LangGraph
- **Observability**: LangFuse
- **Evaluation**: LLM-as-a-Judge
- **Architecture Pattern**: Pipeline Provider + Subgraph

## Period

July 2025 - November 2025 | Bucketplace (오늘의집)

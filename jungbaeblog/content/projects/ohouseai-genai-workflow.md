---
title: "OHouseAI GenAI Workflow Systematization"
date: 2025-11-15
draft: false
tags: ["industrial", "genai", "langchain", "langgraph", "llm-evaluation", "interior-design", "bucketplace"]
categories: ["Industrial Projects"]
---

## Overview

OHouseAI is an AI-powered interior design generation service at Bucketplace (오늘의집) that enables users to reimagine their living spaces through generative AI. I led the systematization of the GenAI workflow, modularizing the architecture into a Pipeline Provider + Subgraph pattern using LangGraph. This restructuring delivered dramatic improvements across all key service metrics and positioned OHouseAI to reach **Korea #8 ranking in the Graphics/Design category**.

![OHouseAI Architecture](/blog/images/projects/ohouseai_architecture.png)

## Key Achievements

- **Net Satisfaction Score (NSS)**: +253% improvement
- **Positive-Negative Ratio (PN)**: +205% improvement
- **User Engagement**: Requests per user increased by 2.3x
- **Retention**: Improved from 7% to 14% (doubled)
- **Latency**: Reduced from 71.7 seconds to 35.7 seconds (50% reduction)
- **Model Quality**: Outperformed GPT-IMAGE-1.5 and Gemini Nano with scores of 8.3/10 on intent reflection and 8.1/10 on context preservation
- **App Ranking**: Korea #8 in Graphics/Design category

## Technical Approach

### Pipeline Provider + Subgraph Architecture

The core architectural innovation was decomposing the monolithic generation pipeline into modular, composable components:

- **Pipeline Provider**: A centralized orchestration layer that manages the lifecycle of generation requests, routing them through appropriate subgraphs based on user intent and input modality
- **Subgraph Pattern**: Each generation capability (style transfer, room redesign, furniture placement) is implemented as an independent LangGraph subgraph, enabling independent iteration and A/B testing

![OHouseAI Comparison](/blog/images/projects/ohouseai_comparison.png)

### LLM-as-a-Judge Evaluation Pipeline

To enable data-driven model selection and quality assurance, I built a comprehensive batch evaluation pipeline:

- **Scale**: 4 evaluation rounds, each covering 99 test sets
- **Methodology**: Automated side-by-side comparisons with structured scoring across two primary dimensions:
  - **Intent Reflection**: How well the generated output matches the user's stated design intent
  - **Context Preservation**: How faithfully the output preserves the original room context and constraints
- **Application**: Used to systematically compare candidate models (including GPT-IMAGE-1.5 and Gemini Nano) and select the best-performing configuration for production deployment

![OHouseAI Judge Scores](/blog/images/projects/ohouseai_judge_scores.png)

### Monitoring and Observability

Production monitoring through LangFuse provided end-to-end tracing of the generation pipeline, enabling rapid identification of quality degradation and latency bottlenecks.

![OHouseAI Dashboard](/blog/images/projects/ohouseai_dashboard.png)

## Tech Stack

- **Agent/Workflow Framework**: LangChain, LangGraph
- **Observability**: LangFuse
- **Evaluation**: LLM-as-a-Judge, Batch Evaluation Pipeline
- **Architecture Pattern**: Pipeline Provider + Subgraph

## Impact

The systematization of OHouseAI's GenAI workflow transformed it from a prototype-quality service into a production-grade platform. Doubling retention and more than tripling user satisfaction scores validated the architectural approach. The LLM-as-a-Judge evaluation pipeline established a repeatable, data-driven process for model selection that eliminates subjective decision-making and enables continuous quality improvement. The 50% latency reduction directly improved user experience, contributing to the strong app store ranking.

## Period

July 2025 - November 2025 | Bucketplace (오늘의집)

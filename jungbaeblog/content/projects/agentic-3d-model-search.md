---
title: "Agentic Compositional Multimodal Natural Language 3D Model Search"
date: 2026-01-15
draft: false
tags: ["industrial", "agentic-ai", "langgraph", "multimodal-retrieval", "3d-search", "bucketplace", "a2a"]
categories: ["Industrial Projects"]
---

## Overview

At Bucketplace (오늘의집), I am building an AI-powered search agent that interprets natural language queries and translates them into structured retrieval signals for Room Planner 3D products. The system decomposes free-form user intent into actionable dimensions -- category, attributes, color, dimensions, and budget -- via LLM reasoning, then executes BM25+KNN hybrid search on ElasticSearch to surface the most relevant 3D product models.

At the core of this project is **CoI-Fit (Context-Intent Fit Matching)**, a compositional multimodal retrieval framework I designed to serve as the retrieval backbone for multiple downstream agents. CoI-Fit combines space analysis, mood/style interpretation, dimensional constraints, and conversational context drawn from image, text, and 3D coordinate inputs to produce contextually grounded retrieval results.

## Key Achievements

- **Compositional Retrieval Framework**: Designed CoI-Fit, a novel multimodal retrieval architecture that fuses heterogeneous signals (visual, textual, spatial) into a unified retrieval pipeline
- **Multi-Agent Architecture**: Architected a LangGraph pipeline with parallel fan-out inference, enabling concurrent processing of multiple retrieval dimensions
- **Auto Quality Recovery**: Implemented intelligent filter relaxation retry mechanisms that automatically recover from overly restrictive queries, ensuring high recall even for long-tail searches
- **Dual Interface Design**: Built both A2A (Agent-to-Agent) JSON-RPC and REST/FastAPI interfaces, enabling seamless integration with both agent ecosystems and traditional service architectures
- **Evaluation Pipeline**: Developed a persona-based evaluation pipeline that generates synthetic query-document sets to evaluate retrieval relevance across long-tail distributions, ensuring robust performance on rare and complex queries

## Technical Approach

The system follows a multi-stage agentic pipeline:

1. **Query Understanding**: An LLM-based agent parses natural language queries into structured retrieval signals, identifying product category, visual attributes, color preferences, spatial dimensions, and budget constraints.

2. **Compositional Multimodal Retrieval (CoI-Fit)**: The retrieval backbone combines four signal types:
   - **Space Analysis**: Understanding the room context and spatial arrangement from 3D coordinates
   - **Mood/Style Matching**: Extracting aesthetic intent from text and image inputs
   - **Dimensional Constraints**: Filtering by physical size requirements derived from the 3D scene
   - **Conversational Context**: Maintaining coherent retrieval across multi-turn interactions

3. **Hybrid Search Execution**: BM25 lexical search combined with KNN vector search on ElasticSearch, with dynamic weight balancing based on query characteristics.

4. **Parallel Fan-Out Architecture**: LangGraph orchestrates parallel inference across multiple retrieval dimensions, with results aggregated through a scoring and ranking layer.

5. **Quality Assurance**: Auto-recovery via filter relaxation retry ensures that overly specific queries gracefully degrade to broader matches rather than returning empty results.

## Tech Stack

- **Agent Framework**: LangGraph, A2A (Agent-to-Agent Protocol), ADK (Agent Development Kit)
- **Observability**: LangFuse
- **Search Infrastructure**: ElasticSearch (BM25 + KNN hybrid)
- **Orchestration**: Airflow
- **Model Serving**: Triton Inference Server
- **API**: FastAPI, JSON-RPC
- **Models**: Vision-Language Models (VLM), Multimodal Retrieval Models

## Impact

This project establishes a foundational retrieval layer for the Room Planner ecosystem at Bucketplace. By serving as the retrieval backbone for multiple downstream agents, CoI-Fit enables a new class of AI-powered interior design experiences where users can describe what they want in natural language -- referencing images, spatial constraints, and stylistic preferences -- and receive precisely matched 3D product recommendations. The dual A2A/REST interface ensures the system integrates cleanly into both the emerging agent-to-agent ecosystem and existing microservice infrastructure.

## Period

January 2026 - Current | Bucketplace (오늘의집)

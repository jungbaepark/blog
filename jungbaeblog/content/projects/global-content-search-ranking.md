---
title: "Global Content Search Ranking System"
date: 2023-09-15
draft: false
tags: ["industrial", "search-ranking", "elasticsearch", "content-ranking", "bucketplace"]
categories: ["Industrial Projects"]
---

## Overview

At **Bucketplace (오늘의집)**, built a two-stage content ranking system for 3 content types with time decay and a global language analyzer, served via Redis caching.

## Key Achievements

- Built two-stage ranking pipeline (candidate retrieval + function-score reranking) for 3 content types
- Integrated time decay into ranking
- Implemented a global language analyzer for search quality
- Redis-cached serving for low-latency responses

## Technical Approach

- **Stage 1 - Candidate Retrieval**: ElasticSearch queries with a global language analyzer to produce an initial candidate set
- **Stage 2 - Function-Score Reranking**: Reranking candidates using ElasticSearch function-score queries with time decay
- **Serving**: Results cached in Redis

## Tech Stack

- **Search Engine**: ElasticSearch
- **Orchestration**: Airflow
- **Backend**: Go Server
- **Caching**: Redis

## Period

July 2023 - September 2023 | Bucketplace (오늘의집)

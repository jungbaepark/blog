---
title: "Global Content Search Ranking System"
date: 2023-09-15
draft: false
tags: ["industrial", "search-ranking", "elasticsearch", "content-ranking", "bucketplace"]
categories: ["Industrial Projects"]
---

## Overview

At Bucketplace (오늘의집), I built a two-stage content ranking system to power search across the platform's global content surfaces. The system handles three distinct content types, each with its own relevance signals and ranking requirements, unified under a single retrieval and reranking architecture. A global language analyzer ensures consistent search quality across different languages, while time decay mechanisms keep results fresh and relevant.

## Key Achievements

- **Multi-Content-Type Support**: Designed and shipped ranking pipelines for 3 distinct content types within a unified architecture
- **Two-Stage Ranking**: Implemented candidate retrieval followed by function-score reranking for precision at scale
- **Global Language Support**: Built a global language analyzer enabling consistent search quality across multiple languages
- **Time Decay Integration**: Incorporated temporal decay functions to balance relevance with content freshness
- **Low-Latency Serving**: Redis-cached serving layer ensures fast response times for end users

## Technical Approach

### Two-Stage Ranking Architecture

The system follows a classic two-stage information retrieval pattern optimized for content search:

**Stage 1 -- Candidate Retrieval**: ElasticSearch queries with the global language analyzer produce an initial candidate set. The language analyzer handles tokenization, stemming, and normalization across multiple languages, ensuring that queries in any supported language retrieve relevant content regardless of the original content language.

**Stage 2 -- Function-Score Reranking**: Candidates from the first stage are reranked using ElasticSearch function-score queries that combine multiple signals:
- **Text Relevance**: BM25 scores from the retrieval stage
- **Time Decay**: Gaussian or exponential decay functions that down-weight older content, tuned per content type to reflect different freshness requirements
- **Content-Type-Specific Signals**: Engagement metrics, quality scores, and other signals specific to each of the three content types

### Serving Architecture

The ranking results are cached in Redis to minimize latency for repeated and popular queries. The cache strategy balances freshness (invalidation on new content) with performance (high cache hit rates for common queries).

## Tech Stack

- **Search Engine**: ElasticSearch (retrieval + function-score reranking)
- **Orchestration**: Airflow (index management, data pipelines)
- **Backend**: Go Server
- **Caching**: Redis

## Impact

The global content search ranking system provided Bucketplace users with a unified, high-quality search experience across all content types on the platform. The two-stage architecture balanced the need for broad recall (retrieving all potentially relevant content) with precise ranking (surfacing the most relevant and fresh results at the top). The global language analyzer was particularly important for supporting the platform's international expansion, ensuring that search quality remained consistent as new markets were added.

## Period

July 2023 - September 2023 | Bucketplace (오늘의집)

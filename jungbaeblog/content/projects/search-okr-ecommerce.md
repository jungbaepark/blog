---
title: "Search OKR: E-commerce Deals / Price 2.0 Ranking Optimization"
date: 2025-06-15
draft: false
tags: ["industrial", "search-ranking", "a-b-testing", "e-commerce", "automl", "bucketplace"]
categories: ["Industrial Projects"]
---

## Overview

At Bucketplace (오늘의집), I drove measurable OKR impact through a series of production search ranking experiments focused on optimizing deal and price-based ranking for e-commerce surfaces. The project encompassed end-to-end delivery from PRD and Design Doc authorship through DAG development to production rollout, establishing a reusable experimentation foundation that the team continues to build upon.

![Search Ranking Experimentation](/images/projects/page9_img1.png)

## Key Achievements

### STORE Search Result Page (SRP) -- Deals Ranking
- **Buyer Conversion**: +1.99%
- **Click Conversion**: +0.83%
- **Special-Offer Exposure**: +7.35%

### Category Product List Page (PLP) -- Price 2.0 Ranking
- **Buyer Conversion**: +11.17%
- **Click Conversion**: +5.87%
- **Product Exposure**: +27.9%

### Experimentation Track Record
- **4 total production experiments** conducted
- **3 winners** shipped to production (75% win rate)

## Technical Approach

### Experimentation Infrastructure

The project established a reusable pipeline for rapid experimentation on search ranking:

1. **Query Feature Table**: A centralized feature store capturing query-level signals (search volume, category distribution, deal availability, price sensitivity indicators) computed via Airflow DAGs and served through Redis for low-latency access.

2. **Feature Serving Pipeline**: Query Feature Table data flows through Redis into the ranking server, enabling real-time feature lookup during search request processing without adding significant latency to the search path.

![Feature Pipeline Architecture](/images/projects/page17_img1.png)

### End-to-End Delivery Process

Each experiment followed a rigorous process:
- **PRD / Design Doc**: Formal specification of the hypothesis, expected impact, and rollback criteria
- **DAG Development**: Airflow DAGs for feature computation, model training, and data pipeline orchestration
- **Production Rollout**: Staged deployment with A/B testing framework integration

![Experiment Results](/images/projects/page24_img1.png)

### Hyperparameter Optimization

I developed a specialized Grid Search HPO approach for ranking parameter tuning, complemented by more advanced techniques:

- **Bayesian Optimization**: For efficient exploration of high-dimensional parameter spaces
- **Optuna**: For structured hyperparameter search with pruning
- **Ray Tune**: For distributed hyperparameter optimization at scale

![HPO Results](/images/projects/page26_img1.png)

## Tech Stack

- **Feature Store**: Redis (serving), Query Feature Table (computation)
- **Orchestration**: Airflow DAGs
- **Search Engine**: ElasticSearch
- **AutoML/HPO**: Grid Search, Optuna, Ray Tune, Bayesian Optimization
- **Experimentation**: A/B Testing Framework

## Impact

This project demonstrated the value of systematic experimentation infrastructure for search ranking. The +11.17% buyer conversion improvement on Category PLP alone represents significant revenue impact for the e-commerce platform. More importantly, the reusable experimentation foundation (Query Feature Table, Redis serving pipeline, DAG templates) reduced the marginal cost of running subsequent experiments, enabling the team to iterate faster on ranking improvements. The 75% experiment win rate reflects the effectiveness of the data-driven approach to hypothesis generation and parameter tuning.

## Period

February 2025 - June 2025 | Bucketplace (오늘의집)

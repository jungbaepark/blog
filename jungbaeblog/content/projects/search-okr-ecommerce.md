---
title: "Search OKR: E-commerce Deals / Price 2.0 Ranking Optimization"
date: 2025-06-15
draft: false
tags: ["industrial", "search-ranking", "a-b-testing", "e-commerce", "automl", "bucketplace"]
categories: ["Industrial Projects"]
summary: "Delivered measurable search ranking OKR impact at Bucketplace through 4 production A/B experiments (3 winners shipped), achieving +11.17% buyer conversion on category pages and +7.35% deals exposure on store search."
weight: 5
cover:
  image: "/blog/images/projects/search_okr_results-2.png"
  alt: "A/B Test Results for Search OKR Experiments"
  hidden: false
  hiddenInList: false
---

## Overview

At Bucketplace, I delivered measurable OKR impact through production experiments by establishing a reusable experimentation foundation (Query Feature Table, Redis, Server) and shipping end-to-end from PRD/Design Doc through DAG development to production rollout.

## Key Achievements

### STORE Search Result Page (SRP) -- Deals Ranking
- **Buyer Conversion**: +1.99%
- **Click Conversion**: +0.83%
- **Special-Offer Exposure**: +7.35%

### Category Product List Page (PLP) -- Price 2.0 Ranking
- **Buyer Conversion**: +11.17%
- **Click Conversion**: +5.87%
- **Exposure**: +27.9%

### Experimentation Track Record
- **4 total production experiments** conducted
- **3 winners** shipped to production
- Minimal side effects observed

## Technical Approach

### Experimentation Infrastructure

The project established a reusable experimentation foundation:

- **Query Feature Table**: Computed via Airflow DAGs and served through Redis for low-latency access during search request processing.
- **Feature Serving Pipeline**: Query Feature Table flows through Redis into the ranking server.

### End-to-End Delivery Process

Each experiment followed the full delivery lifecycle:
- **PRD / Design Doc** authorship
- **DAG Development** via Airflow
- **Production Rollout**

![A/B Test Results](/blog/images/projects/search_okr_results-2.png)

### Hyperparameter Optimization

Developed specialized Grid Search HPO for ranking parameter tuning, with additional tooling from Optuna and Ray Tune. Integrated with the MOHPER framework for multi-objective optimization across CTR, CVR, and exposure metrics.

## Tech Stack

- **Feature Serving**: Redis, Query Feature Table, Feature-Serving-API
- **Orchestration**: Airflow DAGs
- **Search Engine**: ElasticSearch
- **HPO**: Grid Search, Optuna, Ray Tune, MOHPER
- **Data Processing**: PySpark, Athena

## Period

February 2025 - June 2025 | Bucketplace (오늘의집)

---
title: "Search OKR: E-commerce Deals / Price 2.0 Ranking Optimization"
date: 2025-06-15
draft: false
tags: ["industrial", "search-ranking", "a-b-testing", "e-commerce", "automl", "bucketplace"]
categories: ["Industrial Projects"]
---

## Overview

At Bucketplace, I delivered measurable OKR impact through production experiments by establishing a reusable experimentation foundation (Query Feature Table, Redis, Server) and shipping end-to-end from PRD/Design Doc through DAG development to production rollout.

![Search Ranking Experimentation](/blog/images/projects/page9_img1.png)

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

![Feature Pipeline Architecture](/blog/images/projects/page17_img1.png)

### End-to-End Delivery Process

Each experiment followed the full delivery lifecycle:
- **PRD / Design Doc** authorship
- **DAG Development** via Airflow
- **Production Rollout**

![Experiment Results](/blog/images/projects/page24_img1.png)

### Hyperparameter Optimization

Developed specialized Grid Search HPO for ranking parameter tuning, with additional tooling from Optuna and Ray Tune.

![HPO Results](/blog/images/projects/page26_img1.png)

## Tech Stack

- **Feature Serving**: Redis, Query Feature Table
- **Orchestration**: Airflow DAGs
- **Search Engine**: ElasticSearch
- **HPO**: Grid Search, Optuna, Ray Tune

## Period

February 2025 - June 2025 | Bucketplace (오늘의집)

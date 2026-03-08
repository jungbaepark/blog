---
title: "Multi-Objective Model Hyperparameter Optimization for E-commerce Search"
date: 2025-01-15
draft: false
tags: ["industrial", "automl", "optimization", "published", "bucketplace", "cikm"]
categories: ["Industrial Projects"]
---

## Overview

At **Bucketplace (오늘의집)**, developed MOHPER, a multi-objective model hyperparameter optimization framework designed specifically for e-commerce retrieval systems. This project tackles the challenge of optimizing multiple business metrics simultaneously (CTR, CVR) without harming other guardrail metrics.

## Key Achievements

- **Publication**: Accepted to **CIKM'25 Applied Science Track (Oral)**
- **Patent**: Patent application filed
- **Production Impact**: Launched tuned parameters **5+ times** on Search Result Page (SERP) and **3+ times** on Category Product List Page (CPLP)
- **Business Metrics**: Each A/B test targeted either CTR or CVR improvements without degrading other metrics
- **Domain Expansion**: Framework expanded into the **AD domain** and adopted as common stack for the **Search Team**

## Technical Approach

E-commerce ranking systems need to balance multiple objectives simultaneously:
- Click-Through Rate (CTR)
- Conversion Rate (CVR)
- User engagement metrics
- Business constraints (guardrails)

Traditional single-objective optimization often improves one metric while degrading others. MOHPER solves this through multi-objective Bayesian optimization, leveraging Optuna and Ray Tune to efficiently explore the hyperparameter space while respecting guardrail constraints.

## Tech Stack

- **AutoML**: Optuna, Ray Tune
- **Optimization**: Bayesian Optimization, Evolutionary Strategies (ES)
- **Search**: ElasticSearch
- **Configuration**: Hydra-core
- **Infrastructure**: E-commerce search stack

## Period

October 2023 - January 2025

## Impact

The framework has become a critical tool for the Search Team, enabling data-driven optimization of ranking systems across multiple product surfaces and business domains. Its adoption as a common stack and expansion into the AD domain demonstrates its versatility and value.

## Publications

- Accepted to **CIKM'25 Applied Science Track (Oral Presentation)**

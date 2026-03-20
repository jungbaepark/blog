---
title: "Multi-Objective Model Hyperparameter Optimization for E-commerce Search"
date: 2025-01-15
draft: false
tags: ["industrial", "automl", "optimization", "published", "bucketplace", "cikm"]
categories: ["Industrial Projects"]
summary: "Built a multi-objective hyperparameter optimization framework for e-commerce search at Bucketplace, launching tuned parameters 5x+ on SERP and 3x+ on CPLP for CTR/CVR gains. Accepted to CIKM'25 Applied Research Track."
weight: 5
cover:
  image: "/blog/images/projects/mohper_architecture-3.png"
  alt: "MOHPER Framework Architecture (Figure 1, CIKM Paper)"
  hidden: false
  hiddenInList: false
---

## Overview

At **Bucketplace (오늘의집)**, increased iteration velocity and production tuning coverage by launching tuned parameters on SERP and CPLP, targeting CTR/CVR improvements without harming other metrics.

## Key Achievements

- **Publication**: Accepted to **CIKM'25 Applied Research Track** (DOI: 10.1145/3746252.3761496)
- **Patent**: Patent applied
- **Production Impact**: Launched tuned parameters >5x on SERP and >3x on CPLP
- **Online A/B Results**: SERP CTR **+0.95%**, Click/Query **+1.23%**; CPLP CTCVR **+1.10%**, Purchase/Query **+1.62%**
- **Domain Expansion**: Expanded into the AD domain and adopted as common Search Team stack

## Technical Approach

### Framework Architecture

MOHPER is a multi-objective hyperparameter optimization framework that automatically tunes ElasticSearch ranking parameters while balancing multiple business metrics simultaneously.

![MOHPER Module Architecture](/blog/images/projects/bp_mohper_module.png)

### Core Components

1. **Multi-Objective Optimization**: Bayesian optimization with Optuna/Ray Tune, jointly optimizing CTR, CVR, and other metrics to avoid "whack-a-mole" metric trade-offs
2. **Transform Functions**: Custom conversion functions mapping raw signals to ranking scores, enabling fine-grained control over how features influence search ranking
3. **Safety Guardrails**: Each optimization run ensures no significant degradation in non-target metrics before promotion to production

![Transform Function Design](/blog/images/projects/bp_mohper_transform_function.png)

### Algorithm Flow

The optimization loop follows:
1. Sample hyperparameter configuration via Bayesian optimization
2. Construct ElasticSearch QueryDSL with sampled parameters
3. Evaluate against offline metrics (simulated click/purchase)
4. Update surrogate model and propose next configuration
5. Promote best configuration to online A/B test

![MOHPER Algorithm](/blog/images/projects/bp_mohper_algorithm.png)

### Production Deployment

- Launched tuned parameters **>5x on SERP** and **>3x on CPLP**
- Each optimization targeted CTR/CVR improvements while ensuring other metrics were not harmed
- Expanded the framework into the AD domain and integrated it as common stack for the Search Team
- Nominated for Bucketplace Engineering Awards

![AutoML Integration Overview](/blog/images/projects/bp_mohper_automl.png)

![Transform Function and Conversion Funnel](/blog/images/projects/mohper_details-4.png)

## Tech Stack

- **AutoML**: Optuna, Ray Tune
- **Optimization**: Bayesian Optimization, Multi-Objective (Pareto)
- **Search**: ElasticSearch QueryDSL
- **Configuration**: Hydra-core
- **Orchestration**: Airflow, Katib
- **Evaluation**: Offline simulation + Online A/B testing

## Period

October 2023 - January 2025 | Bucketplace (오늘의집)

## Publications

- Jungbae Park, Heonseok Jang - "MOHPER: Multi-objective Hyperparameter Optimization Framework for E-commerce Retrieval System" (CIKM 2025, Applied Research Track; arXiv:2503.05227; DOI: 10.1145/3746252.3761496)

## Talks

- **CIKM 2025**: Oral presentation at the Applied Research Track
- **Bucketplace Internal**: "AutoML for Retrieval (ElasticSearch) System Tutorials" (2024.10.24)

![MOHPER Paper Abstract](/blog/images/projects/bp_mohper_abstract.png)

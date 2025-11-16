---
title: "⚙️ MOHPER: Multi-Objective Hyperparameter Optimization for E-commerce"
date: 2025-01-15
draft: false
tags: ["industrial", "automl", "optimization", "published", "bucketplace", "cikm"]
categories: ["Industrial Projects"]
---

## Overview

MOHPER is a multi-objective hyperparameter optimization framework designed specifically for e-commerce retrieval systems. This project tackles the challenge of optimizing multiple business metrics simultaneously (CTR, CVR) without harming other guardrail metrics.

## Key Achievements

- **Production Impact**: Launched tuned parameters **5+ times** on Search Result Page (SERP) and **3+ times** on Category Product List Page (CPLP)
- **Business Metrics**: Each A/B test targeted either CTR or CVR improvements without degrading other metrics
- **Publication**: Accepted to **CIKM'25 Applied Science Track** (top conference on information retrieval)
- **Patent**: Patent application filed
- **Team Expansion**: Framework now expanded to AD domain and adopted as common stack for Search Team

## Tech Stack

- **AutoML**: Optuna, Ray Tune
- **Optimization**: Evolutionary Strategies (ES)
- **Configuration**: Hydra-core
- **Infrastructure**: Existing search stack

## Problem Statement

E-commerce ranking systems need to balance multiple objectives:
- Click-Through Rate (CTR)
- Conversion Rate (CVR)
- User engagement metrics
- Business constraints (guardrails)

Traditional single-objective optimization often improves one metric while degrading others. MOHPER solves this through multi-objective optimization.

## Impact

The framework has become a critical tool for the Search Team, enabling data-driven optimization of ranking systems across multiple product surfaces and business domains.

## Period

October 2023 - January 2025

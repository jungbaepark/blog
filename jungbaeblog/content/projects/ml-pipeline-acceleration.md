---
title: "ML Pipeline Acceleration & Multi-GPU Training at RIIID (뤼이드)"
date: 2020-12-15
draft: false
tags: ["industrial", "mlops", "multi-gpu", "distributed-training", "ci-cd", "riiid"]
categories: ["Industrial Projects"]
summary: "Introduced RIIID's first multi-GPU training, boosting GPU utilization from 25% to 95% and cutting initialization time from 1 hour to 10 seconds. Built CI/CD pipelines with GitHub Actions."
weight: 15
cover:
  image: "/blog/images/projects/ml_pipeline_accel.png"
  alt: "ML Pipeline Acceleration: GPU Utilization 25% to 95%"
  hidden: false
  hiddenInList: false
---

## Overview

At **RIIID (뤼이드)**, introduced the company's first multi-GPU training and improved all pipeline procedures.

## Key Achievements

- **GPU Utilization**: Increased from 25% to 95%
- **Initialization Time**: Reduced from 1 hour to 10 seconds
- **First Multi-GPU Training**: Introduced the first multi-GPU training in the company
- **CI/CD**: Built CI/CD pipelines using GitHub Actions

```mermaid
graph LR
    A[Single GPU\n25% util] --> B[DDP Setup]
    B --> C[Multi-GPU\nTraining]
    C --> D[Docker\nContainer]
    D --> E[Distributed\n95% util]
```

## Technical Approach

- Introduced multi-GPU training to the company for the first time
- Improved all pipeline procedures, resulting in GPU utilization going from 25% to 95% and initialization time dropping from 1 hour to 10 seconds
- Set up CI/CD with GitHub Actions

## Tech Stack

- **Training**: Multi-GPU, Data-Distributed Training (PyTorch DDP)
- **CI/CD**: GitHub Actions
- **Infrastructure**: Docker, AWS

## Period

June 2020 - December 2020 | RIIID (뤼이드)

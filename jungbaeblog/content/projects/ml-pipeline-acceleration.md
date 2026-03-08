---
title: "ML Pipeline Acceleration & Multi-GPU Training at RIIID (뤼이드)"
date: 2020-12-15
draft: false
tags: ["industrial", "mlops", "multi-gpu", "distributed-training", "ci-cd", "riiid"]
categories: ["Industrial Projects"]
---

## Overview

At RIIID (뤼이드), I introduced the company's first multi-GPU training capability and systematically overhauled the entire ML pipeline to eliminate bottlenecks at every stage. The results were dramatic: GPU utilization jumped from 25% to 95%, and pipeline initialization time dropped from 1 hour to just 10 seconds. These improvements fundamentally changed how the ML team operated, enabling faster experimentation and shorter development cycles across all projects.

## Key Achievements

- **GPU Utilization**: Increased from **25% to 95%** through multi-GPU training and optimized data loading
- **Initialization Time**: Reduced pipeline startup from **1 hour to 10 seconds**, a 360x improvement
- **First Multi-GPU Training**: Introduced and deployed the company's first distributed training setup, setting the standard for all subsequent ML work
- **CI/CD for ML**: Built automated testing and deployment pipelines using GitHub Actions, bringing software engineering best practices to the ML workflow

## Technical Approach

### Multi-GPU Training

Before this project, all model training at RIIID (뤼이드) ran on single GPUs, which severely limited both the scale of experiments and the speed of iteration. I researched, implemented, and validated multi-GPU training strategies, carefully handling data parallelism, gradient synchronization, and batch size scaling. The transition required reworking data loading, checkpoint management, and evaluation routines to function correctly in a distributed setting.

### Pipeline Optimization

The 1-hour initialization time was traced to a combination of inefficient data preprocessing, redundant I/O operations, and suboptimal dependency loading. I profiled each stage of the pipeline, identified the critical bottlenecks, and restructured the flow to use lazy loading, caching, and parallel preprocessing. The result was a 10-second cold start that made rapid iteration practical for the first time.

### GPU Utilization Improvements

The jump from 25% to 95% GPU utilization came from multiple coordinated changes: optimized data loaders that kept GPUs fed with batches without idle time, mixed-precision training where appropriate, and elimination of CPU-bound preprocessing steps that had been running synchronously with GPU computation.

### CI/CD with GitHub Actions

I introduced CI/CD pipelines using GitHub Actions to automate testing, linting, and deployment of ML code. This reduced the risk of regressions when pipeline code changed and gave the team confidence to iterate faster without fear of breaking production workflows.

## Tech Stack

- **Distributed Training**: Multi-GPU (data parallelism, gradient synchronization)
- **CI/CD**: GitHub Actions (automated testing, deployment)
- **Profiling & Optimization**: Pipeline profiling, data loader optimization, caching strategies
- **Infrastructure**: GPU cluster management

## Impact

These improvements transformed the ML team's velocity at RIIID (뤼이드). What previously required overnight training runs could now be completed in a fraction of the time, and the near-instant pipeline initialization meant engineers could iterate on experiments throughout the day rather than waiting for lengthy startup sequences. The CI/CD infrastructure also reduced production incidents caused by untested code changes. Together, these changes established engineering standards that persisted well beyond my tenure on the team.

## Period

June 2020 - December 2020

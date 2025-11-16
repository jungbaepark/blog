---
title: "📚 Knowledge Tracing with Contrastive Learning (SOTA)"
date: 2022-10-15
draft: false
tags: ["industrial", "knowledge-tracing", "contrastive-learning", "deep-learning", "riiid"]
categories: ["Industrial Projects"]
---

## Overview

Research project achieving state-of-the-art (SOTA) performance on knowledge tracing and student dropout prediction using patch-level contrastive loss. This work significantly improved our ability to predict student performance and identify at-risk learners.

## Key Achievements

- **SOTA Performance**: Improved AUC from 77% to 88% on knowledge tracing benchmarks
- **Novel Method**: Applied patch-level contrastive learning to sequential student data
- **Multiple Datasets**: Validated approach across 6 different datasets
- **Deployment Ready**: Attempted deployment to SANTA TOEIC App using BentoML

## Technical Approach

### Knowledge Tracing
Predicting whether a student will correctly answer a question based on their historical interaction patterns.

### Dropout Prediction
Identifying students at risk of churning from the learning platform.

### Contrastive Learning
Applied conditional contrastive loss at the interaction level to learn better student representations that:
- Capture fine-grained learning patterns
- Generalize across different question types
- Identify struggling students early

## Tech Stack

- **Framework**: PyTorch, Deep Learning
- **Method**: Contrastive Learning, Sequential Modeling
- **Deployment**: BentoML (attempted)
- **Data**: Student interaction logs

## Impact

Better understanding of student learning patterns enables:
- Personalized learning recommendations
- Early intervention for struggling students
- Improved content difficulty calibration

## Period

August 2021 - October 2022

## Publications

- *Jungbae Park, et al. - "SAICL: Student Modelling with Interaction-level Auxiliary Contrastive Tasks for Knowledge Tracing and Dropout Prediction" (Arxiv, 2023)
- *Jungbae Park, Soonwoo Kwon, Jinyoung Kim, Sang Wan Lee - "SACCL: Sequential User Representations with Relation Contrastive Learning"

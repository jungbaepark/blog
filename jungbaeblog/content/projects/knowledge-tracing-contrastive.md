---
title: "Knowledge Tracing with Contrastive Learning"
date: 2022-10-15
draft: false
tags: ["industrial", "knowledge-tracing", "contrastive-learning", "deep-learning", "riiid"]
categories: ["Industrial Projects"]
---

## Overview

At **RIIID (뤼이드)**, conducted research achieving state-of-the-art performance on knowledge tracing and student dropout prediction using conditional contrastive learning. This work significantly improved the ability to predict student performance and identify at-risk learners, and was deployed to the Santa TOEIC platform.

## Key Achievements

- **AUC Improvement**: From 77% to 88% with conditional contrastive learning
- **Multi-Dataset Validation**: Validated approach across **6 different datasets**
- **Production Deployment**: Deployed to **Santa TOEIC** app via BentoML
- **Novel Method**: Applied conditional contrastive loss at the interaction level

## Technical Approach

### Knowledge Tracing

Predicting whether a student will correctly answer a question based on their historical interaction patterns. The model captures fine-grained learning trajectories to provide accurate performance predictions.

### Dropout Prediction

Identifying students at risk of churning from the learning platform, enabling early intervention strategies.

### Conditional Contrastive Learning

Applied conditional contrastive loss at the interaction level to learn better student representations that:
- Capture fine-grained learning patterns
- Generalize across different question types
- Identify struggling students early
- Leverage conditional information for more discriminative embeddings

## Tech Stack

- **Framework**: PyTorch
- **Architecture**: Transformer, Sequential Modeling
- **Method**: Contrastive Learning, Knowledge Tracing
- **Deployment**: BentoML

## Period

August 2021 - October 2022

## Impact

Better understanding of student learning patterns enables personalized learning recommendations, early intervention for struggling students, and improved content difficulty calibration on the Santa TOEIC platform.

## Publications

- Jungbae Park, et al. - "SAICL: Student Modelling with Interaction-level Auxiliary Contrastive Tasks for Knowledge Tracing and Dropout Prediction" (Arxiv, 2023)
- Jungbae Park, Soonwoo Kwon, Jinyoung Kim, Sang Wan Lee - "SACCL: Sequential User Representations with Relation Contrastive Learning"

---
title: "Knowledge Tracing with Contrastive Learning"
date: 2022-10-15
draft: false
tags: ["industrial", "knowledge-tracing", "contrastive-learning", "deep-learning", "riiid"]
categories: ["Industrial Projects"]
summary: "Proposed ACCL and RCL contrastive learning methods at RIIID, achieving state-of-the-art on student modeling across 6 benchmarks (dropout prediction, knowledge tracing). Deployed to Santa TOEIC platform."
weight: 10
cover:
  image: "/blog/images/projects/surcl_rcl_modules-02.png"
  alt: "Figure 1: RCL contrastive learning modules from SURCL paper"
  hidden: false
  hiddenInList: false
---

## Overview

At **RIIID (뤼이드)**, proposed Attentive Conditional Contrastive Learning (ACCL) and Relation Contrastive Learning (RCL), achieving state-of-the-art on student (user) modeling---including dropout prediction, conditional dropout prediction, and knowledge tracing---across 6 benchmarks. Deployed to the Santa TOEIC platform.

## Key Achievements

- **SOTA on Student Modeling**: Achieved state-of-the-art on dropout prediction, conditional dropout prediction, and knowledge tracing with proposed ACCL across multiple benchmarks
- **Multi-Dataset Validation**: Validated approach across **6 different datasets**
- **Production Deployment**: Deployed to **Santa TOEIC** app via BentoML
- **Novel Methods**: ACCL (trainable attentional coefficients reweighting CL objectives) and RCL (RelationNCE loss)

## Technical Approach

![SAICL framework figure](/blog/images/projects/saicl_framework-02.png)

### Dropout Prediction

Predicting whether a student will churn from the learning platform, enabling early intervention strategies. Covers both naive dropout prediction and conditional dropout prediction (conditioned on contextual information). Achieved SOTA with the proposed ACCL method.

### Knowledge Tracing

Predicting whether a student will correctly answer a question based on their historical interaction patterns. Improved performance with contrastive learning approaches.

### SAICL: Auxiliary Interaction-level Contrastive Learning

The SAICL framework introduces a novel student modeling approach that addresses the sparsity problem in user interaction sequences by:
- **Self-supervised contrastive objective** at each interaction step (not just sequence-level)
- **Auxiliary interaction-level CL** that helps the model distinguish between user behavior dynamics across sessions
- **Conditional dropout prediction** (CondDP) — a new task formulation beyond standard knowledge tracing

![SAICL Paper: Auxiliary Interaction-level Contrastive Learning](/blog/images/projects/saicl_paper-01.png)

### SURCL: Sequential User Representations via Relation Contrastive Learning

SURCL introduces learnable attentional coefficients for RelationNCE loss that:
- Pay attention to **relations between patches** rather than just point-level contrasts
- Adaptively mediate contrastive objectives based on **conditional input similarity**
- Incorporate both conditional inputs and output embeddings for better user representations
- Generalize across multiple downstream tasks (knowledge tracing, dropout prediction, sequential recommendation)

![SURCL Paper: Relation Contrastive Learning](/blog/images/projects/surcl_paper-01.png)

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

- Jungbae Park, Jinyoung Kim, Soonwoo Kwon, Sang Wan Lee - "SAICL: Auxiliary Interaction-level Contrastive Learning for Knowledge Tracing and Dropout Prediction" (Submitted to AAAI 2023; arXiv:2210.09012)
- Jungbae Park, Soonwoo Kwon, Jinyoung Kim, Sang Wan Lee - "SURCL: Sequential User Representations via Relation Contrastive Learning" (Submitted to NeurIPS 2022)

---
title: "🔍 CLIP-based E-Commerce Multimodal Search and Classification"
date: 2023-06-15
draft: false
tags: ["industrial", "CLIP", "multimodal-ai", "e-commerce", "bucketplace"]
categories: ["Industrial Projects"]
---

## Overview

Designed and developed CLIP-based solutions for e-commerce downstream tasks, including multimodal retrieval and product classification, significantly improving search performance and product categorization.

## Key Projects

### 1. Multimodal Retrieval

Enabled users to search for products using both text and images through CLIP embeddings.

**Results**:
- **Query CTR**: +3.03% improvement
- **Query CTCVR**: +16.39% improvement
- **Quantization**: 2x speed improvement, 4x disk memory reduction

### 2. Product Category & Attributes Classification

Automated product categorization using CLIP-based models for a large-scale product catalog.

**Performance**:
- **Top-10 Accuracy**: 92.23% among >2,000 categories
- Robust classification across diverse product types
- Automated attribute extraction

## Tech Stack

- **Model**: CLIP (Contrastive Language-Image Pre-training)
- **Optimization**: Model quantization for production
- **Infrastructure**: E-commerce search stack
- **Deployment**: Production-grade serving

## Challenges & Solutions

**Challenge**: Large category space (>2,000 categories) with imbalanced data
**Solution**: Fine-tuned CLIP with category-specific data and implemented hierarchical classification

**Challenge**: Latency requirements for real-time search
**Solution**: Applied quantization techniques achieving 2x speed with minimal accuracy loss

## Impact

These CLIP-based solutions transformed how users discover products, enabling more intuitive search through natural language and images while improving internal product management through automated classification.

## Period

January 2023 - June 2023

---
title: "CLIP-based E-Commerce Multimodal Search and Classification"
date: 2023-06-15
draft: false
tags: ["industrial", "CLIP", "multimodal-ai", "e-commerce", "bucketplace", "quantization"]
categories: ["Industrial Projects"]
---

## Overview

At **Bucketplace (오늘의집)**, designed and developed CLIP-based solutions for e-commerce downstream tasks, including multimodal retrieval and product classification. These systems significantly improved search performance and product categorization across the platform.

## Key Achievements

- **Query CTR**: +3.03% improvement in search click-through rate
- **Query CTCVR**: +16.39% improvement in click-through conversion rate
- **Inference Speed**: 2x speed improvement via quantization
- **Disk Usage**: 1/4 disk memory reduction through model compression
- **Top-10 Accuracy**: 92.23% among >2,000 product categories

## Technical Approach

### Multimodal Retrieval

Enabled users to search for products using both text and images through CLIP embeddings. By aligning text and image modalities in a shared embedding space, the system supports flexible cross-modal queries, allowing users to find visually similar products or search by natural language descriptions.

### Product Category and Attributes Classification

Automated product categorization using CLIP-based models for a large-scale product catalog. Fine-tuned CLIP with category-specific data and implemented hierarchical classification to handle the large category space (>2,000 categories) with imbalanced data distributions.

### Quantization for Production

Applied quantization techniques to meet real-time latency requirements for production search systems, achieving 2x speed improvement with minimal accuracy loss and 4x disk memory reduction.

## Tech Stack

- **Model**: CLIP (Contrastive Language-Image Pre-training)
- **Optimization**: Quantization, Model Compression
- **Retrieval**: Multimodal Retrieval
- **Deployment**: Production-grade serving infrastructure

## Period

January 2023 - June 2023

## Impact

These CLIP-based solutions transformed how users discover products on the platform, enabling more intuitive search through natural language and images while improving internal product management through automated classification across thousands of categories.

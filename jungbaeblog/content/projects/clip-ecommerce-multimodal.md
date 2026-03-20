---
title: "CLIP-based E-Commerce Multimodal Search and Classification"
date: 2023-06-15
draft: false
tags: ["industrial", "CLIP", "multimodal-ai", "e-commerce", "bucketplace", "quantization"]
categories: ["Industrial Projects"]
summary: "Shipped CLIP-based multimodal retrieval at Bucketplace, achieving +16.39% query CTCVR, 2x inference speed via quantization, and 92.23% Top-10 accuracy across 2,000+ product categories."
weight: 10
cover:
  image: "/blog/images/projects/clip_retrieval_showcase.png"
  alt: "CLIP Multimodal Retrieval: Before vs After — zero-result queries now return relevant products via semantic matching"
  hidden: false
  hiddenInList: false
---

## Overview

At **Bucketplace (오늘의집)**, shipped multimodal retrieval improvements and quantization optimizations for e-commerce search, along with product classification across a large category space.

## Key Achievements

- **Query CTR**: +3.03% improvement
- **Query CTCVR**: +16.39% improvement
- **Inference Speed**: 2x speed improvement via quantization
- **Disk Usage**: 1/4 disk reduction through quantization
- **Classification**: Top-10 Accuracy 92.23% among >2,000 product categories

## Technical Approach

### Multimodal Dense Retrieval

Integrated CLIP-based dense vector retrieval into the e-commerce search pipeline, enabling semantic matching beyond traditional BM25 keyword search:

- **Image-to-Text Retrieval**: Users can search products using text queries that match against product image embeddings
- **Partial Hybrid Search**: Combined dense image retrieval via CLIP with traditional text-based BM25, creating a hybrid retrieval system
- **Query Embedding Service**: Built a dedicated service for real-time query vector generation

### Production Optimization

- **INT8 Quantization**: Achieved 2x inference speed and 1/4 disk usage with minimal quality degradation
- **Serving Architecture**: Deployed via Triton Inference Server for efficient batch inference

### Product Classification

Built a multi-label classification system across >2,000 product categories:
- **Top-10 Accuracy**: 92.23% — enabling automated category assignment at scale
- **Application**: Used for product catalog enrichment and search filter generation

![Related Works: NAVER Shopping and e-CLIP Architectures](/blog/images/projects/clip_related-04.png)

## Tech Stack

- **Model**: CLIP (OpenAI), SigLIP
- **Optimization**: INT8 Quantization, ONNX Runtime
- **Retrieval**: Dense Vector Retrieval, Hybrid Search (BM25 + KNN)
- **Serving**: Triton Inference Server
- **Search**: ElasticSearch

## Period

January 2023 - June 2023 | Bucketplace (오늘의집)

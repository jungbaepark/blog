---
title: "Scene-to-Products Retrieval for Digital Twin (Image-to-3D)"
date: 2026-01-01
draft: false
tags: ["industrial", "digital-twin", "3d-reconstruction", "genai", "segmentation", "bucketplace"]
categories: ["Industrial Projects"]
---

## Overview

At Bucketplace (오늘의집), I built an end-to-end segmentation-to-indexing-to-demo-validation pipeline for scene-to-products retrieval, and implemented a process-centric generative AI pipeline for Digital Twin creation at scale.

## Key Achievements

- **Lead Time Reduction**: 2 weeks to 3 days
- **Recall@10**: 2.06% to 28.08% (13x+ improvement)
- **Defective Image Removal**: 56.7% defective images removed (more than 2x yield)
- **Catalog Scale**: 30k to 400k+ products across 154 to 277 categories (+80%)
- **SAM3D Pipeline**: ~1/100 cost vs outsourced Image-to-3D
- **3D Collaboration**: 6,000x cost reduction and 2,200x production increase

## Technical Approach

### Process-Centric GenAI Pipeline

The pipeline follows four stages:

1. **Refine**: Quality assessment and preprocessing of raw product images
2. **Representative Extraction**: Identifying and extracting the most representative views of each product
3. **Validate/Filter**: Automated validation of generated outputs
4. **Indexing**: Validated products indexed into the retrieval system

### E2E Pipeline

Built end-to-end segmentation, indexing, and demo validation pipeline operating across the full product catalog.

## Tech Stack

- **3D Reconstruction**: SAM3D Pipeline
- **Computer Vision**: Segmentation, Object Detection
- **GenAI Pipeline**: Process-centric generative AI workflow
- **Retrieval**: Vector Indexing

## Period

December 2025 - January 2026 | Bucketplace (오늘의집)

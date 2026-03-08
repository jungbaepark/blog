---
title: "Scene-to-Products Retrieval for Digital Twin (Image-to-3D)"
date: 2026-01-01
draft: false
tags: ["industrial", "digital-twin", "3d-reconstruction", "genai", "segmentation", "bucketplace"]
categories: ["Industrial Projects"]
---

## Overview

At Bucketplace (오늘의집), I built an end-to-end pipeline for scene-to-products retrieval in the context of Digital Twin creation, converting 2D product images into 3D models at scale. The project addressed a critical bottleneck in the Room Planner product: the slow, expensive process of populating the 3D product catalog. By designing a process-centric generative AI pipeline, I dramatically reduced lead times while scaling coverage across product categories.

## Key Achievements

- **Lead Time Reduction**: Cut production lead time from **2 weeks to 3 days** through end-to-end automation
- **Recall Improvement**: Improved Recall@10 from **2.06% to 28.08%**, a **13x+ improvement**, through the segmentation-to-indexing pipeline
- **Defective Image Removal**: Eliminated **56.7% of defective images**, more than doubling the usable yield from source data
- **Catalog Scale**: Expanded product coverage from **30k to 400k+ products** across **154 to 277 categories (+80%)**
- **Cost Efficiency**: SAM3D pipeline achieved approximately **1/100th the cost** of outsourced Image-to-3D conversion
- **Production Scaling**: Realized **6,000x cost reduction** and **2,200x production increase** through 3D collaboration pipeline

## Technical Approach

The pipeline follows a process-centric generative AI workflow with four key stages:

1. **Refine**: Raw product images undergo quality assessment and preprocessing, filtering out defective or unsuitable images that would produce poor 3D reconstructions.

2. **Representative Extraction**: From the refined image set, the system identifies and extracts the most representative views of each product -- the angles and perspectives that capture essential geometric and aesthetic information for 3D reconstruction.

3. **Validate and Filter**: Generated 3D models pass through automated validation checks, ensuring geometric fidelity, texture quality, and dimensional accuracy before entering the product catalog.

4. **Indexing**: Validated 3D products are indexed into the retrieval system with rich metadata, enabling downstream search and recommendation services to surface them effectively.

The end-to-end pipeline (segmentation, indexing, demo validation) was built to operate autonomously, with each stage feeding quality signals forward to improve downstream performance.

## Tech Stack

- **3D Reconstruction**: SAM3D Pipeline, Image-to-3D conversion
- **Computer Vision**: Segmentation models, Object Detection
- **GenAI Pipeline**: Process-centric generative AI workflow
- **Retrieval**: Vector Indexing, Similarity Search
- **Infrastructure**: Automated batch processing pipeline

## Impact

This project transformed the economics of 3D product catalog creation at Bucketplace. What previously required expensive outsourced labor and weeks of lead time now runs as an automated pipeline delivering results in days. The 13x recall improvement means users of Room Planner can find relevant 3D products far more effectively, while the 80% expansion in category coverage ensures a much broader selection is available. The cost and production scaling (6,000x and 2,200x respectively) made it feasible to build a comprehensive 3D product catalog that would have been economically impossible through manual processes.

## Period

December 2025 - January 2026 | Bucketplace (오늘의집)

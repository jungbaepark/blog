---
title: "Scene-to-Products Retrieval for Digital Twin (Image-to-3D)"
date: 2026-01-01
draft: false
tags: ["industrial", "digital-twin", "3d-reconstruction", "genai", "segmentation", "bucketplace"]
categories: ["Industrial Projects"]
summary: "Built an end-to-end scene-to-products retrieval pipeline for Digital Twin at Bucketplace, achieving 13x recall improvement, 6,000x cost reduction in 3D collaboration, and scaling the catalog from 30K to 400K+ products."
weight: 1
cover:
  image: "/blog/images/projects/page17_img1.png"
  alt: "Segment Selection and 3D Layout Visualization"
  hidden: false
  hiddenInList: false
---

## Overview

At Bucketplace (오늘의집), I built an end-to-end segmentation-to-indexing-to-retrieval pipeline that detects and separates multiple furniture/decor instances from room scene images, connects them to the product index, and achieves performance far beyond naive image-to-image similarity. The project also established the foundation for a 3D object retrieval-based digital twin pipeline.

![Room Scene to Products Retrieval Task](/blog/images/projects/notion_room_scene_task.png)

## Key Achievements

- **DetectRate@10**: 2.06% to **28.08%** (13.6x improvement over baseline)
- **Lead Time Reduction**: 2 weeks to 3 days for segmap refinement pipeline
- **Defective Image Removal**: 56.7% defective images removed (more than 2x yield)
- **Catalog Scale**: 80K to **440K** products (5.5x expansion, filtered from 700K for quality)
- **Category Coverage**: 154 to 277 categories (+80%)
- **SAM3D Pipeline**: ~1/100 cost vs outsourced Image-to-3D
- **3D Collaboration**: 6,000x cost reduction and 2,200x production increase
- **VLM Refinement Optimization**: Switched from QWEN3 8B (1 week+ GPU) to GPT-5-nano with reasoning, completing refinement in 2 days via API parallelization

## Technical Approach

### Retrieval Pipeline Architecture

The pipeline follows a multi-stage approach:

`[Room Scene] → [Object Detection] → [Query Generation] → [Product DB (ES) Search] → [Post-processing] → [Results]`

### v1 to v2 Improvements

| Component | v1 | v2 | Improvement |
|---|---|---|---|
| Product DB Size | 80K | 440K | 5.5x expansion |
| Data Quality | Inaccurate filtering | 700K → 440K quality filter | Removed low-quality products |
| Segmap Quality | Low | Improved | VLM-based verification pipeline |
| Post-processing | None | Category Boost | Category-aware re-ranking |
| VLM Refinement | QWEN3 8B (1 week+, 2 GPUs) | GPT-5-nano + reasoning (2 days, API parallel) | 3.5x faster, higher accuracy |

![Category Coverage Expansion](/blog/images/projects/notion_room_scene_category.png)

### Segmap Refinement Pipeline

- **IoM-based Merging**: Automatic merging of overlapping instances
- **VLM Category Verification**: Filtering incorrectly detected objects via vision-language models
- **Representativeness Scoring**: Prioritizing search-suitable segments

### Experiment Results

Best configuration: **SAM3 bbox → Full Image Search + Category Boost**

| Configuration | DetectRate@10 | Hit Rate@10 | MRR |
|---|---|---|---|
| SAM3 bbox → Full Image + Category | **28.08%** | 33.06% | 0.157 |
| OWLv2 bbox → bbox crop + Category | 26.56% | 30.20% | 0.166 |
| SAM3 bbox → segmap crop + Category | 26.28% | 30.43% | 0.152 |
| Baseline (naive SigLIP2) | 2.06% | 2.06% | 0.011 |

Key findings:
- Bbox crop outperforms segmap crop as query (+7.6%p)
- Full product image indexing outperforms cropped indexing
- Weak filtering (0.01) outperforms strong filtering (0.05) — excessive filtering excludes correct answers

### 3D Digital Twin Extension

Retrieved products can be further transformed into 3D objects for digital twin placement, collaborated with the XR team for top-N segment 3D reconstruction.

![3D Digital Twin from Retrieved Products](/blog/images/projects/notion_room_scene_3d.png)

![SAM3D Workflow Pipeline](/blog/images/projects/bp_sam3d_workflow.png)

## Tech Stack

- **Embedding Model**: SigLIP2
- **Object Detection**: SAM3, OWLv2
- **VLM Refinement**: GPT-5-nano (reasoning), QWEN3 8B Instruct
- **3D Reconstruction**: SAM3D Pipeline
- **Search Infrastructure**: ElasticSearch (vector KNN)
- **Evaluation**: DetectRate@K, Hit Rate@K, MRR

## Period

December 2025 - January 2026 | Bucketplace (오늘의집)

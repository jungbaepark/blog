---
title: "Personalized Multimodal Retrieval with VLM Distillation"
date: 2025-06-15
draft: false
tags: ["industrial", "multimodal-retrieval", "knowledge-distillation", "recommendation", "bucketplace"]
categories: ["Industrial Projects"]
summary: "Developed personalized multimodal retrieval combining SASRec sequential recommendation with Jina-CLIP-V2 vision-language representations, using knowledge distillation for efficient production serving at Bucketplace."
weight: 5
cover:
  image: "/blog/images/projects/multimodal_vlm_pipeline.png"
  alt: "Personalized Multimodal Retrieval Pipeline"
  hidden: false
  hiddenInList: false
---

## Overview

At **Bucketplace (오늘의집)**, researched and developed personalized multimodal retrieval systems by combining sequential recommendation models with vision-language models and knowledge distillation techniques. This work explores unifying visual understanding, language comprehension, and user behavior modeling into a single retrieval framework for e-commerce product recommendation.

## Key Achievements

- **Sequential Modeling**: Implemented SASRec (Self-Attentive Sequential Recommendation) for user behavior modeling, learning from product page view and click patterns
- **Multimodal Embeddings**: Integrated Jina-CLIP-V2 for joint vision-language representations
- **Knowledge Distillation**: Applied distillation techniques to create efficient production models from large VLMs
- **Demo Development**: Built interactive demo using Streamlit and BentoML

## Technical Approach

### Problem Context

Existing recommendation systems at Bucketplace (e.g., SASRec-based producers for PDP feed) operate on behavioral signals alone — click patterns, view history, and purchase sequences. These models predict "what the user will look at next" but lack understanding of *why* — the visual attributes, style preferences, and aesthetic choices that drive user decisions.

### Approach: VLM-Distilled Sequential Recommendation

1. **Teacher Model (VLM)**: Jina-CLIP-V2 generates rich multimodal embeddings that capture both visual and textual product attributes
2. **Student Model (SASRec)**: A lightweight sequential recommendation model is trained to predict the VLM's embedding outputs, effectively distilling multimodal understanding into an efficient sequential model
3. **Metric Learning**: PyTorch-Metric-Learning for contrastive training between user interaction sequences and multimodal product representations
4. **Efficient Training**: QLoRA for parameter-efficient fine-tuning, DeepSpeed for distributed training

### Integration with Recommendation Pipeline

The distilled model slots into the existing Producer → Mixer → Ranker → Twiddler recommendation pipeline at Bucketplace, providing multimodal-aware candidate generation alongside existing behavioral producers (SASRec from PDP click, similar image, popular CTR, etc.).

## Tech Stack

- **Deep Learning**: PyTorch, HuggingFace, DeepSpeed
- **Training**: Lightning AI, QLoRA
- **Metric Learning**: PyTorch-Metric-Learning
- **VLM**: Jina-CLIP-V2
- **Sequential Models**: SASRec
- **Deployment**: BentoML, Streamlit

## Period

May 2025 - June 2025 | Bucketplace (오늘의집)

## Impact

This project explores the next generation of product recommendation by bridging the gap between visual understanding and behavioral prediction. By distilling VLM knowledge into efficient sequential models, the approach enables personalized multimodal retrieval that can understand both *what users do* and *what they see*, unlocking style-aware and context-aware product discovery at scale.

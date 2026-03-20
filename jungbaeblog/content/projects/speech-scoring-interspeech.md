---
title: "Prompt-Aware Speech Scoring System for Second Language Learners"
date: 2023-01-15
draft: false
tags: ["industrial", "speech-processing", "deep-learning", "published", "riiid", "interspeech", "cold-start"]
categories: ["Industrial Projects"]
summary: "Developed a prompt-aware automatic speech scoring system at RIIID that solves the cold-start item problem using BERT/CLIP prompt embeddings. Published at InterSpeech 2023 and deployed to SANTA Say TOEIC Speaking app."
weight: 10
cover:
  image: "/blog/images/projects/speech_scoring_arch-3.png"
  alt: "Figure 3: End-to-end speech scoring model architecture from InterSpeech paper"
  hidden: false
  hiddenInList: false
---

## Overview

At **RIIID (뤼이드)**, developed an end-to-end automatic speech scoring system for second language learners that addresses the cold-start item problem by incorporating prompt awareness. Proposed prompt embeddings combined with question context (BERT/CLIP) to enable reliable scoring even for unseen prompts. The system was successfully deployed to SANTA Say, a TOEIC Speaking practice app.

## Key Achievements

- **Publication**: Accepted to **InterSpeech 2023** (top conference on speech and audio processing)
- **Production Deployment**: Integrated into SANTA Say TOEIC Speaking App
- **Cold-Start Solution**: Proposed prompt embeddings + question context (BERT/CLIP) to address the cold-start item problem
- **Real-World Impact**: Enabling thousands of language learners to improve their speaking skills

## Technical Approach

![Figure 1: Cold start problem visualization](/blog/images/projects/speech_scoring_problem-1.png)

Traditional speech scoring systems struggle when encountering new prompts (questions) they have not seen during training. This is the cold-start item problem. Our approach incorporates:

- **Prompt Embeddings**: Learned representations of question prompts that capture their semantic content
- **Question Context via BERT/CLIP**: Leveraging pre-trained language and vision-language models to encode prompt text and images
- **End-to-End Architecture**: Joint optimization of prompt understanding and speech scoring components

This allows the system to provide accurate scores even for new, unseen prompts by understanding the context of what learners are responding to.

## Tech Stack

- **Domain**: Speech Scoring, TOEIC Speaking
- **Models**: PyTorch, BERT, CLIP
- **Problem**: Cold-start Item Problem
- **Deployment**: Production-grade serving for mobile app

## Period

October 2022 - January 2023

## Impact

Enables fair and consistent scoring for speaking practice, helping language learners track their progress and identify areas for improvement, even as new practice questions are added to the platform.

## Publications

- Jungbae Park, Seungtaek Choi - "Addressing Cold Start Problem for End-to-end Automatic Speech Scoring" (InterSpeech 2023, DOI: 10.21437/Interspeech.2023-533)

---
title: "Attentional Control for Time-Series Data (Master's Thesis)"
date: 2019-02-15
draft: false
tags: ["academic", "deep-learning", "attention-mechanism", "time-series", "kaist"]
categories: ["Academic Research"]
summary: "Master's thesis at KAIST on attentional control for time-series classification and synthesis, solving the memory-based vs. memoryless trade-off for EEG signals. Oral presentation at IEEE SMC 2018."
weight: 25
cover:
  image: "/blog/images/projects/eeg_rl_system-3.png"
  alt: "Overall system architecture for EEG signal classification with Deep RL (IEEE SMC 2018)"
  hidden: false
  hiddenInList: false
---

## Overview

Master's thesis research at KAIST exploring attentional control methods for time-series data classification and synthesis. This work investigated how attention mechanisms can improve deep learning models' ability to process sequential data, with applications in neuroscience and signal processing.

## Key Achievements

- **Publication**: Oral presentation at IEEE SMC 2018
- Developed novel attention-based approaches for time-series classification and synthesis
- Applied reinforcement learning for adaptive EEG signal processing
- Solved the memory-based vs. memoryless trade-off problem

## Technical Approach

### EEG Signal Classification

Applied reinforcement learning for adaptive EEG signal processing, addressing the memory-based vs. memoryless trade-off problem. This approach enables the model to dynamically decide when to rely on historical context and when to focus on current observations.

![RL controller, CNN, LSTM, and Mix architectures for EEG classification](/blog/images/projects/eeg_rl_arch-2.png)

### Attention Mechanisms for Sequential Data

Investigated how attention can focus on relevant time steps in sequential data, balancing model capacity with interpretability. Applications span neuroscience and signal processing domains.

## Tech Stack

- **Deep Learning**: LSTM, Attention Mechanisms
- **Signal Processing**: EEG Analysis, Time-Series Processing
- **Frameworks**: TensorFlow, PyTorch

## Period

March 2017 - February 2019

## Impact

This foundational research in attention mechanisms laid the groundwork for later work in multimodal AI and sequential modeling, including knowledge tracing and recommendation systems.

## Publications

- Jungbae Park, Sang Wan Lee - "Solving the Memory-based-Memoryless Trade-off Problem for EEG Signal Classification" (IEEE SMC 2018, Oral)

## Thesis

- **Title**: "Attentional Control Methods for Time-series Data Classification and Synthesis"
- **Advisor**: Prof. Sang Wan Lee
- **Institution**: KAIST, Lab for Brain and Machine Intelligence

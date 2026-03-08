---
title: "Polyphonic Sound Event Detection with Transfer Learning"
date: 2019-04-15
draft: false
tags: ["academic", "audio-processing", "transfer-learning", "deep-learning", "published", "icassp", "humelo"]
categories: ["Academic Research"]
---

## Overview

At **Humelo (휴멜로)**, conducted research on detecting multiple simultaneous sound events using convolutional bidirectional LSTMs and synthetic data-based transfer learning. This work addressed the challenge of learning from limited real-world audio data and was published at ICASSP 2019 as corresponding author.

## Key Achievements

- **F1 Score**: +28.4% improvement on TUT 2016 dataset
- **Error Rate**: -0.42 reduction on TUT 2016 dataset
- **Publication**: Published at **ICASSP 2019** (top conference on audio and signal processing), corresponding author
- **Patents**: Multiple registered patents on sound event detection model training

## Technical Approach

### Synthetic Data-Based Transfer Learning

- Generated synthetic audio data for pre-training
- Transferred knowledge to real-world sound event detection
- Achieved robust performance with limited labeled data

### Architecture

- **Model**: Convolutional Bidirectional LSTM
- **Data Augmentation**: Synthetic audio generation
- **Transfer Learning**: Pre-train on synthetic data, fine-tune on real data
- **Evaluation**: TUT 2016 Sound Event Detection dataset

## Tech Stack

- **Framework**: PyTorch
- **Method**: Transfer Learning, Convolutional Bidirectional LSTM
- **Domain**: Polyphonic Sound Event Detection

## Period

2018 - 2019

## Impact

This work demonstrated how synthetic data could effectively address the scarcity of labeled real-world audio data, a principle applicable to many audio and speech processing tasks. The significant improvements in F1 score and error rate validated the transfer learning approach for sound event detection.

## Publications

- Seokwon Jeong, Jungbae Park (corresponding author), Sang Wan Lee - "Polyphonic sound event detection using convolutional bidirectional LSTM and Synthetic data-based transfer learning" (ICASSP 2019)

## Patents

- Method and Apparatus for Training Sound Event Detection Model (KR 1021724750000 and others)

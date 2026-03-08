---
title: "Speech Emotion Recognition & Classification System"
date: 2019-02-01
draft: false
tags: ["startup", "speech-processing", "emotion-recognition", "deep-learning", "humelo"]
categories: ["Startup Projects"]
---

## Overview

At Humelo (휴멜로), I managed and developed a speech emotion classification system that served as a critical component in the company's Emotional TTS pipeline. The system extracted acoustic features from raw audio signals and classified them into multiple emotion categories, enabling downstream TTS models to synthesize speech with appropriate emotional expression. This work combined classical audio signal processing with modern deep learning architectures to achieve robust multi-class emotion detection.

## Key Achievements

- **End-to-End System**: Built a complete pipeline from raw audio input to multi-class emotion classification
- **Feature Engineering**: Developed a feature extraction module combining MFCC and Mel-spectrogram analysis for rich acoustic representations
- **Deep Learning Classifiers**: Implemented and compared multiple architectures including SpeechCNN and CRNN for emotion classification
- **Pipeline Integration**: Integrated the emotion recognition module into Humelo (휴멜로)'s broader Emotional TTS pipeline, enabling emotion-aware speech synthesis

## Technical Approach

### Feature Extraction

The feature extraction stage transformed raw audio waveforms into representations suitable for deep learning classifiers. I implemented a dual-feature approach combining Mel-Frequency Cepstral Coefficients (MFCC) with Mel-spectrogram analysis. MFCCs captured the spectral envelope characteristics closely related to how humans perceive speech, while Mel-spectrograms provided a time-frequency representation that preserved temporal dynamics crucial for emotion detection. The combination gave classifiers access to both compact perceptual features and detailed spectro-temporal patterns.

### Classifier Architecture

I developed and evaluated two primary architectures:

**SpeechCNN**: A convolutional neural network designed for spectrogram-based inputs, using stacked convolutional layers to learn hierarchical audio features. The CNN architecture excelled at capturing local spectral patterns associated with different emotional states, such as pitch variation, energy distribution, and spectral tilt.

**CRNN (Convolutional Recurrent Neural Network)**: This hybrid architecture combined convolutional layers for local feature extraction with recurrent layers (LSTM/GRU) for modeling temporal dependencies. Emotions in speech unfold over time -- a sentence might start neutral and shift to anger -- and the recurrent component captured these dynamics more effectively than purely convolutional approaches.

### Multi-Class Emotion Detection

The system classified audio segments into multiple emotion categories (e.g., neutral, happy, sad, angry, fearful). Training involved careful handling of class imbalance, as emotional speech datasets typically contain disproportionate amounts of neutral speech. I applied data augmentation techniques and class-weighted loss functions to ensure the model performed reliably across all emotion categories.

### Integration with Emotional TTS

The emotion classifier fed its predictions into the broader TTS pipeline, where emotion labels and confidence scores guided the synthesis model's prosody, pitch contour, and speaking rate. This closed the loop between emotion recognition and emotion generation, allowing Humelo (휴멜로)'s TTS system to both understand and reproduce emotional speech.

## Tech Stack

- **Deep Learning Framework**: PyTorch
- **Architectures**: SpeechCNN, CRNN (CNN + LSTM/GRU)
- **Audio Features**: MFCC, Mel-spectrogram analysis
- **Domain**: Speech emotion recognition, multi-class classification
- **Integration**: Emotional TTS pipeline

## Impact

The speech emotion recognition system became a foundational component of Humelo (휴멜로)'s Emotional TTS product line. By accurately detecting emotions in reference audio, the system enabled the TTS pipeline to generate speech that matched desired emotional qualities -- a key differentiator in a market where most TTS systems produced flat, emotionless output. This work also contributed to the research published at ICASSP and supported the government-funded R&D grants that sustained the company's growth.

## Period

April 2018 - February 2019

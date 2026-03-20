---
title: "Emotional Text-to-Speech and Voice Conversion Systems"
date: 2020-05-15
draft: false
tags: ["startup", "TTS", "speech-synthesis", "deep-learning", "humelo", "published", "voice-conversion", "VAE"]
categories: ["Startup Projects"]
summary: "Led development of duration-controllable TTS and emotional voice conversion at Humelo, producing two ICASSP publications (2019 Oral 1st author, 2020). Won Minister of Science and ICT Special Award at K-Startup 2018."
weight: 20
cover:
  image: "/blog/images/projects/tts_model-2.png"
  alt: "ICASSP 2019 Duration Controllable TTS: attention alignment and PDC model architecture"
  hidden: false
  hiddenInList: false
---

## Overview

As Research Lead and COO at **Humelo (휴멜로)**, led the development of next-generation speech synthesis and voice conversion systems. This work produced two ICASSP publications: Duration Controllable TTS (ICASSP 2019, Oral, 1st author) and Emotional Voice Conversion (ICASSP 2020). The project was funded by the Ministry of SMEs and Startups through the TIPS R&D grant.

## Key Achievements

- **ICASSP 2019 (Oral, 1st Author)**: Duration Controllable TTS with phonemic-level duration control
- **ICASSP 2020**: Multi-speaker, multi-domain emotional voice conversion
- **Government Grant**: Secured TIPS R&D grant from Ministry of SMEs (S2644149)
- **Awards**: Minister of Science and ICT Special Award at K-Startup 2018

## Technical Approach

### Duration Controllable TTS (ICASSP 2019, Oral)

Achieved natural speech synthesis through phonemic-level duration control using teacher attention alignment. This approach allows fine-grained control over the timing and rhythm of synthesized speech by leveraging attention alignment information from a teacher model to guide duration prediction.

![Training curves: alignment loss and evaluation loss](/blog/images/projects/tts_results-3.png)

### Emotional Voice Conversion (ICASSP 2020)

Developed multi-speaker, multi-domain emotional voice conversion using Factorized Hierarchical Variational Autoencoder (FHVAE). This architecture disentangles speaker identity, emotional expression, and linguistic content into separate latent representations, enabling flexible control over each factor independently.

![FHVAE Voice Conversion Architecture (ICASSP 2020)](/blog/images/projects/voice_conversion_arch-1.png)

Key contributions:
- **Sequence-level and segment-level disentanglement** using FHVAE to separate speaker identity from emotional expression
- **Emotion embedding with margin loss** to further facilitate emotion conversion via cycle-consistency loss
- **Multi-speaker, multi-domain** setup: 2 speakers x 6 emotion classes, evaluated with MOS (Mean Opinion Score) surveys

![Disentanglement Visualization and Experimental Results](/blog/images/projects/voice_conversion_results-3.png)

## Tech Stack

- **Core**: E2E TTS, Neural Vocoder, TensorFlow
- **Duration Control**: Attention Alignment, Teacher-Student Architecture
- **Voice Conversion**: Disentangled Representation, Factorized Hierarchical VAE
- **Domain**: Multi-speaker, Multi-domain Emotional Speech

## Period

April 2018 - March 2020

## Awards

![K-Startup Award](/blog/images/projects/k_startup_award.jpg)
![KAIST Startup Award](/blog/images/projects/kaist_startup_award.jpg)

## Impact

As a co-founder, this work helped establish Humelo as an innovator in AI-driven audio technology. The dual publications at ICASSP demonstrated both the scientific rigor and practical applicability of the research, covering the full spectrum from speech synthesis to voice conversion.

## Publications

- Jungbae Park, Kijong Han, Yuneui Jeong, Sang Wan Lee - "Phonemic-level Duration Control Using Attention Alignment for Natural Speech Synthesis" (ICASSP 2019, Oral, DOI: 10.1109/ICASSP.2019.8683827)
- Mohamed Elgaar, Jungbae Park, Sang Wan Lee - "Multi-speaker and Multi-domain Emotional Voice Conversion Using Factorized Hierarchical Variational Autoencoder" (ICASSP 2020, DOI: 10.1109/ICASSP40776.2020.9054534)
- Hyunmook Park, Jungbae Park, Sang Wan Lee - "End-to-end Trainable Self-Attentive Shallow Network for Text-Independent Speaker Verification" (arXiv:2008.06146, 2020)

## Patents

- Voice conversion system and method (KR 1022772050000)
- Apparatus for synthesizing speech and method thereof (Multiple patents)

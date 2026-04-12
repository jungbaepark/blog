---
title: "Jungbae Park"
---

<div class="profile-hero">
  <img src="/blog/images/profile.jpeg" alt="Jungbae Park" class="profile-photo" />
  <div class="profile-info">
    <h1>Jungbae (Bobby) Park</h1>
    <p class="profile-title">ML Engineer / Research Scientist</p>
    <div class="profile-links">
      <a href="https://linkedin.com/in/jungbaepark/">LinkedIn</a>
      <a href="https://drive.google.com/drive/folders/1CawAwpkrz_sTHtMrI3eT44A57XWS3_fC">Portfolio</a>
      <a href="mailto:jbpark0614@gmail.com">Email</a>
    </div>
  </div>
</div>

---

## About

*"I believe in the brightening and cozy future, led by **cognitive computing**."*

My journey into ML started with curiosity about the brain --- how we think, learn, and perceive the world. At **KAIST**, I studied **Bio & Brain Engineering** with a minor in **Computer Science**, and had the great fortune of being mentored by **Prof. Sang Wan Lee** at the Lab for Brain & Machine Intelligence. Under his guidance, I explored the intersection of neuroscience and AI --- from deep RL for EEG signal processing to multi-agent cognitive policy learning --- which shaped the way I think about intelligent systems today.

That academic foundation led me to co-found **Humelo**, a speech/audio AI startup where I wore many hats (Research Lead, COO, Co-Founder), published at **ICASSP**, showcased AI music at **SXSW**, and learned how to build a company from scratch. From there I moved to **RIIID**, where I built MLOps infrastructure and achieved SOTA on student modeling, before joining **Bucketplace (오늘의집)** --- Korea's largest interior & lifestyle platform --- where I now work across **Search** (ranking, multimodal retrieval, A/B experimentation) and **AIL** (Applied Intelligence Lab --- agentic AI, GenAI workflows, and 3D scene understanding).

Over **7+ years** and three companies, I've shipped production ML systems end-to-end and hold **8 registered patents** with 3 more applied. I also enjoy bridging industry and academia --- **6 papers** at international conferences (CIKM, InterSpeech, ICASSP, IEEE SMC) with 5 more at domestic venues and arXiv.

Beyond R&D, I enjoy inventing, prototyping, mentoring, and creating music.

---

## Core Tech

**Programming**: Python (primary), SQL · Kotlin, Go, C++, Java, JavaScript, Scala, Dart

**ML/DL & AutoML**: PyTorch, TensorFlow, HuggingFace, Lightning AI, XGBoost, LightGBM, LoRA, Optuna, Ray Tune

**Agentic AI & Protocols**: LangChain, LangGraph, ADK, LangFuse, A2A, MCP, Claude Code, Codex, Cursor

**MLOps & Serving**: BentoML, Triton, TorchServe, MLFlow, Airflow (K8s), W&B

**Data & Search**: ElasticSearch, Spark, Athena, BigQuery, Redis, PostgreSQL, MongoDB, Milvus

**Web/App**: FastAPI, Django REST, React, Flutter

**Cloud & CI/CD**: AWS (EC2, S3, ECR, RDS, Lambda), GCP (Cloud Computing, GCS), Docker, GitHub Actions

---

## Education

| | |
|---|---|
| **Ph.D. Student** (Withdrawal) | KAIST, Lab for Brain & Machine Intelligence (2019--2022) |
| **M.S. in Bio & Brain Engineering** | KAIST (2017--2019). Thesis: *Attentional Control Methods for Time-series Data Classification and Synthesis* |
| **B.S. in Bio & Brain Engineering** | KAIST, Minor in Computer Science (2012--2017) |

---

## Selected Publications

| Year | Publication | Venue |
|------|------------|-------|
| 2025 | **MOHPER**: Multi-objective HPO for E-commerce Retrieval | **CIKM** (Applied Research Track) |
| 2023 | Addressing Cold Start for E2E Speech Scoring | **InterSpeech** |
| 2020 | Multi-speaker Emotional Voice Conversion (FHVAE) | **ICASSP** |
| 2019 | Phonemic-level Duration Control for Speech Synthesis (oral) | **ICASSP** |
| 2019 | Polyphonic Sound Event Detection with Transfer Learning | **ICASSP** |
| 2018 | EEG Signal Classification via Deep RL (oral) | **IEEE SMC** |

Plus 5 more publications, 2 arXiv preprints, and a Best Paper Award (KIIS 2016).

---

## Patents (8 Registered, 3 Applied)

**Registered:**

| # | Title | Registration |
|---|-------|-------------|
| I | Adaptive EEG signal processing using reinforcement learning | KR 1023187750000 |
| II | Voice conversion system and method | KR 1022772050000 |
| III | System/device/method to generate polyphonic music | KR 1022274150000 + PCT |
| IV | Training sound event detection model | KR 1021724750000 |
| V | Training sound event detection model | KR 1020256520000 + PCT |
| VI | Apparatus for synthesizing speech | KR 1020579270000 + PCT |
| VII | Apparatus for synthesizing speech | KR 1020579260000 + PCT |
| VIII | Vibration sensor | KR 1012602650000 |

**Applied:**

| # | Title | Application |
|---|-------|------------|
| I | E-commerce retrieval support | KR / US / JP |
| II | Supervised contrastive learning for patch-level temporal representation | KR |
| III | Training sound event detection model | KR |

---

## Work Experience

### Bucketplace (오늘의집) &mdash; ML Engineer <span class="date-tag">Jan 2023 -- Present</span>

**Search & Applied Intelligence Lab (AIL)**

On the **AIL** side, I've led ML-side development of GenAI interior design workflows that achieved **+253% Net Satisfaction**, contributed to scene-to-products retrieval for Digital Twin with **13x recall improvement** (enabling **6000x** cost reduction in Image-to-3D), and I'm currently building an agentic natural language compositional retrieval system for RoomPlanner using LangGraph and A2A. I also built a multi-agent R&D workflow automation plugin (17 agents, 14 skills, cross-model code review).

On the **Search** side, I've architected and shipped **11 A/B experiments (8 winners)** spanning multi-objective ranking HPO (SERP CTR **+0.95%**, published at **CIKM'25**, patent applied), deals ranking (buyer conv up to **+11%**), and CLIP-based hybrid retrieval (Query CTR **+3.03%**, CTCVR **+16%**). I also built the team's ML experiment infrastructure --- offline evaluation, log monitoring, and automated A/B analysis.

### RIIID (뤼이드) &mdash; ML Engineer, Research Scientist <span class="date-tag">Jul 2020 -- Jan 2023</span>

**MLOps & AI Research**

I shipped and operated model registries, dataset pipelines, and distributed training infrastructure serving **4+ EdTech products** (SANTA TOEIC, IVYGlobal SAT, CASA GRANDE, INICIE), improving GPU utilization from **25% to 95%** with the company's first multi-GPU training setup.

On the research side, I achieved **SOTA on student modeling** (dropout prediction, knowledge tracing) via Attentive Conditional Contrastive Learning (ACCL) across 6 benchmarks, and developed a multimodal speech scoring system deployed to SANTA Say (TOEIC Speaking), published at **InterSpeech 2023**. I also presented at **PyCon KR 2021** on multi-domain ML deployment.

### Humelo (휴멜로) &mdash; Research Lead; COO; Co-Founder <span class="date-tag">Apr 2018 -- Jun 2020</span>

**Speech/Audio AI Startup**

I co-founded Humelo and managed **5+ AI R&D projects** --- Emotional TTS (**ICASSP 2019**, oral, 1st author), Voice Conversion (**ICASSP 2020**), Sound Event Detection (**ICASSP 2019**), Speech Emotion Recognition, and AI Music Composition (showcased at **SXSW 2019**, featured on **KBS Documentary**). Published **3 top-venue papers** as 1st or corresponding author.

As COO, I handled HR, finance, and culture, and secured **~$875K** across 3 government R&D grants (IITP, TIPS, Seoul R&BD). The company grew from founding through its Series A stage.

---

<div class="cta-buttons">
  <a href="/blog/projects/" class="cta-btn">View All Projects</a>
</div>

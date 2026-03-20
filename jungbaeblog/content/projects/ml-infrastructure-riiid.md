---
title: "ML Model Registry, Dataset Pipeline & Infrastructure at RIIID (뤼이드)"
date: 2021-09-15
draft: false
tags: ["industrial", "mlops", "mlflow", "airflow", "infrastructure", "riiid"]
categories: ["Industrial Projects"]
summary: "Built ML model registry (MLFlow) and dataset pipelines (Airflow, Athena, BigQuery) at RIIID, serving 4+ products including SANTA TOEIC, IVYGlobal SAT, CASA GRANDE, and INICIE."
weight: 15
cover:
  image: "/blog/images/projects/ml_infra_riiid.png"
  alt: "ML Infrastructure: Model Registry & Pipeline (RIIID)"
  hidden: false
  hiddenInList: false
---

## Overview

At **RIIID (뤼이드)**, built a model registry using MLFlow and dataset pipelines using Airflow, Athena, and BigQuery, serving 4+ products.

## Key Achievements

- Built model registry with MLFlow
- Built dataset pipelines with Airflow, Athena, and BigQuery
- Infrastructure served 4+ products: SANTA TOEIC, IVYGlobal SAT, CASA GRANDE, and INICIE

```mermaid
graph TD
    subgraph Products
        P1[SANTA TOEIC] ~~~ P2[IVYGlobal SAT] ~~~ P3[CASA GRANDE] ~~~ P4[INICIE]
    end
    subgraph Serving
        S1[BentoML] ~~~ S2[Model Registry]
    end
    subgraph Training
        T1[MLFlow] ~~~ T2[Multi-GPU DDP]
    end
    subgraph Pipeline
        L1[Airflow DAGs] ~~~ L2[Dataset Pipeline]
    end
    subgraph Storage
        D1[Athena] ~~~ D2[BigQuery] ~~~ D3[S3]
    end

    Products --> Serving --> Training --> Pipeline --> Storage
```

## Technical Approach

- **Model Registry**: Built on MLFlow for model versioning and experiment tracking
- **Dataset Pipelines**: Orchestrated with Apache Airflow, using AWS Athena and GCP BigQuery for data processing
- **Containerization**: Pipeline components containerized with Docker

## Tech Stack

- **Model Management**: MLFlow
- **Orchestration**: Apache Airflow
- **Data Processing**: AWS Athena, GCP BigQuery
- **Containerization**: Docker
- **Products Served**: SANTA TOEIC, IVYGlobal SAT, CASA GRANDE, INICIE

## Period

January 2021 - September 2021 | RIIID (뤼이드)

## Talks

- **PyCon KR 2021**: "하나의 코드 베이스, 파이프라인으로 여러 도메인에 AI 모델들을 배포할 수 있을까" (Can We Deploy AI Models Across Multiple Domains with a Single Codebase and Pipeline?)

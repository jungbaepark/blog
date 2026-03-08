---
title: "ML Model Registry, Dataset Pipeline & Infrastructure at RIIID (뤼이드)"
date: 2021-09-15
draft: false
tags: ["industrial", "mlops", "mlflow", "airflow", "infrastructure", "riiid"]
categories: ["Industrial Projects"]
---

## Overview

At RIIID (뤼이드), I designed and built the core ML infrastructure that powered the company's AI-driven education products. This involved establishing a centralized model registry using MLFlow and constructing robust dataset pipelines with Apache Airflow, AWS Athena, and GCP BigQuery. The infrastructure served as the backbone for four major products: SANTA TOEIC, IVYGlobal SAT, CASA GRANDE, and INICIE, each targeting different educational markets and standardized tests.

## Key Achievements

- **Multi-Product Support**: Built infrastructure serving **4+ production products** across different educational domains and geographies
- **Model Registry**: Established the company's first centralized MLFlow model registry, enabling reproducible model versioning, experiment tracking, and streamlined deployment
- **Dataset Pipelines**: Designed and deployed end-to-end data pipelines orchestrated by Apache Airflow, handling data ingestion, transformation, and delivery across cloud platforms
- **Cross-Cloud Architecture**: Integrated AWS Athena and GCP BigQuery into a unified pipeline architecture, allowing teams to leverage the strengths of both cloud ecosystems

## Technical Approach

### Model Registry with MLFlow

The model registry was built on MLFlow to address the growing complexity of managing models across multiple products. Each product team needed the ability to track experiments, compare model performance, and promote models through staging to production with confidence. The registry provided a single source of truth for all trained models, their hyperparameters, metrics, and artifacts.

### Dataset Pipeline Architecture

The dataset pipelines were orchestrated using Apache Airflow, with DAGs designed to handle the distinct data requirements of each product. Data from user interactions on SANTA TOEIC, IVYGlobal SAT, CASA GRANDE, and INICIE flowed through extraction layers in AWS Athena and GCP BigQuery, underwent transformation and validation steps, and were delivered to training and evaluation environments in standardized formats.

### Containerized Deployment

All pipeline components and the model registry were containerized with Docker, ensuring consistency across development, staging, and production environments. This also simplified onboarding for new team members and reduced environment-related debugging overhead.

## Tech Stack

- **Model Management**: MLFlow (experiment tracking, model registry, artifact storage)
- **Orchestration**: Apache Airflow (DAG scheduling, dependency management, monitoring)
- **Data Processing**: AWS Athena, GCP BigQuery
- **Containerization**: Docker
- **Products Served**: SANTA TOEIC, IVYGlobal SAT, CASA GRANDE, INICIE

## Impact

The infrastructure I built became the standard ML platform at RIIID (뤼이드), enabling multiple product teams to iterate faster and deploy models with greater confidence. By centralizing model management and automating dataset pipelines, the company reduced duplicated effort across teams and established reliable, auditable processes for moving from experimentation to production. This was especially critical as the company scaled its product portfolio across international markets.

## Period

January 2021 - September 2021

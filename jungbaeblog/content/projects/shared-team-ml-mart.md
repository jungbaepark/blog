---
title: "Design & Development of a Shared Team ML Mart"
date: 2023-06-01
draft: false
tags: ["industrial", "data-quality", "monitoring", "pyspark", "bucketplace"]
categories: ["Industrial Projects"]
summary: "Designed a shared ML feature mart for Bucketplace Search Team with client-side log validation, lag anomaly detection, and automated A/B test analysis pipeline using PySpark and HiveDB."
weight: 10
cover:
  image: "/blog/images/projects/shared_ml_mart.png"
  alt: "Shared ML Feature Mart & Experiment Infrastructure"
  hidden: false
  hiddenInList: false
---

## Overview

At **Bucketplace (오늘의집)**, improved data quality monitoring by implementing client-side log validation and log anomaly detection notifications.

## Key Achievements

- Designed **shared ML feature mart** for the Search Team
- Implemented **client-side log validation** at the ingestion layer
- Built **lag anomaly detection** with automated notifications
- Created **automated A/B test analysis pipeline** for experiment reporting

```mermaid
graph TD
    subgraph Sources[Data Sources]
        S1[Client Logs] ~~~ S2[Server Logs] ~~~ S3[Search Logs]
    end
    subgraph Processing
        P1[Log Validation] ~~~ P2[Anomaly Detection]
    end
    subgraph FeatureMart[Feature Mart]
        F1[Shared ML Features] ~~~ F2[Query Features]
    end
    subgraph Experiment
        E1[Offline Eval] ~~~ E2[A/B Analysis] ~~~ E3[Reporting]
    end

    Sources --> Processing --> FeatureMart --> Experiment
```

## Technical Approach

### Search Mart v2 Pipeline

Designed and built the Search Team's shared ML feature mart (Search Mart v2), consolidating search logs, server logs, and client interaction logs into a unified feature pipeline for downstream ML models and experiment analysis.

![Search Mart v2 Airflow DAG Pipeline](/blog/images/projects/notion_search_mart_diagram.png)

### Client-Side Log Validation

Implemented `DataQualityOperator` for validation at the log ingestion layer, catching schema mismatches, missing fields, and malformed events before they enter the pipeline.

### Log Anomaly Detection

Built automated lag anomaly detection with notification alerts, enabling the team to detect and respond to data freshness issues and pipeline failures proactively.

### Automated A/B Test Analysis

Created a standardized experiment analysis pipeline producing automated reports for Search Team A/B tests — reducing manual analysis effort and ensuring consistent metric computation.

## Tech Stack

- **Data Processing**: PySpark, Athena
- **Data Warehouse**: HiveDB
- **Orchestration**: Airflow (DataQualityOperator)
- **Monitoring**: Anomaly detection, automated alerting

## Period

April 2023 - June 2023 | Bucketplace (오늘의집)

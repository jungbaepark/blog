---
title: "Design & Development of a Shared Team ML Mart"
date: 2023-06-01
draft: false
tags: ["industrial", "data-quality", "monitoring", "pyspark", "bucketplace"]
categories: ["Industrial Projects"]
---

## Overview

At Bucketplace (오늘의집), I designed and developed a shared ML Mart -- a centralized data layer serving machine learning features and datasets across the team. A key focus of the project was improving data quality monitoring by implementing client-side log validation and building log anomaly detection notifications, ensuring that the data feeding into ML models was reliable and trustworthy.

## Key Achievements

- **Client-Side Log Validation**: Implemented validation logic at the log ingestion layer to catch malformed, missing, or inconsistent data before it enters the data warehouse
- **Anomaly Detection Notifications**: Built automated alerting for log anomalies -- sudden volume drops, schema drift, unexpected null rates -- enabling the team to detect and respond to data quality issues proactively rather than discovering them downstream in model performance degradation
- **Shared ML Mart**: Established a centralized, well-documented data mart that multiple team members and models could reliably depend on

## Technical Approach

### Data Quality Monitoring

Data quality is a persistent challenge in production ML systems. Issues at the logging layer -- dropped events, schema changes, instrumentation bugs -- propagate silently through pipelines and manifest as degraded model performance that is difficult to diagnose. This project addressed the problem at two levels:

1. **Client-Side Validation**: Validation rules applied at the point of log ingestion catch structural issues (missing fields, type mismatches, out-of-range values) immediately, preventing corrupt data from entering the pipeline.

2. **Anomaly Detection**: Statistical monitoring of log volumes, field distributions, and null rates detects subtler issues -- a gradual decline in event volume from a particular source, a shift in categorical distributions, or a sudden spike in null values -- and triggers notifications to the team for investigation.

### ML Mart Design

The shared ML Mart was built on HiveDB, with PySpark jobs handling the ETL transformations that produce curated feature tables from raw logs. The mart design emphasized:

- **Consistency**: Standardized schemas and naming conventions across feature tables
- **Discoverability**: Clear documentation and metadata for each table
- **Reliability**: Automated validation and monitoring at every stage of the pipeline

## Tech Stack

- **Data Processing**: PySpark
- **Data Warehouse**: HiveDB
- **Monitoring**: Log anomaly detection, client-side validation

## Impact

The shared ML Mart improved the reliability and velocity of ML development at Bucketplace. By centralizing feature computation and enforcing data quality at the source, the project reduced the time team members spent debugging data issues and increased confidence in model training data. The anomaly detection system caught several data quality incidents early, preventing them from affecting production model performance.

## Period

April 2023 - June 2023 | Bucketplace (오늘의집)

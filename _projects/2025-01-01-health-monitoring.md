---
title: "Large-scale Health Monitoring and User Behavior Analysis"
excerpt: "Lead researcher on the SamenGezond dataset—one of the world's largest preventive health datasets, spanning 7+ years with 83,000+ consented participants."
collection: projects
date: 2025-01-01
---

**Duration**: 2025 -- Present

**Role**: Lead researcher of work package 4: smart data for data analysis and predictive modeling.

**Collaborators**: Menzis (Dutch health insurance company); Prof. dr. Claudine Lamoth (Professor of Movement Analysis & Smart Technology in Aging, Dept. of Human Movement Sciences, UMCG).

## Overview

This project centers on the **SamenGezond** ("Healthy Together") platform, a large-scale preventive health program operated by Menzis. Launched in July 2012 as a website and expanded with a mobile app in October 2017, the platform promotes healthy behaviors across physical activity, nutrition, mental health, sleep, and stress management through a points-based reward system.

The figure below illustrates the end-to-end data pipeline: multimodal data from 5 sources (app usage, mHealth sensors, email engagement, surveys, and clinical demographics) are ingested via Azure Pipelines into a Data Management Platform for aggregation, anonymization, and ETL. Processed data flows into Databricks for feature engineering and ML pipelines, supporting four downstream task categories: prediction (churn, health forecasting, hospitalization risk), classification (user segmentation, risk stratification), anomaly detection (health anomalies, behavioral change, early warning), and recommendation (personalized interventions, nudge optimization, goal setting).

<img src="/assets/images/projects/flowchart1.jpg" alt="SamenGezond Multi-modal Health Data Pipeline" width="100%">
<em>Figure 1. SamenGezond multi-modal health data pipeline: from data sources through Azure and Databricks to downstream ML tasks.</em>

## Dataset

- **Observation period**: July 2012 -- September 2019 (376 weeks, ~7.2 years)
- **Participants**: 83,466 consented adults (from ~838,500 enrolled users), aged 18--80 (mean 46.5 years), 56% female
- **Average enrollment duration**: ~3.6 years per participant
- **Temporal granularity**: Weekly

**Data modalities include**:
- Demographics (age, gender)
- Wearable sensor recordings (physical activity, sleep, heart rate)
- Health surveys and questionnaires
- Platform interaction logs (GPS-tracked exercises, goal-setting, AI coaching, social challenges)
- Insurance records
- Neighborhood-level socioeconomic status (NSES), derived from 9 indicators via the Dutch Central Bureau of Statistics
- Marketing campaign temporal markers (radio, TV, web)

The bubble chart below compares SamenGezond against 34 other health datasets across three dimensions: number of participants (x-axis), observation duration (y-axis), and number of data modalities (bubble size). SamenGezond stands out with its combination of large participant count (83,466), long duration (7.2 years), and high modality richness (26 modalities).

<img src="/assets/images/projects/bubble_chart_34datasets.png" alt="Health Dataset Landscape: Participants vs. Duration vs. Modalities" width="100%">
<em>Figure 2. Health dataset landscape comparing participants, duration, and modalities. SamenGezond (highlighted) combines large scale, long duration, and high modality count.</em>

The table below summarizes participant demographics across the pre-training, downstream activity, and downstream metabolic task splits, covering sex, age, and BMI distributions.

<img src="/assets/images/projects/demographics_table.jpg" alt="Demographics of SamenGezond datasets" width="100%">
<em>Figure 3. Demographics (sex, age, BMI) across pre-training and downstream task datasets.</em>

## Participant Typology

Four distinct adoption types were identified based on when participants enrolled on the website and whether they subsequently adopted the mobile app after its October 2017 launch:

- **Type 1** (32.2%): Enrolled before app launch, website only
- **Type 2** (37.5%): Enrolled before app launch, later adopted the app
- **Type 3** (15.6%): Enrolled after app launch, adopted both website and app
- **Type 4** (14.7%): Enrolled after app launch, website only

<img src="/assets/images/projects/participant_types.png" alt="Participant adoption typology timeline" width="100%">
<em>Figure 4. Participant adoption typology across the pre-app era (2012--2017) and post-app era (2017--2019), showing web enrollment, app adoption timing, and right censoring.</em>

## Key Characteristics

- **Socioeconomic stratification**: Participants stratified into NSES quintiles, enabling analysis of health behavior adoption across socioeconomic segments.
- **Naturalistic design**: Observational (non-experimental), capturing genuine user decision-making and adoption behaviors.
- **Ethics**: Voluntary informed consent; IRB-approved by the University of Groningen; reported following STROBE guidelines.

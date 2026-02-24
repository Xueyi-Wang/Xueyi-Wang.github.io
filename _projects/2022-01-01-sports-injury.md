---
title: "Sports Injury Prediction and Prevention for Professional Athletes"
excerpt: "Machine learning-based injury prediction for competitive runners, using 7 years of training data from 74 athletes with ~600 injury events."
collection: projects
date: 2022-01-01
---

**Duration**: 2022 -- 2023

## Overview

Staying injury-free is critical for athletic success, yet injuries remain notoriously difficult to predict. This project leverages machine learning to forecast injuries in competitive middle- and long-distance runners, using one of the largest and most detailed training-log datasets in the running injury literature — spanning **7 years** of data from **74 high-level athletes** with nearly **600 injury events**.

## Motivation

Traditional statistical methods (e.g., logistic regression) have shown limited success in predicting sports injuries, largely because they cannot capture the complex, nonlinear interactions among training-load variables. Meanwhile, prior machine learning studies were constrained by small datasets and coarse feature representations. This project addresses both issues by:

- Collecting a rich, multi-year longitudinal dataset with both **objective** (GPS watch) and **subjective** (perceived exertion, recovery, training success) features.
- Modeling training load at two temporal granularities — **daily** and **weekly** — to capture both acute and chronic load patterns.

## Dataset

| Property | Detail |
|---|---|
| Athletes | 74 competitive runners (27 women, 47 men) |
| Period | 2012–2019 (7 years) |
| Distances | 800 m to marathon |
| Healthy events | ~42,000 |
| Injury events | ~580 (~1.4% of total) |
| Data sources | GPS watch (distance, duration, heart rate zones), subjective ratings (exertion, recovery, training success), strength & cross-training logs |

## Methodology

### Two Approaches to Feature Construction

We designed two complementary modeling strategies to capture training load at different time scales:

- **Day Approach (micro-level):** Each of the 7 days before the event is described by 10 features (distance by heart rate zone, sprinting distance, strength sessions, cross-training hours, and three subjective ratings), yielding a **70-dimensional** feature vector that preserves the temporal sequence of daily training.

- **Week Approach (macro-level):** The 3 weeks before the event are each summarized by 22 aggregated features (totals, maxima, session counts, etc.), plus 3 features capturing relative changes in weekly mileage, yielding a **69-dimensional** feature vector.

### Machine Learning Pipeline

- **Algorithm:** XGBoost (Extreme Gradient Boosting) with Platt scaling calibration
- **Class imbalance handling:** Bagging with 9 balanced sub-models (2048 injury + 2048 healthy samples each)
- **Normalization:** Per-athlete z-score normalization based on healthy events
- **Evaluation:** Temporal hold-out — trained on the first 64 athletes, tested on the 10 most recently joined

## Results

| Approach | Specificity | Sensitivity | AUC |
|---|---|---|---|
| **Day** | 0.741 | 0.584 | **0.724** |
| **Week** | 0.746 | 0.504 | 0.678 |

The **Day approach** consistently outperforms the Week approach, indicating that fine-grained daily training patterns in the week preceding an injury carry the strongest predictive signal. Notably, at a 10% false-positive rate, the Day model can still detect approximately 30% of injuries — a practically valuable trade-off given the high cost of injuries vs. the low cost of a precautionary rest day.

### Model Calibration

After Platt scaling, both models produce well-calibrated risk scores that neither overestimate nor underestimate injury probability, enabling meaningful interpretation of the output as actual risk levels.

### Feature Importance

Key findings from the feature importance analysis:

- **Day approach:** High-intensity distance (Z5–T1–T2) on the day before the injury is the single most important feature, followed by perceived training success and perceived recovery. This highlights the interplay between objective load and subjective well-being.
- **Week approach:** Subjective features (average/minimum training success) dominate, alongside maximum single-day distance and relative weekly mileage increases.
- Individual feature correlations with injury are weak (r < 0.07), confirming that injuries arise from **complex multi-variable interactions** rather than any single factor — underscoring the value of machine learning over simple correlation-based methods.

## Practical Applications

The system is designed as a **coach-assistance tool**, providing a continuous injury risk score between 0 and 1 for each athlete before each training session. Coaches can:

- **Adjust training load** when risk scores are elevated (e.g., prescribe rest or reduce intensity)
- **Tune the decision threshold** based on context — a lower threshold (higher sensitivity) may be appropriate close to major competitions
- **Combine model output** with their own expertise and knowledge of each athlete's injury history

## Key Takeaways

1. **Machine learning can meaningfully predict running injuries** from training logs, achieving AUC scores above 0.7 — considered a strong effect in sports science.
2. **Daily-level modeling outperforms weekly aggregation**, suggesting that the temporal sequence of training in the days before an injury is highly informative.
3. **Injuries are driven by complex feature interactions**, not single variables — classical regression methods miss these patterns.
4. **Both objective and subjective training data matter** — perceived recovery and training success are among the top predictive features.
5. The approach is **generalizable** and can be adapted by other running teams or sports with comparable data collection.

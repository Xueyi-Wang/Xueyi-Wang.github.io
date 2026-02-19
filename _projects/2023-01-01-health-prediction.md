---
title: "Interpretable and Personalized Health Prediction System"
excerpt: "Developed an end-to-end health prediction system using smartwatch data with an Adaptive Spatial-Temporal Interpretable framework for stress and sleep prediction."
collection: projects
date: 2023-01-01
---

## Overview

**Duration**: 2023 -- 2025

Developed an end-to-end health prediction system using smartwatch data. Proposed an Adaptive Spatial-Temporal Interpretable framework for accurate stress and sleep prediction despite data sparsity. Adapts to diverse user profiles (age, gender, behavior) to mitigate domain shift, while revealing key contributing factors for personalized health recommendations.

- **Personalized Sleep Prediction** -- A two-stage adaptive spatial-temporal model for interpretable and personalized sleep quality prediction from sparse wearable data.
  <br>***Wang, X.**, Claudine J. C. Lamoth, & Wilhelm, E. (2025). Personalized and interpretable sleep prediction via two stage adaptive spatial-temporal model. arXiv:2509.06974, under review.*
- **Adaptive Stress Prediction** -- An online adaptive learning framework for interpretable and personalized stress prediction using multivariate and sparse physiological signals.
  <br>***Wang, X.**, Claudine J. C. Lamoth, & Wilhelm, E. (2026). AdaptStress: Online Adaptive Learning for Interpretable and Personalized Stress Prediction Using Multivariate and Sparse Physiological Signals. Under review.*
- **Deep Adaptive Spatiotemporal Modeling** -- Personalized sleep prediction via deep adaptive spatiotemporal modeling from sparse wearable sensor data.
  <br>***Wang, X.**, Lamoth, C. J. C., & Wilhelm, E. (2025). Personalized sleep prediction via deep adaptive spatiotemporal modeling and sparse data. 47th Annual International Conference of the IEEE Engineering in Medicine and Biology Society (EMBC). IEEE, 2025.*
- **Multivariate Stress Forecast** -- Stress forecasting from sparse data collected during lifestyle interventions using multivariate wearable signals.
  <br>***Wang, X.**, Bellink, C., Lamoth, C., & Wilhelm, E. (2024). Multivariate stress forecast from sparse data during lifestyle interventions. IEEE International Conference on E-health Networking, Application & Services (HealthCom).*
- **Personalized Stress Forecasting** -- Personalized stress forecasting utilizing multivariate sparse data from wearable devices.
  <br>***Wang, X.**, Lamoth, C. J. C., & Wilhelm, E. (2025). Personalized stress forecasting utilizing multivariate sparse data. 10th Dutch Bio-Medical Engineering Conference.*

---

## Key Challenge: Domain Shift Across Users

A core challenge in wearable health prediction is the significant domain shift across different users. Due to individual differences in physiology, lifestyle, and behavior, data distributions vary drastically between subjects, making it difficult for a single model to generalize.

<img src="https://arxiv.org/html/2509.06974v1/x1.png" alt="Illustration of domain adaptation for data from various subjects and conditions" width="100%">

*Figure: Illustration of domain adaptation for data from various subjects and conditions. The model adapts from source domains (training users) to target domains (new users) to handle individual variability.*

<img src="https://arxiv.org/html/2509.06974v1/x3.png" alt="Domain shifts for features from different subjects by PCA" width="100%">

*Figure: Domain shifts visualized via PCA -- features from different subjects exhibit distinct distributions, motivating the need for personalized adaptation.*

---

## Adaptive Spatial-Temporal Model

We proposed a two-stage adaptive spatial-temporal architecture that captures both spatial interactions among multivariate features and temporal dependencies across time steps, combined with a domain adaptation strategy for personalization.

<img src="https://arxiv.org/html/2509.06974v1/x4.png" alt="Flowchart of the adaptive spatial-temporal model" width="100%">

*Figure: Flowchart of the adaptive spatial-temporal model with optional two-stage domain adaptation. Stage 1 performs training-time adaptation to reduce overfitting; Stage 2 applies source-free test-time adaptation for new users without requiring labels.*

---

## Results

The model achieved strong performance across multiple prediction horizons, outperforming baselines including LSTM, Informer, PatchTST, and TimesNet.

<img src="https://arxiv.org/html/2509.06974v1/x6.png" alt="Comparison of models performance" width="100%">

*Figure: Comparison of all participants' MAE, MSE, and RMSE across different models (3-day input, 1-day prediction window). Our model consistently achieves the lowest error.*

---

## Interpretability via SHAP Analysis

Beyond prediction accuracy, interpretability is essential for clinical trust. We used SHAP analysis to reveal which features most influence sleep quality predictions and in which direction.

<img src="https://arxiv.org/html/2509.06974v1/x7.png" alt="Feature importance analysis by SHAP" width="100%">

*Figure: Feature importance analysis with impact direction via SHAP. Each dot represents a data point; color indicates feature value (red = high, blue = low); position shows impact on prediction.*

---

## Related Publications

1. **Wang, X.**, Claudine J. C. Lamoth, & Wilhelm, E. (2026). AdaptStress: Online Adaptive Learning for Interpretable and Personalized Stress Prediction Using Multivariate and Sparse Physiological Signals. *Under review*.

2. **Wang, X.**, Claudine J. C. Lamoth, & Wilhelm, E. (2025). Personalized and interpretable sleep prediction via two stage adaptive spatial-temporal model. *arXiv:2509.06974, under review*.

3. **Wang, X.**, Lamoth, C. J. C., & Wilhelm, E. (2025). Personalized sleep prediction via deep adaptive spatiotemporal modeling and sparse data. *47th Annual International Conference of the IEEE Engineering in Medicine and Biology Society (EMBC)*. IEEE, 2025.

4. **Wang, X.**, Lamoth, C. J. C., & Wilhelm, E. (2025). Personalized stress forecasting utilizing multivariate sparse data. *10th Dutch Bio-Medical Engineering Conference*.

5. **Wang, X.**, Bellink, C., Lamoth, C., & Wilhelm, E. (2024). Multivariate stress forecast from sparse data during lifestyle interventions. *IEEE International Conference on E-health Networking, Application & Services (HealthCom)*.

---
title: "Fall Detection Research By Egocentric Cameras"
excerpt: "Designed and built the EGOFalls multimodal fall detection benchmark dataset from an egocentric perspective, now open-sourced and adopted by multiple international teams."
collection: projects
date: 2019-01-01
---

## Overview

Fall-related injuries are a leading cause of accidental death and hospitalization, especially among the elderly. Traditional fall detection systems rely on wearable sensors or fixed ambient cameras, which suffer from limited coverage, privacy concerns, or user discomfort.

This project explores a **non-intrusive, first-person vision approach** to fall detection using body-worn egocentric cameras. Over the course of five years (2019--2024), we built a comprehensive research pipeline spanning dataset creation, novel algorithm design, and multi-modal fusion:

- **EGOFALLS Dataset** -- One of the first large-scale visual-audio fall detection benchmarks from an egocentric perspective, now open-sourced and adopted by multiple international research teams.
- **Event Camera + Spiking Neural Network** -- A visual-audio fusion framework combining neuromorphic event cameras with spiking neural networks, achieving robust detection across diverse environmental and lighting conditions.
- **Literature Survey** -- A comprehensive survey of elderly fall detection systems, providing a structured taxonomy of existing approaches.

---

## EGOFALLS Dataset

EGOFALLS is a visual-audio dataset and benchmark for fall detection using egocentric cameras, covering 12 activity types including 4 kinds of falls and 8 kinds of non-falls.

![Examples of 12 activities, including four kinds of falls and eight kinds of non-falls.](https://github.com/Xueyi-Wang/EGOFALLS/assets/55747740/fc7cc58f-1c8e-4c08-8da5-4b9caef27134)

### Data Collection

| Item | Detail |
|------|--------|
| **Duration** | 2018 -- 2022 |
| **Location** | Groningen, Netherlands |
| **Equipment** | OnReal G1 (RGB), CAMMHD Bodycams (RGB and Infrared) |
| **Subjects** | 14 (12 male, 2 female), age 20--60 |
| **Camera Position** | Neck and Waist |
| **Environment** | Indoor and Outdoor |
| **Modalities** | Vision and Audio |

### Dataset Structure

Quantity and type of video clips per participant (C1 and C2 refer to camera 1 and camera 2):

<img width="1108" alt="Data overview" src="https://github.com/Xueyi-Wang/EGOFALLS/assets/55747740/f855201d-8b08-472e-bba5-533b0d43045f">

The dataset is organized within individual directories corresponding to each subject:

<img width="786" alt="Subject directories" src="https://github.com/Xueyi-Wang/EGOFALLS/assets/55747740/63960f60-3b3e-4292-9292-d83c25f90076">

The data follows a hierarchical structure:

<img width="712" alt="Hierarchical structure" src="https://github.com/Xueyi-Wang/EGOFALLS/assets/55747740/1be4c4ab-fb3f-4107-abc9-74667e671ea9">

---

## Related Publications

1. **Wang, X.** (2024). Egofalls: A visual-audio dataset and benchmark for fall detection using egocentric cameras. *International Conference on Pattern Recognition (ICPR)*.

2. **Wang, X.**, Talavera, E., Karastoyanova, D., & Azzopardi, G. (2023). Fall detection with a non-intrusive and first-person vision approach. *IEEE Sensors Journal*.

3. **Wang, X.**, Risi, N., Talavera, E., Chicca, E., Karastoyanova, D., & Azzopardi, G. (2023). Fall detection with event-based data: A case study. *International Conference on Computer Analysis of Images and Patterns (CAIP)*, pp. 33-42.

4. **Wang, X.**, Talavera, E., Karastoyanova, D., & Azzopardi, G. (2021). Fall detection and recognition from egocentric visual data: A case study. *International Conference on Pattern Recognition (ICPR)*, pp. 431-443.

5. **Wang, X.**, Ellul, J., & Azzopardi, G. (2020). Elderly fall detection systems: A literature survey. *Frontiers in Robotics and AI*, 7, 71.

---

## Links

- [GitHub Repository](https://github.com/Xueyi-Wang/EGOFALLS)

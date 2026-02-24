---
title: "Multimodal Epileptic Seizure Detection System -- SeizeIT2"
excerpt: "Algorithm developer in the EU multi-center SeizeIT2 project — the first-ever phase-4 clinical trial for wearable seizure monitoring, with 11,640 hours of data from 125 patients."
collection: projects
date: 2024-01-01
---

**Duration**: 2024 -- 2025

**Role**: Algorithm developer for multimodal fusion and model compression.

**Collaborators**: International collaboration with KU Leuven, UCL, Aarhus University, and clinical sites across Europe (EU multi-center clinical project).

## Overview

The **SeizeIT2** project is an international multicenter clinical trial ([NCT04284072](https://clinicaltrials.gov/study/NCT04284072)) — the **first-ever phase-4 clinical trial** for a wearable device targeting in-home seizure monitoring. The project unites public and private stakeholders across Europe to address an unmet clinical need: reliable, continuous seizure detection using non-invasive wearable sensors in real-world settings.

This project is a continuation of the [SeizeIT1](https://rdr.kuleuven.be/dataset.xhtml?persistentId=doi:10.48804/P5Q0OJ) ICON project, expanding the scope to a much larger patient cohort and multimodal sensor setup.

Developed attention-based multimodal deep learning algorithms for neurophysiological signal analysis, with cross-modal feature fusion strategies to improve seizure detection accuracy and robustness. Explored model compression techniques to enable deployment on resource-constrained edge devices.

## Clinical Partners

Data was collected across **5 European Epilepsy Monitoring Units (EMUs)**:

| Center | Country |
|---|---|
| University Hospital Leuven (incl. pediatric patients) | Belgium |
| Freiburg University Medical Center | Germany |
| RWTH University of Aachen | Germany |
| Karolinska University Hospital | Sweden |
| Coimbra University Hospital | Portugal |

Data collection spanned from **January 2020** to **June 2022**, approved by the UZ Leuven ethics committee (approval ID: S63631).

## Dataset

| Property | Detail |
|---|---|
| **Patients** | 125 (51 female, 41%) with focal epilepsy |
| **Total recording time** | ~11,640 hours of wearable data |
| **Total seizures** | 886 focal seizures |
| **Mean seizure duration** | 58 seconds (range: 3 sec – 16 min) |
| **Modalities** | 4 (behind-the-ear EEG, ECG, EMG, accelerometer/gyroscope) |
| **Environment** | Hospital video-EEG monitoring |

## Multimodal Wearable Sensor Setup

The recording setup consists of two Sensor Dot (SD) wearable devices:

- **Behind-the-ear EEG (bte-EEG):** Two Ag/AgCl cup electrodes placed on the mastoid bone (corresponding to T7/T8 and P9/P10 positions), creating two bipolar channels — one per hemisphere.
- **ECG:** Two electrodes on the left chest measuring cardiac activity.
- **EMG:** Two electrodes on the left deltoid muscle capturing muscle activity.
- **Motion (ACC + GYRO):** Both SD modules contain built-in accelerometers and gyroscopes for movement monitoring.

All participants have wearable bte-EEG recordings. In approximately 3% of cases, ECG/EMG/motion data were unavailable due to technical issues. Concurrent **video-EEG** monitoring with a standardized 25-electrode array served as the gold-standard reference for seizure annotation.

## Seizure Distribution

### By Seizure Type

| Type | Count | Percentage |
|---|---|---|
| Focal Aware (FA) | 317 | 35.8% |
| Focal Impaired Awareness (FIA) | 393 | 44.4% |
| Focal-to-Bilateral Tonic-Clonic (FBTC) | 55 | 6.2% |
| Focal with unclear awareness | 12 | 1.4% |
| Subclinical focal | 2 | 0.2% |
| Unknown / unreported onset | 93 | 10.5% |

### By Hemisphere Onset

| Hemisphere | Percentage |
|---|---|
| Left | 44% |
| Right | 12% |
| Bilateral | 1% |
| Unclear | 43% |

Seizure onsets were distributed across the central, frontal, temporal, occipital, parietal, and insular lobes, with a **predominance of temporal lobe seizures (30%)**. About 26% of seizures could not be paired with a clear onset lobe.

## Deliverables

- Participated in the SeizeIT2 Seizure Detection Challenge.
- Presented results at multiple consortium meetings.
- Attended and presented at the final SeizeIT2 workshop.

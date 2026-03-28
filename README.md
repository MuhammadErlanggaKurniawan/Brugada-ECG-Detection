# Brugada-ECG-Detection

# Clinically-Informed Brugada ECG Detection

This repository contains our work on Brugada syndrome detection using morphology-aware models and deep learning under limited data conditions.

## Dataset
Brugada-HUCA dataset (describe access policy here).

## Methods
- Generic ML baseline
- Morphology-aware models
- CNN on V1-V3 and 12-lead ECG

## Main Results
- Best morphology-aware model: LightGBM + GA
- Best deep learning model: CNN V1-V3

## Repository Structure
- `src/`: source code
- `notebooks/`: exploratory and experiment notebooks
- `results/`: summarized outputs
- `reports/`: technical report

## How to Run
```bash
pip install -r requirements.txt
# Clinically-Informed Brugada ECG Detection

This repository contains our solution for Brugada syndrome detection using ECG signals, developed for IDSC 2026.

## Overview
Brugada syndrome is a cardiac condition associated with a high risk of sudden cardiac death. This project explores different modeling approaches under limited data conditions, including:

- Generic machine learning baselines
- Morphology-aware feature-based models
- Deep learning (1D CNN) on ECG signals

## Dataset
- Total patients: 356
- Classes: Normal vs Brugada
- 12-lead ECG signals (10 seconds, 100 Hz)

> Note: Raw data is not included in this repository due to access restrictions.

## Methods

### 1. Preprocessing
- Bandpass filtering (0.5–40 Hz)
- Signal normalization
- Patient-level train/test split

### 2. Model Families
- **Generic ML**: Logistic Regression, Random Forest, XGBoost
- **Morphology-aware**: Feature extraction (QRS, ST, T-wave) + XGBoost / LightGBM (GA)
- **Deep Learning**: 1D CNN (V1–V3 and 12-lead)

### 3. Evaluation
- ROC-AUC
- F1-score
- Sensitivity
- Specificity

## Results

- Best overall model: **LightGBM + Genetic Algorithm**
- CNN (V1–V3) achieved competitive performance
- CNN (12-lead) showed unstable behavior under limited data

## Repository Structure
├── figures/ # Visualizations and plots
├── Notebooks/ # Experiment notebooks
├── Reports/ # Technical report
├── Results/ # Model outputs and metrics
├── requirements.txt
└── README.md

## How to Run

Install dependencies:
```bash
pip install -r requirements.txt
Run notebooks:

Open files in Notebooks/ using Jupyter or Colab
Authors
Muhammad Erlangga Kurniawan
Teuku Muhammad Rizky Ardiansyah

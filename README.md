# 🧬 Microsatellite Entropy Analysis & ML Classification Pipeline

[![Jupyter Notebook](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter)](microsatellites_analysis_ML.ipynb)
[![Python 3.8+](https://img.shields.io/badge/Python-3.8+-blue?logo=python)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

A reproducible Jupyter Notebook pipeline for analyzing microsatellite (STR) data using information theory, automated annotation correction, and machine learning for stability classification.

## 📖 Overview

This project provides an end-to-end analytical workflow for microsatellite instability (MSI) research. It transforms raw STR proportion data from Excel into actionable insights by:

- ✅ Calculating **Shannon entropy** and statistical features for each sample
- ✅ Automatically **correcting expert annotations** using entropy-based thresholds
- ✅ Training and evaluating **Machine Learning models** (Random Forest, XGBoost)
- ✅ Generating publication-ready **visualizations and audit reports**

## 🚀 Features

- **Automated Data Extraction**: Robust parsing of structured STR Excel files with dynamic offset handling and NaN fallback
- **Entropy-Driven QC**: Identifies and corrects mislabeled samples (`S` → `N`) using conservative IQR/STD thresholds
- **Feature Engineering**: Converts raw proportions into ML-ready features (entropy, std, peak proportions, one-hot STR encoding)
- **Model Training & Evaluation**: Supports `RandomForest` and `XGBoost` with stratified train/test splits and comprehensive metrics
- **Comprehensive Reporting**: Confusion matrices, classification reports, feature importance plots, and JSON correction audits
- **Reproducible & Modular**: Phase-based notebook structure for easy adaptation to new datasets or custom thresholds

## 📂 Repository Contents

- `microsatellites_analysis_ML.ipynb`: The main Jupyter Notebook containing the complete analysis pipeline.
- `MSI1.xlsx`: A sample dataset in Excel format containing raw STR proportions for analysis.
- `README.md`: This file.

## 📦 Installation

### Prerequisites

- Python `3.8+`
- `pip` or `conda`

### Dependencies

```bash
pip install pandas numpy matplotlib seaborn scikit-learn xgboost openpyxl jupyter

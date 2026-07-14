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

Setup Instructions
Clone the repository:

bash
git clone https://github.com/VladAgapov1969/cancer_microsatellites_analysis_ML.git
cd cancer_microsatellites_analysis_ML

(Optional but recommended) Create a virtual environment:

bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
Install dependencies:

bash
pip install pandas numpy matplotlib seaborn scikit-learn xgboost openpyxl jupyter

Running the Pipeline
Launch Jupyter Notebook from your terminal:

bash
jupyter notebook
In the Jupyter interface, navigate to and open the microsatellites_analysis_ML.ipynb file.

Execute the cells in order. The notebook is clearly divided into phases (Data Loading, EDA, Feature Engineering, Modeling) for easy navigation.

All outputs—including figures, model metrics, and the correction audit JSON—will be generated within the notebook.

🧠 Methodology

Here is the complete, unified README.md file. I have merged your original content with my suggested improvements, preserving all your key points while enhancing the structure, clarity, and professional detail.

You can copy and paste the entire block below into your README.md file.

markdown
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
Setup Instructions
Clone the repository:

bash
git clone https://github.com/VladAgapov1969/cancer_microsatellites_analysis_ML.git
cd cancer_microsatellites_analysis_ML
(Optional but recommended) Create a virtual environment:

bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
Install dependencies:

bash
pip install pandas numpy matplotlib seaborn scikit-learn xgboost openpyxl jupyter
▶️ Running the Pipeline
Launch Jupyter Notebook from your terminal:

bash
jupyter notebook
In the Jupyter interface, navigate to and open the microsatellites_analysis_ML.ipynb file.

Execute the cells in order. The notebook is clearly divided into phases (Data Loading, EDA, Feature Engineering, Modeling) for easy navigation.

All outputs—including figures, model metrics, and the correction audit JSON—will be generated within the notebook.

🧠 Methodology
The workflow follows a structured scientific pipeline:

Data Loading: Reads the Excel file, performs initial cleaning, and selects relevant features.

Exploratory Analysis & Annotation Correction:

Calculates Shannon entropy for each sample as a measure of complexity.

Identifies outliers in the entropy distribution.

Flags and corrects samples where the expert annotation (S or N) does not align with the entropy-based threshold.

Feature Engineering: Constructs a robust feature set for model training.

Model Training & Evaluation: Trains and compares the performance of Random Forest and XGBoost classifiers using a hold-out test set and reports standard metrics.

Results Visualization: Generates key plots (feature importance, confusion matrices) to interpret model decisions.

📊 Example Results
After successfully running the notebook, you can expect:

A corrected annotation report: A JSON file detailing which samples were reclassified.

Model Performance Metrics: Printed outputs showing accuracy, precision, recall, and F1-score for both models.

Visualization Panels:

Bar charts of feature importance.

Heatmaps of confusion matrices.

Distribution plots of the corrected annotations.

Note: Exact results will vary based on the input dataset.

🤝 Contributing
Contributions are welcome! If you find a bug, have a suggestion, or want to extend the pipeline, please open an issue or submit a pull request.

Fork the repository.

Create your feature branch (git checkout -b feature/your-amazing-feature).

Commit your changes (git commit -m 'Add some amazing feature').

Push to the branch (git push origin feature/your-amazing-feature).

Open a Pull Request.

📄 License
This project is open-source and available under the MIT License.

👤 Author
Dr. Vladislav Agapov (VladAgapov1969)

📬 Citation
If you use this code or pipeline in your research, please consider citing the repository:

bibtex
@misc{agapov2026microsatelliteML,
  author = {Vladislav Agapov},
  title = {Microsatellite Entropy Analysis & ML Classification Pipeline},
  year = {2026},
  publisher = {GitHub},
  journal = {GitHub Repository},
  howpublished = {\url{https://github.com/VladAgapov1969/cancer_microsatellites_analysis_ML}}
}


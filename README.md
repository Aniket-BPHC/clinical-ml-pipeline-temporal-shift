# Clinical ML Pipeline Under Temporal Shift

An end-to-end machine learning system for clinical prediction using electronic health record (EHR) data. The project focuses on building interpretable predictive models, evaluating their robustness under temporal distribution shift, and studying the effectiveness of continual learning on newer patient populations through an interactive Streamlit dashboard.

---

## Overview

Machine learning models in healthcare often experience performance degradation when deployed on patient populations that differ from the data they were originally trained on. This project investigates that challenge by constructing a complete clinical ML pipeline and evaluating model behavior across historical and current cohorts.

The project includes:

* EHR data integration from multiple clinical tables
* Feature engineering and patient-level aggregation
* Exploratory Data Analysis (EDA)
* Temporal dataset splitting
* Supervised learning for disease prediction
* Feature importance analysis
* Bias-variance analysis
* Continual learning experiments
* Interactive dashboard for model exploration

---

## Problem Statement

Given patient demographics, observations, and diagnosed conditions, build predictive models that can identify clinically relevant conditions while analyzing how model performance changes over time.

The project specifically investigates:

* How well models generalize across temporal shifts
* Which features drive predictions
* Whether retraining on newer data improves performance
* Trade-offs between model complexity and generalization

---

## Dataset

The project uses a synthetic Electronic Health Record (EHR) dataset derived from Synthea.

Data sources include:

* Patient demographics
* Clinical observations
* Medical conditions

These tables are merged and transformed into patient-level feature vectors suitable for machine learning.

Expected directory structure:

```
synthea-mimic/
└── csv/
├── patients.csv
├── observations.csv
└── conditions.csv
```

---

## Feature Engineering

The pipeline performs extensive preprocessing and feature construction, including:

* Patient-level aggregation of clinical observations
* Missing value handling
* Temporal filtering
* Condition frequency analysis
* Target label generation
* Numerical feature extraction

The resulting dataset is used for both binary and multilabel prediction tasks.

---

## Models Implemented

### Decision Tree

Interpretable tree-based classifier used as a baseline model.

### Support Vector Machine (SVM)

Kernel-based classifier for capturing non-linear decision boundaries.

### Multi-Layer Perceptron (MLP)

Neural network model for learning complex feature interactions.

---

## Evaluation Framework

Models are evaluated using:

* Accuracy
* Precision
* Recall
* F1 Score
* ROC Analysis
* Confusion Matrices

Performance is compared across both historical and current patient cohorts.

---

## Temporal Shift Analysis

A key objective of this project is understanding temporal drift.

The dataset is divided into:

* Dataset 1 (Historical Cohort)
* Dataset 2 (Current Cohort)

Models trained on historical data are evaluated on newer data to measure robustness under distributional change.

This enables analysis of:

* Generalization performance
* Dataset drift
* Model degradation over time

---

## Continual Learning

The project investigates whether retraining models on newer patient records improves performance.

Experiments compare:

* Original model performance
* Performance after exposure to Dataset 2
* Adaptation effectiveness under temporal drift

---

## Dashboard Features

The Streamlit dashboard provides:

### Data Exploration

* Dataset statistics
* Class distributions
* Clinical feature summaries

### Model Training

* Model selection
* Hyperparameter controls
* Interactive experimentation

### Model Evaluation

* Classification metrics
* ROC curves
* Confusion matrices

### Feature Interpretation

* Feature importance rankings
* Model explainability views

### Temporal Analysis

* Historical vs current cohort comparison
* Temporal drift visualization

### Continual Learning Analysis

* Before and after retraining comparisons
* Performance tracking across datasets

---

## Repository Structure

```
.
├── clinical_ml_dashboard.py
├── requirements.txt
├── README.md
├── assets/
│   └── screenshots/
└── synthea-mimic/
└── csv/
```

---

## Installation

Install dependencies:

```
pip install -r requirements.txt
```

---

## Running the Dashboard

Launch the Streamlit application:

```
streamlit run clinical_ml_dashboard.py
```

The dashboard will open locally in your browser.

---

## Technologies Used

* Python
* Streamlit
* Pandas
* NumPy
* Scikit-learn
* Matplotlib
* Seaborn

---

## Key Learning Outcomes

* Healthcare machine learning workflows
* Feature engineering on structured EHR data
* Model evaluation under temporal shift
* Continual learning techniques
* Interactive ML dashboard development
* Model interpretation and explainability

---

## Future Improvements

Potential extensions include:

* Advanced continual learning methods
* Ensemble learning approaches
* SHAP-based model explanations
* Calibration analysis
* Real-world healthcare datasets
* Automated hyperparameter optimization

---

## Author

Aniket Shukla

Computer Science, BITS Pilani Hyderabad

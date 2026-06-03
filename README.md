# Clinical ML Pipeline Under Temporal Shift

An end-to-end machine learning pipeline for clinical prediction using Electronic Health Record (EHR) data. The project focuses on feature engineering, predictive modeling, temporal distribution shift analysis, continual learning, and model interpretability through an interactive Streamlit dashboard.

---

## Overview

Machine learning models deployed in healthcare often experience performance degradation when the underlying patient population changes over time. This project investigates that challenge by building a complete clinical prediction pipeline and evaluating model performance across historical and current patient cohorts.

The system includes:

* EHR data integration and preprocessing
* Patient-level feature engineering
* Temporal train-test splitting
* Clinical condition prediction
* Model comparison and evaluation
* Temporal shift analysis
* Continual learning experiments
* Interactive Streamlit dashboard

---

## Dataset

This project uses a synthetic Electronic Health Record (EHR) dataset generated using Synthea.

Dataset download:

https://drive.google.com/drive/u/2/folders/1d7QielEDfhua8YfU77U0EmPF048LEcLv

After downloading, place the dataset in the following structure:

```
synthea-mimic/
└── csv/
├── allergies.csv
├── careplans.csv
├── claims.csv
├── claims_transactions.csv
├── conditions.csv
├── devices.csv
├── encounters.csv
├── imaging_studies.csv
├── immunizations.csv
├── medications.csv
├── observations.csv
├── organizations.csv
├── patients.csv
├── payer_transitions.csv
├── procedures.csv
├── providers.csv
└── supplies.csv
```

The application expects this exact directory structure.

---

## Feature Engineering

The pipeline transforms raw healthcare records into patient-level machine learning features through:

* Demographic feature extraction
* Observation aggregation
* Clinical measurement statistics
* Encounter history analysis
* Condition labeling
* Missing value handling
* One-hot encoding of categorical attributes

---

## Prediction Tasks

The dashboard supports two prediction settings:

### Multilabel Prediction

Predicts the presence of the most common clinical conditions using independent binary labels.

### Binary Prediction

Predicts whether a patient has any of the target clinical conditions.

---

## Models Implemented

### Decision Tree

Interpretable tree-based classifier with configurable depth and split constraints.

### Support Vector Machine (SVM)

Kernel-based classifier supporting linear, polynomial, and RBF kernels.

### Multi-Layer Perceptron (MLP)

Feed-forward neural network with configurable architecture and training parameters.

---

## Evaluation Metrics

Models are evaluated using:

* Accuracy
* Precision
* Recall
* F1 Score
* ROC Curves
* Confusion Matrices
* Classification Reports

---

## Temporal Shift Analysis

A key objective of this project is understanding how model performance changes over time.

The dataset is divided into:

* Historical Dataset (Dataset 1)
* Current Dataset (Dataset 2)

Models trained on historical data are evaluated on newer patient populations to measure robustness under temporal distribution shift.

---

## Continual Learning

The project studies whether retraining models on newer patient data improves predictive performance.

This allows comparison between:

* Original model performance
* Post-update model performance
* Adaptation effectiveness under temporal drift

---

## Dashboard Features

### Dataset Exploration

* Dataset statistics
* Feature distributions
* Class balance analysis

### Model Training

* Hyperparameter tuning
* Interactive experimentation

### Model Evaluation

* Classification metrics
* ROC analysis
* Confusion matrices

### Model Interpretation

* Feature importance analysis
* Decision Tree visualization

### Temporal Analysis

* Historical vs current cohort comparison
* Distribution shift evaluation

### Continual Learning

* Before and after retraining comparisons

---

## Repository Structure

```
.
├── clinical_ml_dashboard.py
├── requirements.txt
└── README.md
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

## Future Improvements

Potential extensions include:

* Advanced continual learning methods
* Ensemble learning approaches
* Explainable AI techniques
* Automated hyperparameter optimization
* Real-world healthcare datasets

---

## Author

Aniket Shukla

BITS Pilani, Hyderabad Campus

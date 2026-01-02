# NSTEMI Risk Prediction: A MIMIC-IV Data Science Pipeline

## 📖 Project Overview
This project develops a predictive pipeline to assess 30-day mortality risk for patients with **Non-ST-Elevation Myocardial Infarction (NSTEMI)**. It demonstrates the complete lifecycle of healthcare data science, with a heavy focus on high-fidelity data engineering from the MIMIC-IV database.

## 🛠️ My Core Contributions: The Data Foundation
I developed the entire data infrastructure for this project, transforming millions of raw clinical records into a curated dataset for machine learning.

### 1. Advanced Cohort Extraction (`01_cohort_extraction_sql.ipynb`)
I designed and implemented the SQL logic to define the "Golden Standard" cohort:
* **Clinical Definition**: Combined ICD-10 diagnosis codes with laboratory evidence, specifically filtering for peak **Troponin** levels to confirm NSTEMI cases.
* **Feature Retrieval**: Engineered queries to extract 40+ dynamic and static variables, including vital signs, lab results, and comorbidities.

### 2. Robust Data Preprocessing (`02_data_preprocessing.ipynb`)
I built the preprocessing engine to handle the inherent noise of ICU data:
* **Missing Value Imputation**: Evaluated and applied sophisticated strategies for clinical variables with high missingness.
* **Outlier Management**: Implemented logic to detect and handle physiological outliers (e.g., extreme heart rate or BP readings).
* **Feature Engineering**: Normalized skewed clinical distributions and performed categorical encoding for medical histories.
* **Class Balancing**: Addressed the mortality class imbalance to ensure robust model training.



## 🗂️ Project Pipeline
* **01_cohort_extraction_sql.ipynb**: (My Work) SQL-based cohort and feature extraction.
* **02_data_preprocessing.ipynb**: (My Work) The engine for data cleaning and transformation.
* **03_baselines_timi_lr.ipynb**: Baseline experiments using TIMI risk scores and Logistic Regression.
* **04_lightgbm_model.ipynb**: Gradient Boosting implementation.
* **05_mlp_model.ipynb**: Deep Learning (MLP) implementation.

## 🔬 Methodology & Performance
By focusing on high-quality data engineering, our team achieved significant performance gains. **LightGBM** emerged as the superior model, outperforming traditional clinical scoring systems like TIMI in predicting short-term mortality.

## 🚀 Environment
* **Database**: Google BigQuery (MIMIC-IV)
* **Stack**: Python (Pandas, Scikit-learn, PyTorch), SQL

---
*Note: This was a collaborative project for the Machine Learning Applications for Health course.*

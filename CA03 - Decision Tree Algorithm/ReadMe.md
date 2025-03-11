# Building a Decision Tree Model for Income Classification

## Overview
This project implements a **Decision Tree Classifier** to predict whether an individual's income is **≤50K or >50K** based on demographic and work-related attributes.  
The model is trained on a dataset from the **Census Bureau**, where numerical features have been **binned into categorical groups** for better interpretability and modeling efficiency.

The model follows these steps:
- **Preprocesses the dataset** by binning numerical columns and encoding categorical features.
- **Trains an initial Decision Tree model** using `DecisionTreeClassifier`.
- **Tunes hyperparameters** (`split criterion`, `min_samples_leaf`, `max_features`, `max_depth`).
- **Evaluates model performance** using accuracy, precision, recall, and F1-score.
- **Uses the best model to predict income** for a new individual with predefined attributes.

**Target Accuracy:** **~84.41%** (after hyperparameter tuning).

---

## Dataset Information
- **Training Data:** 48,842 observations, categorized into **≤50K or >50K** income groups.
- **Features:** 9 binned attributes derived from demographic and work-related factors:
  - `hours_per_week_bin`
  - `occupation_bin`
  - `msr_bin` (Marriage Status & Relationships)
  - `capital_gl_bin`
  - `race_sex_bin`
  - `education_num_bin`
  - `education_bin`
  - `workclass_bin`
  - `age_bin`
- **Target Variable (`y`)**: 1 (`>50K` income) or 0 (`≤50K` income).

Each numerical attribute was **binned into labeled categories (`a., b., c., d.`)** to standardize feature representation.

---

## Libraries
Ensure you have the following Python libraries installed:
```bash
pip install numpy pandas scikit-learn matplotlib graphviz

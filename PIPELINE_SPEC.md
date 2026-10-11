# FML Project Pipeline Specification

## Project
Predicting Online Shopper Purchase Intention

## Dataset
UCI Online Shoppers Purchasing Intention Dataset

- Total observations: 12,330
- Target: Revenue
- Task: Binary classification

## Train-Test Split
- Training rows: 9,864
- Testing rows: 2,466
- Test size: 20%
- Random state: 42
- Stratification: Revenue

## Preprocessing
- Numerical features: StandardScaler
- Categorical features: OneHotEncoder
- One-hot encoding uses handle_unknown='ignore'
- Preprocessing must be fitted on training data only.
- Processed feature count: 75

## Baseline Models
1. Logistic Regression
2. Decision Tree
3. Random Forest
4. Support Vector Machine (SVM)

## Evaluation Metrics
- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC

## Baseline Results
See results/taruni/baseline_model_results.csv.

## Saved Artifacts
- data/processed/train_raw.csv
- data/processed/test_raw.csv
- data/processed/y_train.csv
- data/processed/y_test.csv
- data/processed/feature_names.csv
- results/taruni/baseline_model_results.csv
- results/taruni/preprocessing_pipeline.joblib

## Methodological Notes
- Preserve the official split for subsequent comparisons.
- Fit preprocessing and feature-selection steps using training data only.
- Apply resampling only to training data.
- Evaluate final experiments on the held-out test set.
- Examine PageValues for potential target leakage based on prediction-time availability.

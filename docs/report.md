# Project Documentation: Breast Cancer Diagnostic

## Objective
Predict whether a breast tumor is malignant or benign from 30 measurements taken from cell images.

## Dataset
Breast Cancer Wisconsin (Diagnostic), 569 samples and 30 numeric features. About 63% benign and 37% malignant. No missing values.

## Process
1. **Data cleaning:** removed the unused `id` and `Unnamed: 32` columns, checked for duplicates and encoded diagnosis as Malignant = 1, Benign = 0.
2. **EDA:** class distribution, feature histograms, box plots and a correlation heatmap.
3. **Preparation:** 80/20 stratified train-test split and feature scaling inside a pipeline.
4. **Modeling:** Logistic Regression, KNN, SVM, Random Forest and Gradient Boosting.
5. **Evaluation:** accuracy, precision, recall, F1-score, ROC-AUC, confusion matrices and ROC curves.
6. **Tuning:** grid search on the SVM, optimized for recall.

## Key Findings
- Size and shape features (radius, perimeter, area, concave points) are the strongest indicators of malignancy.
- All models performed well, with test accuracy of roughly 96-97%.
- Recall was prioritized, because missing a malignant case is the costliest error.

## Limitations
Small dataset and a single train-test split. This is a learning project, not a clinical tool.

## Tools
Python, pandas, numpy, matplotlib, seaborn, scikit-learn, Google Colab

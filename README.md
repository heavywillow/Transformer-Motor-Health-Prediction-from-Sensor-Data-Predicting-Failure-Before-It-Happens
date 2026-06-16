# Project: Transformer/Motor Health Prediction from Sensor Data — Predicting Failure Before It Happens

## Project Goal
Train a classification model on motor sensor readings (air/process temperature, rotational speed, torque, tool wear) to predict whether a machine is healthy or about to fail — the same underlying idea used in industrial predictive-maintenance systems to avoid costly unplanned downtime.

## Dataset 

Kaggle "Predictive Maintenance Dataset" (AI4I 2020)**
- Link: https://www.kaggle.com/datasets/shivamb/machine-predictive-maintenance-classification
- Columns: Air temperature, Process temperature, Rotational speed, Torque, Tool wear, Failure Type (Yes/No + failure type).
- Already in clean CSV format — easiest to start with, less cleaning headache, since you said you're mediocre in core domain this is the safer pick.

## Steps

1. Load CSV, clean missing values
2. EDA: plot how failures correlate with torque, temperature, tool wear (simple bar/scatter plots)
3. Split data: 80% train, 20% test (literally same as your friend)
4. Train classifier: Logistic Regression first (simple, explainable), then Random Forest (better accuracy, still easy to explain — "it's a bunch of decision trees voting")
5. Predict on the 20% test set
6. Report: Accuracy, Precision, Recall, Confusion Matrix
7. Bonus: feature importance plot — "which sensor reading matters most for predicting failure" (this single chart impresses interviewers because it shows interpretability, not just a black box)

## Tools & Skills
- Python: pandas, numpy, matplotlib/seaborn
- ML: scikit-learn (LogisticRegression, RandomForestClassifier, train_test_split, classification_report, confusion_matrix)
- Optional polish: SHAP library for feature importance (1 extra line of code, looks very advanced in interviews)
- GitHub repo with a clean README



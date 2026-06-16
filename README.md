# Project: Transformer/Motor Health Prediction from Sensor Data — Predicting Failure Before It Happens

## Why this fits what you want
It's the exact same shape as your friend's project (train on 80%, predict/test on 20%, report accuracy), it gives one clean useful output ("this machine will fail / won't fail" or "X% chance of failure"), and the core EE knowledge needed is shallow but real — you just need to explain 3-4 basic concepts (current, vibration, temperature, insulation) which any 2nd-year EE student already knows. It's easy to explain in an interview in 2 minutes.

## Project Title
"Predictive Maintenance of Induction Motors using Machine Learning — Fault Detection from Sensor Data"

## The one-line pitch (use this in interviews)
"I trained a classification model on motor sensor readings (current, vibration, temperature) to predict whether a motor is healthy or about to fail, achieving X% accuracy on unseen test data — this is the same idea as predictive maintenance systems used in industries to avoid costly breakdowns."

That's it. One sentence, anyone (technical or HR) understands it.

## Dataset (pick one — both are beginner-friendly and EE-specific)

**Option A (Recommended): MAFAULDA – Machinery Fault Database**
- Link: http://www02.smt.ufrj.br/~offshore/mfs/page_01.html (also mirrored on Kaggle — search "MAFAULDA dataset")
- Vibration + acoustic data from a motor under normal, imbalance, misalignment, and bearing fault conditions.
- Real motor, real faults, well-documented.

**Option B (Simpler, very beginner-friendly): Kaggle "Predictive Maintenance Dataset" (AI4I 2020)**
- Link: https://www.kaggle.com/datasets/shivamb/machine-predictive-maintenance-classification
- Columns: Air temperature, Process temperature, Rotational speed, Torque, Tool wear, Failure Type (Yes/No + failure type).
- Already in clean CSV format — easiest to start with, less cleaning headache, since you said you're mediocre in core domain this is the safer pick.

**Option C (If you want something closer to "transformer/grid" instead of motor):**
- Kaggle "Power Transformer Health Index Dataset" — search "transformer DGA dataset" or "Dissolved Gas Analysis transformer fault" on Kaggle.
- Uses Dissolved Gas Analysis (DGA) values to classify transformer fault type. Slightly more advanced terms but still explainable (oil degrades, gases form, gas ratios indicate fault type — IEEE C57.104 standard, you can namedrop this for bonus points).

**My recommendation: go with Option B.** Cleanest data, fastest to build, and the explanation is dead simple: "sensors recorded temperature, speed, torque, tool wear — model predicts if/how the machine fails."

## What you actually do (mirrors your friend's project exactly)

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
- Notebook: Google Colab (no setup needed)
- Optional polish: SHAP library for feature importance (1 extra line of code, looks very advanced in interviews)
- GitHub repo with a clean README



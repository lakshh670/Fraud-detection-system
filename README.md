# Fraud-detection-system
💳 Credit Card Fraud Detection — Week 1 (Offline Model Building)
📘 Overview

This project focuses on detecting fraudulent credit card transactions using machine learning.
In Week 1, we built and evaluated the offline version of the model — preparing it for real-time integration in the upcoming weeks.

🧩 Workflow Summary
1️⃣ Data Preprocessing

Cleaned and formatted transaction data.

Converted date columns to datetime format.

Extracted time-based features like hour, day, month, and day of week.

Engineered useful features:

Age

Distance from home

Average amount per card

Amount-to-mean ratio

Transactions per day

2️⃣ Categorical Feature Encoding

Gender → One-Hot Encoding (binary variable)

Job → Target Encoding (high-cardinality column)

Merchant → Label + Frequency Encoding (large number of unique values)

Category → One-Hot Encoding (limited unique values)

3️⃣ Class Imbalance Handling

Applied SMOTE to balance fraud vs. non-fraud transactions.

4️⃣ Model Training

Trained two models:

Logistic Regression → Baseline, interpretable.

XGBoost → Final high-performance model.

Both evaluated using:

Precision, Recall, F1-score, and ROC-AUC.

Plotted Confusion Matrix and ROC Curves for comparison.

5️⃣ Model Saving

Saved key components for later real-time use:

lor_model.pkl — Logistic Regression

xgb_model.pkl — XGBoost

target_encoder.pkl — Job encoder

label_encoder.pkl — Merchant encoder

🎯 Outcome

A fully trained fraud detection model with preprocessing pipeline and performance metrics — ready to be integrated into the real-time streaming pipeline

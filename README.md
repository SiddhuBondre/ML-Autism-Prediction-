# 🧠 Autism Spectrum Disorder (ASD) Prediction

# 📌 Overview

This project predicts whether an individual is likely to have Autism Spectrum Disorder (ASD) using machine learning models.
The dataset includes 10 screening questions (AQ-10 test) along with demographic details such as gender, ethnicity, country of residence, and medical history indicators.


# 📂 Dataset Information

Source: Autism Screening Dataset (Kaggle / UCI)

Total Columns: 22

Target Variable: Class/ASD

Sample Columns:

ID: Unique identifier

A1_Score to A10_Score: Binary scores from AQ-10 autism test (0 or 1)

gender: Male (m) or Female (f)

ethnicity: Ethnic background

jaundice: Whether the individual had jaundice at birth (yes/no)

austim: Family history of autism (yes/no)

contry_of_res: Country of residence

used_app_before: Whether the person has used the autism screening app before

result: AQ-10 total score

age_desc: Age category description (e.g., "18 and more")

relation: Relation of respondent (Self, Parent, etc.)

Class/ASD: Final classification (1 = ASD, 0 = No ASD)

# ⚙️ Tech Stack

# Language: Python 3.x

# Libraries:

pandas, numpy → Data processing

matplotlib, seaborn → Visualization

scikit-learn → ML model building and evaluation

# 🛠 Workflow

# Data Loading

# Data Cleaning

Handle missing values (? in ethnicity, relation)

Encode categorical variables (Label Encoding / One-Hot Encoding)

Normalize numeric values if needed

# EDA (Exploratory Data Analysis)

Distribution plots for AQ-10 scores

Gender-wise ASD count

Correlation heatmap for numeric features

# Model Building

Logistic Regression

Random Forest

XGBoost

# Evaluation Metrics

Accuracy

Precision, Recall, F1-score

ROC-AUC curve

# 📌 Conclusion – Autism Prediction Model Comparison

# From the results:

| Model               | Accuracy | Precision | Recall | F1 Score |
| ------------------- | -------- | --------- | ------ | -------- |
| Logistic Regression | 0.87     | 0.83      | 0.80   | 0.81     |
| Random Forest       | 0.85     | 0.80      | 0.76   | 0.78     |
| XGBoost             | 0.80     | 0.72      | 0.71   | 0.71     |

# Key Insights:

Logistic Regression performed best overall, achieving the highest accuracy, precision, recall, and F1-score among the three models.

Random Forest was close in accuracy but showed slightly weaker recall, meaning it missed more positive ASD cases compared to Logistic Regression.

XGBoost underperformed in this dataset, with noticeably lower recall and F1-score, suggesting it was less effective at correctly identifying ASD cases.

# Final Recommendation:
For this dataset, Logistic Regression is the preferred model because:

It strikes the best balance between precision and recall.

It has the highest F1-score, meaning it’s more reliable for both detecting positive cases and avoiding false positives.

If recall (catching as many ASD cases as possible) is critical, Logistic Regression is still the top choice, but further tuning of Random Forest might help improve recall without sacrificing too much precision.

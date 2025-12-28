# BankMarketing_analysis

# Bank Marketing Campaign Prediction using Machine Learning

## Overview
This project analyzes marketing campaign data from a banking institution to predict whether a customer will subscribe to a term deposit. The goal is to improve campaign targeting by identifying customers with a higher likelihood of conversion using supervised machine learning models.

The dataset contains over **41,000 customer records** with demographic and financial attributes such as age, job type, education level, and loan status. To ensure realistic predictions, campaign-dependent features (e.g., call duration) were excluded. The target variable is highly imbalanced, with only ~11% positive responses.

---

## Data Preparation & Baseline Analysis
- No missing values in the dataset  
- Categorical variables encoded using one-hot encoding  
- Stratified train–test split to preserve class distribution  
- Baseline models used to highlight limitations of accuracy on imbalanced data  

**Majority class baseline accuracy:** **88.74%**, with **zero recall**, demonstrating the need for better evaluation metrics.

---

## Models Trained
The following classification models were trained and evaluated:

- Logistic Regression  
- K-Nearest Neighbors (KNN)  
- Decision Tree  

Evaluation metrics included **accuracy, precision, recall, F1-score, and ROC-AUC**, along with training time.

---

## Model Performance (Default Parameters)

| Model | Test Accuracy | Precision | Recall | F1-Score |
|------|--------------|-----------|--------|----------|
| Logistic Regression | 88.74% | 0.000 | 0.000 | 0.000 |
| K-Nearest Neighbors | 87.70% | 0.297 | 0.067 | 0.109 |
| Decision Tree | 86.40% | 0.227 | 0.086 | 0.125 |

While Logistic Regression matched baseline accuracy, it failed to identify positive cases. KNN and Decision Tree achieved a better balance between precision and recall.

---

## Model Improvement
Hyperparameter tuning using Grid Search and F1-score optimization was applied to improve model performance.

### Best Results After Tuning
- **Best F1-score:** K-Nearest Neighbors (**0.137**)  
- **Best ROC-AUC:** Logistic Regression (**0.649**)  
- Improved recall led to better identification of potential subscribers despite small accuracy trade-offs

---

## Key Insights
- Accuracy alone is misleading for imbalanced classification problems  
- F1-score and ROC-AUC provide more meaningful evaluation for marketing use cases  
- KNN is better suited for conversion-focused targeting  
- Logistic Regression performs well for customer ranking and probability estimation

---

## Tools & Technologies
- Python  
- scikit-learn  
- Pandas, NumPy  
- Matplotlib, Seaborn  

---

## Conclusion
This project demonstrates the importance of metric-driven evaluation when working with imbalanced datasets. By prioritizing recall, F1-score, and ROC-AUC over accuracy, the models become more effective for real-world marketing decision-making.

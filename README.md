# 🩺 Diabetes Prediction

## Overview
A binary classification model that predicts whether a patient has diabetes
based on medical diagnostic features using the Pima Indians Diabetes Database.

## Dataset
- **Source:** Kaggle - Pima Indians Diabetes Database
- **Size:** 768 rows × 9 columns
- **Target:** Outcome (0 = No Diabetes, 1 = Diabetes)
- **Class Distribution:** 500 No Diabetes | 268 Diabetes

## Algorithm
- Logistic Regression

## Results
| Metric | Training | Testing |
|--------|----------|---------|
| Accuracy | 79.64% | 70.78% |
| Precision (Class 1) | - | 60.00% |
| Recall (Class 1) | - | 50.00% |
| F1-Score (Class 1) | - | 54.55% |

> ⚠️ Mild overfitting detected — 8.9% accuracy drop from training to testing

## Feature Importance
| Feature | Coefficient |
|---------|-------------|
| Glucose | 1.1825 |
| BMI | 0.6887 |
| Pregnancies | 0.3775 |
| DiabetesPedigreeFunction | 0.2334 |
| Age | 0.1478 |

> 💡 Glucose is the strongest predictor of diabetes

## Key Tasks
- Handled invalid zero values in medical features (Glucose, BMI, Insulin etc.)
- Filled missing values with median (robust to outliers)
- Applied StandardScaler for feature normalization
- 80/20 stratified train-test split (preserves class proportions)
- Comprehensive EDA with correlation matrix and boxplots

## Key Findings
- Glucose, BMI and Age have strongest correlation with diabetes outcome
- Diabetic patients show significantly higher glucose levels and BMI
- Dataset is imbalanced but acceptable for initial modeling

## Tech Stack
- Python
- Pandas, NumPy
- Scikit-learn
- Matplotlib, Seaborn
- Jupyter Notebook

## How to Run
1. Clone the repo
```bash
   git clone https://github.com/FaseehAbdullah/diabetes-prediction.git
```
2. Install dependencies
```bash
   pip install pandas numpy scikit-learn matplotlib seaborn jupyter
```
3. Open the notebook
```bash
   jupyter notebook week_2_Diabetes_Prediction.ipynb
```

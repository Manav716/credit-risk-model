# 💳 Credit Risk Prediction using Machine Learning

## 📌 Overview
This project focuses on predicting whether a customer is a **good or bad credit risk** using machine learning techniques. The goal is to help financial institutions minimize losses by identifying high-risk customers.

---

## 🎯 Problem Statement
In the banking and financial sector, incorrectly approving a risky customer can lead to financial loss.  
This project aims to build a model that prioritizes **detecting bad customers (high recall)** over simply maximizing accuracy.

---

## 📊 Dataset
- Dataset: German Credit Data
- Features include:
  - Credit amount
  - Duration
  - Age
  - Job
  - Saving accounts
  - Checking account
  - Other financial attributes

---

## 🧠 Workflow

### 🔹 1. Data Preprocessing
- Handled missing values:
  - Categorical → filled with **"No Account"**
- Removed duplicates
- Identified numerical and categorical features

---

### 🔹 2. Exploratory Data Analysis (EDA)
- Univariate analysis:
  - Distribution, skewness, outliers
- Bivariate analysis:
  - Feature vs target relationships
- Identified key risk patterns

---

### 🔹 3. Data Preparation
- Log transformation applied to skewed features
- Outliers handled using IQR capping
- One-Hot Encoding for categorical variables
- Train-test split with stratification

---

### 🔹 4. Handling Imbalanced Data
- Applied **SMOTE** on training data
- Balanced class distribution for better learning

---

### 🔹 5. Model Building
Compared multiple models:
- Logistic Regression
- Random Forest
- XGBoost

---

### 🔹 6. Model Selection
- Selected **Logistic Regression** due to:
  - Better recall (important for risk detection)
  - Stability (less overfitting)
  - Interpretability

---

### 🔹 7. Hyperparameter Tuning
- Used **GridSearchCV**
- Optimized for **recall**

---

### 🔹 8. Threshold Optimization (Key Highlight 🔥)
- Default threshold (0.5) replaced with **0.327**
- Custom threshold selection based on:
  - Minimal F1 drop
  - Maximum recall

---

## 📈 Final Results

| Metric | Value |
|-------|------|
| Accuracy | ~66% |
| Recall (Bad Customers) | **85% 🔥** |
| Precision | ~44% |
| F1 Score | ~0.57 |

---

## 💎 Key Insights
- Threshold tuning significantly improved model performance
- Recall is more important than accuracy in credit risk problems
- Logistic Regression outperformed more complex models due to stability
- Business-driven evaluation is crucial in real-world ML problems

---

## 🛠️ Tools & Technologies
- Python
- Pandas, NumPy
- Scikit-learn
- Matplotlib, Seaborn
- Imbalanced-learn (SMOTE)

---

## 🚀 How to Run

```bash
# Clone repository
git clone https://github.com/your-username/credit-risk-prediction.git

# Install dependencies
pip install -r requirements.txt

# Run notebook

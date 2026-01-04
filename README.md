# 🏦 Bank Customer Churn Prediction

Predicting which customers are likely to leave **Beta Bank** using feature engineering and machine learning.

---

## ⭐ Project Summary

Customer churn greatly impacts business revenue. Beta Bank wants to identify customers at risk of leaving so the bank can proactively retain them.  
This project builds a predictive model, explores class imbalance, applies multiple correction techniques, and evaluates performance using **F1 Score** and **AUC-ROC**.

📌 **Final Performance**
- ✅ **F1 Score:** 0.629
- ✅ **AUC-ROC:** ≈ 0.84  
- 🎯 **Requirement Achieved** (minimum F1 = 0.59)

---

## 🎯 Objectives

- Prepare and clean banking churn dataset  
- Perform feature engineering  
- Analyze class imbalance  
- Train baseline models  
- Apply imbalance-handling techniques  
- Optimize and evaluate model performance  
- Select best model and test it

---

## 📂 Dataset

File: `Churn.csv`

| Feature | Description |
|--------|-------------|
| RowNumber | Row index |
| CustomerId | Unique ID |
| Surname | Customer last name |
| CreditScore | Credit rating |
| Geography | Country |
| Gender | Gender |
| Age | Age |
| Tenure | Years with bank |
| Balance | Account balance |
| NumOfProducts | Number of bank products |
| HasCrCard | Credit card ownership |
| IsActiveMember | Activity status |
| EstimatedSalary | Salary estimate |
| **Exited** | Target: 1 = Churn, 0 = Remains |

**Target Variable:** `Exited`

---

## 🧹 Data Preparation & Feature Engineering

✔ Removed irrelevant identifier fields  
✔ Checked and handled missing values  
✔ Encoded categorical features using One-Hot Encoding  
✔ Scaled numerical features  
✔ Split dataset into Training / Validation / Test

---

## ⚖️ Class Imbalance

The dataset is highly imbalanced (fewer churn cases).  
Actions taken:

1️⃣ Trained baseline models without correction  
2️⃣ Applied imbalance-handling techniques:
- Class Weighting  
- Oversampling / SMOTE  

These significantly improved recall and F1 score.

---

## 🧪 Modeling Approach

### 🔹 Baseline Models (No Imbalance Fix)

| Model | F1 Score | AUC-ROC |
|------|---------:|--------:|
| Logistic Regression | 0.353 | 0.53 |
| Decision Tree | 0.569 | ~0.74 |
| Random Forest | 0.317 | – |

---

### 🔹 Improved Models (With Balancing)

| Model | F1 Score | AUC-ROC |
|------|---------:|--------:|
| Decision Tree | 0.569 | 0.82 |
| **Random Forest (Final Model)** | **0.629** | **≈ 0.84** |

🔥 **Random Forest performed best**, balancing precision and recall well.

---

## 🏁 Final Test Results

- ✔ **F1 Score:** 0.629  
- ✔ **AUC-ROC:** ≈ 0.84  
- ✔ Requirement Passed

The model demonstrates strong ability to distinguish churn vs retained customers.

---

## 📈 Key Insights

- Feature engineering significantly boosts performance  
- Handling imbalance is critical in churn problems  
- Random Forest provides strong, stable results  
- AUC-ROC confirms high class separability  

---

## 🗂 Project Structure


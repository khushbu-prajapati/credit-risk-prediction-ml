# 🏦 Credit Risk Prediction – Machine Learning Project

## 📌 Overview
This project implements an end-to-end **credit risk prediction system**
using machine learning and SQL Server data.
The objective is to minimize financial loss by identifying high-risk loan applicants.

---

## 🧠 Business Problem
In credit lending:
- **False Negatives** (approving risky customers) cause high losses
- **False Positives** (rejecting safe customers) cause opportunity loss

This project optimizes predictions using a **cost-sensitive decision threshold**
instead of relying only on accuracy.

---

## 🗄️ Data Source
- Database: SQL Server
- Table: `credit_risk_dataset`
- Target Variable: `loan_status`

---

## ⚙️ Tech Stack
- Python
- SQL Server
- Pandas, NumPy
- Scikit-learn
- SQLAlchemy, PyODBC

---

## 🧩 Project Workflow
1. Data extraction from SQL Server
2. Data validation & preprocessing
3. Feature engineering (numeric + categorical)
4. Model training:
   - Logistic Regression (baseline)
   - Random Forest (final model)
5. Model evaluation using ROC-AUC & confusion matrix
6. Business cost-based threshold optimization

---

## 📊 Model Evaluation
- Metrics used:
  - Precision, Recall, F1-score
  - ROC-AUC
  - Confusion Matrix

Random Forest showed better performance for identifying risky customers.

---

## 💰 Cost-Sensitive Threshold Optimization
Instead of using default threshold (0.5),
multiple thresholds were evaluated using business cost:

- False Negative cost = 5
- False Positive cost = 1

**Optimal threshold selected based on minimum financial loss.**

---

## 🏗️ Project Structure
```text
credit-risk-prediction-ml/
│
├── notebooks/
│   └── Credit_Risk_Prediction_Production_Pipeline.ipynb
│
├── README.md

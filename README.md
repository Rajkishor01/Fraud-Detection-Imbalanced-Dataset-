# Fraud-Detection-Imbalanced-Dataset-
---
# 🛡️ Fraud Detection Using CatBoost & SMOTE

This project focuses on building a **fraud detection model** using **CatBoost Classifier** on a highly imbalanced transaction dataset. It demonstrates the use of **SMOTE (Synthetic Minority Oversampling Technique)** to balance the data, improve model learning, and boost performance in detecting fraudulent transactions.

---

## 📂 Dataset

- **Size**: ~6.3 million records
- **Nature**: Highly imbalanced (fraud cases are extremely rare)
- **Features**: Transactional and categorical data

---

## 🎯 Objectives

- Detect fraudulent transactions with high recall
- Handle class imbalance using oversampling
- Compare performance metrics to understand trade-offs between recall and precision

---

## 🧰 Tools & Libraries

- Python 
- Pandas, NumPy  
- CatBoost (`catboost`)  
- SMOTE (`imblearn`)  
- Scikit-learn (`sklearn`)  
- Matplotlib, Seaborn (for visualizations)

---

## 🧠 Model Overview

- **Algorithm**: CatBoost Classifier
- **Preprocessing**:
  - Handled missing values (if any)
  - Feature scaling (if required)
- **Training**:
  - Split original dataset into temp-dataset and validation dataset
  - Applied SMOTE on temp-dataset to balance the minority class (fraud)
  - Split temp-dataset into train-test sets
  - Trained on balanced data
- **Evaluation**:
  - Accuracy, Precision, Recall, F1-Score
  - Confusion Matrix on validataion dataset

---

## 📊 Results

| Metric         | Non-Fraud (0) | Fraud (1) |
|----------------|---------------|-----------|
| Precision      | 1.00          | 0.27      |
| Recall         | 1.00          | 0.99      |
| F1-Score       | 1.00          | 0.43      |

- **Overall Accuracy**: ~100%
- **Insight**: Model achieved **very high recall for fraud** cases, even if it comes at the cost of more false positives (lower precision).

---

## 📌 Key Takeaways

- **CatBoost** simplifies preprocessing and handles categorical variables effectively.
- **SMOTE** was crucial for boosting recall on the minority class.
- This setup is well-suited for real-world fraud systems where **catching fraud is more important than occasional false alarms**.


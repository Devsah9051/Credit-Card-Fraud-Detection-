
# 💳 Credit Card Fraud Detection using Machine Learning

## 📌 Project Overview

This project focuses on detecting fraudulent credit card transactions using Machine Learning techniques. Due to the highly imbalanced nature of fraud datasets, special attention was given to data preprocessing, sampling strategies, and model evaluation to build a reliable fraud detection system.

The objective is to classify transactions as:

* **0 → Legitimate Transaction**
* **1 → Fraudulent Transaction**

The final solution uses a **Random Forest Classifier** trained on a balanced dataset created through undersampling and achieves strong classification performance on unseen transactions.

---

## 🚀 Features

* Comprehensive Exploratory Data Analysis (EDA)
* Data Cleaning and Preprocessing
* Class Imbalance Handling using Undersampling
* Feature Scaling using StandardScaler
* Multiple Model Evaluation
* Fraud Detection Prediction System
* Model Serialization using Joblib
* Production-Ready Pipeline

---

## 📊 Dataset Information

The dataset contains:

* **284,807 Transactions**
* **30 Numerical Features**
* **1 Target Variable (Class)**

Target Distribution:

| Class | Meaning                |
| ----- | ---------------------- |
| 0     | Legitimate Transaction |
| 1     | Fraudulent Transaction |

The dataset is highly imbalanced:

* Legitimate Transactions: **284,315**
* Fraudulent Transactions: **492**

---

## 🔍 Exploratory Data Analysis

The following analyses were performed:

* Dataset structure inspection
* Missing value analysis
* Fraud vs Legitimate transaction comparison
* Statistical analysis of transaction amounts
* Class distribution analysis
* Group-wise feature comparison

Key Findings:

* No missing values were present.
* Fraudulent transactions represented less than 0.2% of the total data.
* Significant feature distribution differences existed between fraudulent and legitimate transactions.

---

## ⚙️ Data Preprocessing

### Target Variable Conversion

Converted the target column from string format to integer format.

### Handling Class Imbalance

Used **Random Undersampling** to create a balanced dataset:

* Legitimate Transactions: 492
* Fraudulent Transactions: 492

Final Dataset Size:

```text
984 rows × 31 columns
```

### Feature Scaling

Applied:

```python
StandardScaler()
```

to normalize feature values before model training.

---

## 🤖 Machine Learning Models

The following models were trained and evaluated:

### Logistic Regression

* Accuracy: 96%
* Precision: 98%
* Recall: 95%

### Random Forest Classifier

Parameters:

```python
RandomForestClassifier(
    n_estimators=100,
    max_depth=10
)
```

Performance:

* Accuracy: 96%
* Precision: 97%
* Recall: 95%
* F1-Score: 96%

---

## 📈 Model Performance

| Model               | Accuracy |
| ------------------- | -------- |
| Logistic Regression | 96%      |
| Random Forest       | 96%      |

The Random Forest model was selected as the final model due to its robustness and strong fraud detection performance.

---

## 🛠️ Technologies Used

### Programming Language

* Python

### Libraries

* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Joblib

### Machine Learning Techniques

* Data Preprocessing
* Feature Scaling
* Random Undersampling
* Logistic Regression
* Random Forest Classification
* Model Evaluation

---

## 💾 Model Saving

The trained artifacts were saved using Joblib:

```python
credit_card_model.pkl
scaler.pkl
columns.pkl
```

These files can be directly used for deployment and inference.

---

## 🔮 Prediction Pipeline

The prediction workflow:

1. Receive transaction data
2. Apply feature scaling
3. Load trained Random Forest model
4. Generate prediction
5. Return:

```text
Valid Transaction
```

or

```text
Invalid Transaction
```

---

## 📁 Project Structure

```text
Credit-Card-Fraud-Detection/
│
├── creditcard.csv.zip
├── credit_card_model.pkl
├── scaler.pkl
├── columns.pkl
├── fraud_detection.ipynb
├── README.md
│
└── requirements.txt
```

---

## 🎯 Results

* Successfully handled severe class imbalance.
* Achieved 96% classification accuracy.
* Built a reusable fraud detection pipeline.
* Saved production-ready model artifacts.
* Demonstrated the application of machine learning in financial fraud prevention.

---

## 👨‍💻 Author

**Dev Sah**

Aspiring Data Scientist | Machine Learning Enthusiast

### Skills

* Python
* Machine Learning
* Data Analysis
* SQL
* Deep Learning
* Natural Language Processing (NLP)

---

⭐ If you found this project useful, consider giving it a star on GitHub.

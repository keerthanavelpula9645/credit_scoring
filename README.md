# 💳 Credit Scoring Model

## 📌 Project Overview

The **Credit Scoring Model** is a machine learning project that predicts whether a loan applicant is **creditworthy or not** based on their financial and personal information.

The project uses **Logistic Regression and XGBoost** classification algorithms to predict the target variable `Creditworthy`.

---

## 🎯 Objective

The main objective of this project is to build a machine learning model that can:

- Analyze an applicant's financial information
- Process and clean raw data
- Handle missing values
- Convert categorical data into numerical values
- Predict creditworthiness
- Compare different machine learning models
- Evaluate model performance

---

## 🛠️ Technologies Used

- **Python**
- **Pandas** – Data manipulation and preprocessing
- **NumPy** – Numerical operations
- **Scikit-learn** – Machine learning
- **Matplotlib** – Data visualization
- **Logistic Regression** – Classification
- **XGBoost** – Gradient boosting classification

---

## 📊 Dataset

The dataset contains information about loan applicants, including:

- Age
- Annual Income
- Employment Years
- Employment Type
- Housing Status
- Loan Amount
- Loan Term
- Credit Score
- Debt-to-Income Ratio
- Monthly Debt
- Number of Credit Accounts
- Late Payments
- Previous Defaults
- Loan Purpose
- Creditworthiness

The target variable is:

```text
Creditworthy
```

- `0` = Not Creditworthy
- `1` = Creditworthy

---

## 🔄 Project Workflow

```text
Raw Dataset
     ↓
Data Loading
     ↓
Data Exploration
     ↓
Data Cleaning
     ↓
Handling Missing Values
     ↓
Encoding Categorical Data
     ↓
Feature & Target Selection
     ↓
Train-Test Split
     ↓
Model Training
     ↓
Logistic Regression + XGBoost
     ↓
Prediction
     ↓
Model Evaluation
```

---

## 🤖 Machine Learning Models

### 1. Logistic Regression

Logistic Regression is used as a baseline classification model because the target variable contains two classes:

```text
0 → Not Creditworthy
1 → Creditworthy
```

### 2. XGBoost

**XGBoost (Extreme Gradient Boosting)** is an advanced machine learning algorithm based on decision trees.

It builds multiple decision trees sequentially, where each new tree attempts to correct the errors made by previous trees.

XGBoost is useful for this project because it can:

- Capture complex relationships between financial features
- Handle non-linear patterns
- Reduce prediction errors through boosting
- Provide strong performance on structured/tabular data
- Support feature importance analysis

Example:

```python
from xgboost import XGBClassifier

xgb_model = XGBClassifier(
    n_estimators=100,
    max_depth=4,
    learning_rate=0.1,
    random_state=42
)

xgb_model.fit(x_train, y_train)

y_pred = xgb_model.predict(x_test)
```

---

## 📈 Model Evaluation

The models can be evaluated using:

- Accuracy Score
- Precision
- Recall
- F1-Score
- Confusion Matrix

Example:

```python
from sklearn.metrics import accuracy_score, classification_report

print("Accuracy:", accuracy_score(y_test, y_pred))
print(classification_report(y_test, y_pred))
```

The performance of **Logistic Regression and XGBoost** can then be compared to determine which model performs better on the credit scoring dataset.

---

## 💡 Key Learning Outcomes

Through this project, I learned:

- Data preprocessing using Pandas
- Handling missing values
- Encoding categorical variables
- Train-test splitting
- Binary classification
- Logistic Regression
- XGBoost classification
- Model evaluation
- Comparing machine learning algorithms
- Feature importance analysis

---

## 🚀 Future Improvements

- Perform hyperparameter tuning for XGBoost
- Use cross-validation
- Improve categorical feature encoding
- Handle class imbalance if present
- Add feature importance visualizations
- Compare XGBoost with Random Forest and other boosting models
- Deploy the final model using **Streamlit**

---

## 👨‍💻 Author

**AI/ML Intern Aspirant**

Built as a machine learning portfolio project to demonstrate skills in **Python, data preprocessing, classification, and XGBoost**.

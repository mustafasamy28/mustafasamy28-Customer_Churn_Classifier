# Customer Churn Classifier

This project uses machine learning to predict customer churn based on the Telco Customer dataset.


# Customer Churn Prediction: Step-by-Step Tutorial

This comprehensive tutorial walks through the entire process of building a customer churn prediction model with high accuracy. Each step will show both the proper technique and demonstrate what happens if we skip it, to illustrate its importance.

## Table of Contents
1. [Data Loading and Initial Exploration](#1-data-loading-and-initial-exploration)
2. [Data Cleaning](#2-data-cleaning)
3. [Exploratory Data Analysis](#3-exploratory-data-analysis)
4. [Feature Engineering](#4-feature-engineering)
5. [Data Preprocessing](#5-data-preprocessing)
6. [Model Building](#6-model-building)
7. [Model Evaluation](#7-model-evaluation)
8. [Model Improvement](#8-model-improvement)
9. [Final Model and Interpretation](#9-final-model-and-interpretation)


![Customer Churn Model](abe75502-04df-4700-a787-5d306f61a7a0.png)

## 🧠 Skills & Tools Used

Throughout this project, I utilized a wide range of data science and machine learning tools, libraries, and techniques. Here’s a summary of the key components:

### *Languages & Libraries*
- *Python*: Main programming language.
- *Pandas, NumPy*: Data manipulation and numerical operations.
- *Matplotlib, Seaborn*: Data visualization and styling.

### *Data Preprocessing & Feature Engineering*
- *SimpleImputer, KNNImputer*: Handling missing values.
- *StandardScaler, OneHotEncoder*: Data normalization and categorical encoding.
- *ColumnTransformer, Pipeline*: Efficient and modular preprocessing.
- *SelectFromModel, RFE, mutual_info_classif*: Feature selection techniques.

### *Modeling & Evaluation*
- *Scikit-learn*:
  - Classification algorithms: RandomForestClassifier, GradientBoostingClassifier
  - Model evaluation: classification_report, confusion_matrix, roc_curve, auc, f1_score, accuracy_score
  - Model tuning: GridSearchCV, cross_val_score
- *XGBoost*: Advanced gradient boosting with XGBClassifier.
- *SMOTE (from imbalanced-learn)*: Handling imbalanced datasets.

### *Workflow & Best Practices*
- *Train-test split and cross-validation*: Ensuring generalization and avoiding overfitting.
- *Pipelines*: Structured and clean machine learning workflow.
- *Warnings Management*: Suppressing unnecessary warnings for cleaner outputs.
- *Seaborn Themes*: Enhanced visuals using whitegrid style and custom palette.



## 📂 Dataset

- The dataset is from IBM's sample: `WA_Fn-UseC_-Telco-Customer-Churn.csv`

### 📄 **Column Descriptions:**

| # | Column | Description |
|--|--------|-------------|
| 0 | **customerID** | A unique identifier for each customer. |
| 1 | **gender** | The customer's gender (`Male` or `Female`). |
| 2 | **SeniorCitizen** | Indicates if the customer is a senior citizen (`1` = Yes, `0` = No). |
| 3 | **Partner** | Whether the customer has a partner (`Yes` or `No`). |
| 4 | **Dependents** | Whether the customer has dependents (like children, etc.) (`Yes` or `No`). |
| 5 | **tenure** | The number of months the customer has stayed with the company. |
| 6 | **PhoneService** | Whether the customer has a phone service (`Yes` or `No`). |
| 7 | **MultipleLines** | Whether the customer has multiple phone lines (`Yes`, `No`, or `No phone service`). |
| 8 | **InternetService** | Type of internet service the customer has (`DSL`, `Fiber optic`, or `No`). |
| 9 | **OnlineSecurity** | Whether the customer has online security service (`Yes`, `No`, or `No internet service`). |
| 10 | **OnlineBackup** | Whether the customer uses online backup services (`Yes`, `No`, or `No internet service`). |
| 11 | **DeviceProtection** | Whether the customer has device protection (`Yes`, `No`, or `No internet service`). |
| 12 | **TechSupport** | Whether the customer has technical support (`Yes`, `No`, or `No internet service`). |
| 13 | **StreamingTV** | Whether the customer streams TV (`Yes`, `No`, or `No internet service`). |
| 14 | **StreamingMovies** | Whether the customer streams movies (`Yes`, `No`, or `No internet service`). |
| 15 | **Contract** | Type of contract: `Month-to-month`, `One year`, or `Two year`. |
| 16 | **PaperlessBilling** | Whether the customer receives paperless billing (`Yes` or `No`). |
| 17 | **PaymentMethod** | How the customer pays: `Electronic check`, `Mailed check`, `Bank transfer`, or `Credit card`. |
| 18 | **MonthlyCharges** | The amount charged to the customer each month (float). |
| 19 | **TotalCharges** | Total amount charged over the customer's tenure (note: stored as a string/object). |
| 20 | **Churn** | Whether the customer has left the service (`Yes` = Churned, `No` = Still active). This is likely your **target variable** if you're doing prediction. |

> **Note:** The CSV file is excluded from Git using `.gitignore`.

## ✅ Results

- Accuracy: **92%**
- Best model: **XGBoost**
- Feature importance and confusion matrix are included in the notebook.

## 💡 Sample Output

```python
Prediction: Churn
Probability: 0.87
ّ

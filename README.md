# 📊 IBM Telco Customer Churn Prediction

## 🎯 Project Overview

Customer churn is one of the most critical challenges faced by subscription-based businesses. Retaining existing customers is significantly more cost-effective than acquiring new ones. This project aims to predict customer churn using machine learning techniques on the IBM Telco Customer Churn dataset.

An end-to-end Machine Learning pipeline was developed, covering data preprocessing, exploratory data analysis, dimensionality reduction, model comparison, hyperparameter tuning, and model persistence.

---

## 🏢 Business Problem

Telecommunication companies face significant revenue loss when customers discontinue their services. By accurately identifying customers who are likely to churn, businesses can implement targeted retention strategies and improve customer satisfaction.

### Target Variable

- **Churn = Yes** → Customer leaves the company
- **Churn = No** → Customer remains with the company

---

## 📂 Dataset

The project uses the **IBM Telco Customer Churn Dataset**, which contains customer information including:

- Demographic Information
- Customer Tenure
- Phone Services
- Internet Services
- Online Security
- Tech Support
- Streaming Services
- Contract Type
- Payment Method
- Monthly Charges
- Total Charges
- Churn Status

---

## 🔍 Exploratory Data Analysis (EDA)

Exploratory Data Analysis was performed to gain insights into customer behavior and identify factors influencing churn.

### Analysis Performed

- Churn Distribution Analysis
- Customer Tenure Analysis
- Monthly Charges Analysis
- Contract Type vs Churn
- Internet Service vs Churn
- Service Subscription Patterns
- Feature Relationship Analysis

### Visualization Tools

- Matplotlib
- Seaborn

---

## ⚙️ Machine Learning Pipeline Architecture

A complete Scikit-Learn pipeline was implemented to ensure a reproducible and leakage-free workflow.

### Pipeline Flow

```text
IBM Telco Customer Churn Dataset
                │
                ▼
        Data Understanding
                │
                ▼
      Data Cleaning & Preparation
      ├── Missing Value Analysis
      ├── Data Type Corrections
      └── Feature Selection
                │
                ▼
   Exploratory Data Analysis (EDA)
      ├── Churn Distribution Analysis
      ├── Contract Type Analysis
      ├── Service Usage Analysis
      ├── Tenure Analysis
      ├── Monthly Charges Analysis
      └── Feature Relationship Analysis
                │
                ▼
          Train-Test Split
                │
                ▼
         Feature Processing
      ├── Numerical Features
      │      └── StandardScaler
      │
      └── Categorical Features
             └── OneHotEncoder
                │
                ▼
   ColumnTransformer Integration
                │
                ▼
 Principal Component Analysis (PCA)
      └── Retain 95% Variance
                │
                ▼
     Multiple Model Training
      ├── Logistic Regression
      ├── Decision Tree
      ├── Random Forest
      ├── Gradient Boosting
      ├── K-Nearest Neighbors
      ├── Support Vector Machine
      └── XGBoost
                │
                ▼
      Cross Validation
      └── 5-Fold ROC-AUC Evaluation
                │
                ▼
      Model Comparison
      └── Performance Benchmarking
                │
                ▼
     Hyperparameter Tuning
      └── GridSearchCV
                │
                ▼
      Final Model Selection
                │
                ▼
      Model Evaluation
      ├── Accuracy
      ├── Precision
      ├── Recall
      ├── F1-Score
      ├── ROC-AUC
      └── Confusion Matrix
                │
                ▼
      Model Persistence
      └── Joblib Serialization
                │
                ▼
      Production-Ready Model
```

### Workflow Summary

#### 1. Data Cleaning & Preparation

- Inspected dataset structure and feature types.
- Checked for missing values and inconsistencies.
- Converted features into suitable formats for modeling.

#### 2. Exploratory Data Analysis (EDA)

- Analyzed customer churn behavior.
- Studied the impact of contracts, services, tenure, and billing information.
- Identified patterns and trends influencing churn.

#### 3. Feature Engineering & Preprocessing

- Numerical features were standardized using StandardScaler.
- Categorical features were encoded using OneHotEncoder.
- ColumnTransformer was used to combine preprocessing steps efficiently.

#### 4. Dimensionality Reduction

- PCA was applied after preprocessing.
- Components were selected to retain 95% of the total variance while reducing feature dimensionality.

#### 5. Model Development

Seven machine learning models were trained and evaluated:

- Logistic Regression
- Decision Tree Classifier
- Random Forest Classifier
- Gradient Boosting Classifier
- K-Nearest Neighbors (KNN)
- Support Vector Machine (SVM)
- XGBoost Classifier

#### 6. Cross Validation

- 5-Fold Cross Validation was performed.
- ROC-AUC was used as the primary evaluation metric for model comparison.

#### 7. Hyperparameter Optimization

GridSearchCV was used to optimize the best-performing model by tuning:

- Number of Estimators
- Learning Rate
- Maximum Depth
- Minimum Samples Split
- Minimum Samples Leaf
- Subsample Ratio

#### 8. Final Evaluation

The selected model was evaluated using:

- Accuracy
- Precision
- Recall
- F1 Score
- ROC-AUC Score
- Confusion Matrix
- Classification Report

#### 9. Model Persistence

The final trained model was serialized using Joblib, enabling future deployment and inference without retraining.

This version looks much more like a serious ML engineer's project README because it highlights the entire workflow, not just the Scikit-Learn preprocessing pipeline.
```

### Benefits

- Prevents Data Leakage
- Automates Preprocessing
- Improves Reproducibility
- Simplifies Model Training
- Facilitates Future Deployment

---

## 🤖 Models Evaluated

Multiple machine learning algorithms were trained and compared:

- Logistic Regression
- Decision Tree Classifier
- Random Forest Classifier
- Gradient Boosting Classifier
- K-Nearest Neighbors (KNN)
- Support Vector Machine (SVM)
- XGBoost Classifier

---

## 📈 Model Evaluation

Models were evaluated using:

- Accuracy Score
- Precision Score
- Recall Score
- F1 Score
- ROC-AUC Score
- Confusion Matrix
- Classification Report

### Cross Validation

To ensure reliable performance estimates, 5-Fold Cross Validation was performed using ROC-AUC as the evaluation metric.

---

## 🔧 Hyperparameter Tuning

The best-performing model was further optimized using **GridSearchCV**.

### Parameters Tuned

- Number of Estimators
- Learning Rate
- Maximum Depth
- Minimum Samples Split
- Minimum Samples Leaf
- Subsample Ratio

### Grid Search Configuration

- 5-Fold Cross Validation
- ROC-AUC Optimization
- Parallel Processing (`n_jobs=-1`)

---

## 💾 Model Persistence

The final trained model was saved using Joblib for future use and deployment.

```python
import joblib

joblib.dump(best_model, "churn_model.joblib")
```

---

## 🛠️ Technologies Used

### Programming Language

- Python

### Libraries

- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-Learn
- XGBoost
- Joblib

---

## 📁 Repository Structure

```text
IBM-Telco-Customer-Churn-Prediction/
│
├── README.md
├── LICENSE
├── .gitignore
├── requirements.txt
├── Telco-Customer-Churn.csv
└── IBM_Telco_Customer_Churn_Prediction.ipynb
```

---

## 🚀 Installation

### Clone the Repository

```bash
git clone https://github.com/shubhamm-27/IBM-Telco-Customer-Churn-Prediction.git
```

### Navigate to the Project Directory

```bash
cd IBM-Telco-Customer-Churn-Prediction
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

### Launch Jupyter Notebook

```bash
jupyter notebook
```

---

## 🎓 Key Skills Demonstrated

- Data Cleaning
- Exploratory Data Analysis
- Feature Engineering
- Data Preprocessing
- ColumnTransformer
- One-Hot Encoding
- Standard Scaling
- Principal Component Analysis (PCA)
- Cross Validation
- Model Comparison
- Hyperparameter Tuning
- Ensemble Learning
- Gradient Boosting
- XGBoost
- Model Serialization
- End-to-End Machine Learning Pipeline Development

---

## 📌 Future Improvements

Potential enhancements for this project include:

- Streamlit Web Application
- Flask API Deployment
- SHAP-Based Model Explainability
- LightGBM Integration
- Real-Time Prediction Interface
- Automated Model Monitoring

---

## 📜 License

This project is licensed under the MIT License.

---

## 👨‍💻 Author

**Shubham Sharma**

Aspiring AI Engineer | Machine Learning Enthusiast

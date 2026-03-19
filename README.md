# Task 4: Feature Engineering Challenge

## Overview
This repository contains the solution for **Task 4: Feature Engineering Challenge**, completed as part of my AI & Data Science Internship tasks.  

The task focuses on **improving machine learning model performance** for customer churn prediction using **feature engineering, feature selection, and model tuning**.

---

## Objective
The objective of this task is to enhance predictive modeling by:  
- Creating new features that capture **non-linear relationships** and **interactions**  
- Selecting the **most relevant features** using tree-based importance, correlation, and RFE  
- Training and evaluating a **robust Random Forest model**  
- Comparing performance **before and after feature engineering**

---

## Dataset
**Dataset Name:** Customer Churn Modelling Dataset  
**Type:** Structured CSV dataset  

### Dataset Description
- Total Records: **10,000**  
- Target Variable: **Exited**  
  - 1 → Customer left the bank (Churn)  
  - 0 → Customer stayed with the bank  
- Features:
  - CreditScore – Customer's credit score  
  - Geography – Country of residence  
  - Gender – Customer gender  
  - Age – Customer age  
  - Tenure – Years with the bank  
  - Balance – Account balance  
  - NumOfProducts – Number of bank products used  
  - HasCrCard – Whether the customer owns a credit card  
  - IsActiveMember – Whether the customer actively uses bank services  
  - EstimatedSalary – Estimated annual salary  

**Why this dataset is used**
- Binary target variable, suitable for classification  
- Mix of numerical and categorical features allows preprocessing and feature engineering  
- Large enough to train robust models  
- Well-known dataset in churn analysis, making results interpretable  

---

## Tools & Technologies Used
- Python  
- pandas  
- NumPy  
- Matplotlib & Seaborn  
- Scikit-learn  
- Jupyter Notebook / Google Colab  

---

## Approach

### 1️⃣ Data Loading & Cleaning
- Loaded the dataset using `pandas.read_csv()`  
- Removed unnecessary columns: RowNumber, CustomerId, Surname  
- Checked for missing values and handled them appropriately  
- Converted categorical features using one-hot encoding  

### 2️⃣ Exploratory Data Analysis (EDA)
- Visualized churn distribution using **countplots**  
- Examined correlations with a **heatmap**  
- Analyzed churn patterns by Geography and Age  

### 3️⃣ Baseline Model
- Separated features (`X`) and target (`y`)  
- Split dataset into **training and testing sets**  
- Trained a **Random Forest Classifier**  
- Evaluated baseline accuracy (~84–85%)  

### 4️⃣ Feature Engineering
- **Polynomial Features:** Captured non-linear relationships between numeric variables  
- **Interaction Features:** Created `Balance_Age` and `Salary_Tenure` to capture combined effects  
- **Binning:** Converted Age into categorical bins with one-hot encoding  

### 5️⃣ Feature Selection
- **Feature Importance:** Random Forest used to rank features  
- **Correlation Analysis:** Identified top correlated features  
- **Recursive Feature Elimination (RFE):** Selected the most relevant features (~50 features)  

### 6️⃣ Final Model Training
- Trained a **tuned Random Forest Classifier** with parameters:  
  - n_estimators=300  
  - max_features='sqrt'  
  - min_samples_leaf=2  
- Evaluated accuracy (~87–88%) and confusion matrix  
- Visualized **top 10 features** after RFE  

---

## Results & Insights
- Feature engineering improved model accuracy by 3–4%  
- Polynomial and interaction features captured complex patterns  
- Age binning helped understand group-based churn behavior  
- Feature selection reduced noise and improved model efficiency  
- Random Forest remained robust after tuning  

---

## Conclusion
This task demonstrates the **importance of feature engineering and data-driven optimization** for churn prediction.  
Key outcomes:
- Baseline Random Forest accuracy: ~84–85%  
- After feature engineering: ~87–88%  
- Structured approach combining **feature creation, selection, and model tuning** leads to better predictive models  

---

## Skills Gained
- Feature engineering: polynomial, interaction, and binning  
- Feature selection: importance, correlation, RFE  
- Model evaluation and tuning  
- Data preprocessing and handling categorical/numerical features  
- End-to-end machine learning workflow for structured datasets  

# Borrower Behaviour & Loan Characteristics: Default Risk & Expected Loss Analysis

## Table of Contents
1. Overview  
2. Research Question  
3. Dataset Information  
4. Methodology  
5. Key Models & Metrics  
6. Repository Structure  
7. How to Run  
8. Requirements  

## 1. Overview
This project analyses how borrower behaviour and loan characteristics influence loan default risk and how Expected Loss (EL) can be estimated using credit-risk modelling techniques. The repository demonstrates a complete workflow: data cleaning, feature engineering, model training, evaluation, and calculation of risk metrics such as PD, LGD, EAD, and EL.

The project is designed for academic, research, and portfolio use.

## 2. Research Question
**How can borrower behaviour and loan characteristics be analysed to estimate default risk and calculate Expected Loss?**

## 3. Dataset Information  
The dataset used is the **Lending Club Loan Data (2007–2014)** from Kaggle.  
It contains several hundred thousand observations and includes borrower-level financial attributes, loan terms, credit behaviour variables, and repayment outcomes.

Key features include:  
- **Loan attributes:** funded amount, interest rate, term, installment  
- **Borrower attributes:** credit history, employment length, annual income  
- **Behavioural indicators:** delinquencies, revolving utilization, public records  
- **Target variable:** loan_status converted into a binary default flag  

## 4. Methodology  
The analysis focuses on credit risk estimation and follows standard banking practices:

### **Data Preparation**
- Handling missing values  
- Converting categorical variables  
- Outlier analysis  
- Train-test split  

### **Feature Engineering**
- Credit utilization ratios  
- Debt-to-income transformations  
- Payment-to-income indicators  

### **Modelling**
- Logistic Regression (baseline)  
- Random Forest (non-linear benchmark)  

### **Performance Evaluation**
- ROC-AUC  
- KS Statistic  
- Gini coefficient  
- Confusion matrix  
- ECDF distribution for credit scores  

### **Expected Loss Calculation**
Applying the risk framework:
- **PD (Probability of Default)**: model estimated  
- **LGD (Loss Given Default)**: simplified assumption or proxy  
- **EAD (Exposure at Default)**: loan amount / funded amount  
- **EL = PD × LGD × EAD**

## 5. Key Models & Metrics  
The notebook includes:
- Probability of Default model  
- Credit scoring visualizations (ECDF, KS, ROC)  
- Interpretability through feature importance  

## 6. Repository Structure
```
├── data/
│   └── loan_data_2007_2014.csv
├── notebooks/
│   └── credit_risk_analysis.ipynb
├── README.md
├── requirements.txt
```

## 7. How to Run
```bash
pip install -r requirements.txt
jupyter notebook
```
Open the notebook:
```
notebooks/credit_risk_analysis.ipynb
```

## 8. Requirements
All required Python packages are listed in requirements.txt.

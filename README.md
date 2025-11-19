# Credit Risk Modeling: PD, LGD, EAD & Expected Loss
### *How Can Borrower Behaviour and Loan Characteristics Be Analysed to Estimate Default Risk and Expected Loss?*

## Overview
This project builds a complete credit risk modeling pipeline—from raw data cleaning to Probability of Default (PD), Loss Given Default (LGD), Exposure at Default (EAD), and Expected Loss (EL). The objective is to understand how borrower characteristics and loan features translate into measurable credit risk and quantify portfolio-level expected losses.

All notebooks included in this repository are fully executable and follow a transparent, interpretable approach to credit risk modeling.

## Dataset
Source: Kaggle — Loan Data 2007–2014  
Link: https://www.kaggle.com/datasets/devanshi23/loan-data-2007-2014

## Project Structure
- DATA PREPARATION.ipynb  
- PD MODEL.ipynb  
- LGD, EAD AND EXPECTED LOSS.ipynb 
- README.md
<img width="1200" height="400" alt="pipeline_diagram" src="https://github.com/user-attachments/assets/8b510cf9-167d-4000-ac1f-85229d2ec187" />

## Methodology
### 1. Data Preparation

Cleaned missing values

Normalised important variables (DTI, funded amount, credit score)

Engineered features relevant for credit risk (loan_status, recoveries, revol_util, grade, etc.)

Created dependent variables for PD, LGD, and EAD

Key Insight:
Borrowers who ultimately default show distinct patterns: higher DTI, lower credit scores, and higher interest rates.

### 2. Probability of Default (PD)

A binary classifier was used to estimate the likelihood of default.

Performance Metrics:

KS: 34

Gini: 0.45

Interpretation:
The model demonstrates moderate discriminatory power—sufficient to separate risky borrowers from safe ones for portfolio-level risk analysis.

### 3. Loss Given Default (LGD)

LGD was computed using:

𝐿
𝐺
𝐷
=
1
−
Recovery
Funded Amount
LGD=1−
Funded Amount
Recovery
	​


Observations:

Recoveries were low in most charged-off loans

LGD distribution is skewed towards high loss (often > 0.75)

Insight:
Once a loan defaults, the lender loses the majority of the funded amount.

### 4. Exposure at Default (EAD)

EAD was estimated using the funded amount and utilisation rates.

Insight:
Most loans in this dataset were fully drawn at default, leading to EAD values close to the original funded amount.

### 5. Expected Loss (EL)
EL
=
𝑃
𝐷
×
𝐿
𝐺
𝐷
×
𝐸
𝐴
𝐷
EL=PD×LGD×EAD

Finding:
EL increases sharply for:

High loan amounts

Borrowers with weak credit scores

High DTI ratios

This aligns with typical credit-risk behaviour in consumer lending portfolios.
     
## Model performances

Following models are trained for the use in our case  
1.  Probability of default (PD)  
**Model**: Logistic regression  
**Metrics**: Accuracy: 0.572 | Area under ROC: 0.684 > 0.50  

2.  Loss given default (LGD)  
**Model - Stage/step 1**: Logistic regression  
**Metrics**: Accuracy: 0.595 | Area under ROC: 0.640 > 0.50  
**Model - Stage/step 2**: Linear regression  
**Metric**: Accuracy: 0.777

3. Exposure at default (EAD)  
**Model**: Linear regression  
**Metric**: Accuracy: 0.658

## How to Use
1. Download dataset from Kaggle  
2. Adjust file paths in notebooks  
3. Run notebooks in the recommended order  

## License
MIT License

## Acknowledgements
LendingClub (data origin)  
Kaggle (data hosting)

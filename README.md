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
1. **Data Preparation**  
   - Cleaning, filtering, encoding, feature engineering  
2. **PD Modelling**  
   - Logistic regression, ROC/AUC, confusion matrix  
3. **LGD, EAD, EL Estimation**  
   - Recovery analysis, exposure computation, final EL framework
  
     
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

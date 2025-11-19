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
1. Preprocessing - Converting columns into dummy variables by fine and coarse classing
2. Calculate the PD model with logistic regression
3. Based on PD model, provide a practical scorecard in csv format
4. Construct LGD model with beta regression
5. Build EAD model with linear regression
6. Calculate the exposure loss after obtaining all models
7. Check the models if they are still doing good with the recent credit risk modeling.

## Model performances

Following models are trained for the use in our case  
1.  Probability of default (PD)  
**Model**: Logistic regression  
**Metrics**: Area under ROC: 0.70.17 > 0.50
<img width="571" height="457" alt="pd_model_1" src="https://github.com/user-attachments/assets/8884a14a-f5eb-489b-8668-37572d1f704f" />

gini= 0.40

<img width="570" height="457" alt="pd_model_3" src="https://github.com/user-attachments/assets/064922e7-07d3-4731-b483-86b2f873bf97" />

KS= 0.29 > 0 (It shows that two cummulative functions are sufficiently far away from each other and model has good predictive power.)
<img width="570" height="457" alt="pd_model_3" src="https://github.com/user-attachments/assets/e8c29d8f-67ee-4315-a02e-4b163bf15564" />


3.  Loss given default (LGD)  
**Model - Stage/step 1**: Logistic regression  
**Metrics**: Accuracy: 0.595 | Area under ROC: 0.66> 0.50
<img width="571" height="457" alt="image" src="https://github.com/user-attachments/assets/11076203-b79a-459f-8e88-88db7014a251" />
 
**Model - Stage/step 2**: Linear regression  
**Metric**: Accuracy: 0.777

5. Exposure at default (EAD)  
**Model**: Linear regression  
**Metric**: Accuracy: 0.658

6. Expected loss
   Total Expected Loss as a proportion of total funded amount for all loans- 0.075119.

*Please note that further steps can be taken forward to improve the performance of models.*

## Deliverables

1. Scorecard, easy to interpret in comliance with the requirements    
2. Dataframe to test the impact of cut off rates on the number of accepted borrowers for credit
3. Models on loss given default (LGD), exposure at default (EAD) and expected loss (EL)  
4. Schema to check the population stability index with the recent data  

## Key documents
	
Notebooks  
1 - A preprocessing notebook- data preparation
2 - A notebook on selecting features for probability of default (PD) and modelling PD  - PD modeling
3 - A notebook on modelling loss given default (LGD), exposure at default (EAD) and Expected Loss (EL)  



## How to Use
1. Download dataset from Kaggle  
2. Adjust file paths in notebooks  
3. Run notebooks in the recommended order  


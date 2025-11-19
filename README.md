# How Can Borrower Behaviour and Loan Characteristics Be Analysed to Estimate Default Risk and Calculate Expected Loss?
This project presents an end-to-end credit risk modelling workflow using Python. It demonstrates how borrower behaviour and loan characteristics can be analysed to estimate Probability of Default (PD) and calculate Expected Loss (EL) through the standard risk framework:

𝐸
𝐿 =
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


## Introduction

This project investigates whether borrower behaviour and loan characteristics can be systematically analysed to estimate credit default risk and calculate Expected Loss (EL). Using real-world consumer lending data, it follows the standard credit risk framework used in banks—Probability of Default (PD), Loss Given Default (LGD), and Exposure at Default (EAD).

The goal is not only to build models, but to walk through the steps a bank’s risk or modelling team would expect: cleaning raw lending data, analysing borrower behaviour, estimating PD, and calculating Expected Loss.

## Dataset
The dataset comes from Lending Club. It is a large US peer-to-peer lending company. Different versions of this dataset existing, here the data was taken from a version available on kaggle.com

It contains all available data of consumer loans issued from 2007 to 2014.

## Context

Credit risk sits at the core of financial stability. Banks make lending decisions based on imperfect information, under uncertainty, and under regulatory requirements.
Understanding which borrowers are likely to default, which loans are riskier, and how much the bank could lose, is essential for:

pricing loans

setting credit limits

provisioning capital

managing retail portfolios

## Project Structure

📁 DATA PREPARATION.ipynb  
    → Cleaning, filtering, feature creation, variable selection  

📁 PD MODEL.ipynb  
    → Exploratory analysis, ECDF plots, logistic regression, ROC, KS, calibration  

📁 LGD, EAD AND EXPECTED LOSS.ipynb  
    → Recovery rate analysis, EAD estimation, final Expected Loss calculation  

## Methodology
### 5.1 Data Preparation

Handling missing values

Encoding borrower features

Filtering relevant loan categories

Creating repayment / default targets

Standardising numeric variables

Initial distribution analysis

A strong focus was placed on creating meaningful variables that reflect borrower behaviour.

### 5.2 Probability of Default (PD) Modelling

Models used:

Logistic Regression (interpretable, finance-friendly)

Probability calibration

Performance diagnostics

Evaluation:

ROC Curve

AUC Score

KS Statistic

Confusion Matrix

ECDF visualisation (to assess separation between defaulters & non-defaulters)

The objective was not to build the most complex model, but to demonstrate the full PD pipeline as used in credit analytics teams.

### 5.3 LGD, EAD & Expected Loss

LGD: Estimated using recovery patterns

EAD: Taken as funded exposure at time of default

Expected Loss:

𝐸
𝐿
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

Calculated at the loan-level to produce portfolio-level risk insights.

## Key Findings

Borrowers with lower credit scores, higher debt-to-income ratios, and longer loan terms exhibited significantly higher default likelihood.

ECDF and ROC curves showed clear separations between repaid and defaulted loans, confirming strong behavioural patterns.

Logistic Regression produced stable and interpretable PD estimates, suitable for credit policy work.

LGD and EAD analysis provided realistic exposures, enabling complete Expected Loss calculations.

These findings reflect what risk teams observe in real lending portfolios.

## Visual Summary

The project includes the following visual analyses:

Distribution of credit scores

ECDF plots showing difference between defaulters & non-defaulters

Confusion matrix

ROC curve

KS plot

Expected Loss distribution

(Visuals are available directly in the notebooks.)


# UHS 30-Day Hospital Readmission Analysis

This repo contains the analysis and final report for a semester-long project examining 30-day hospital readmission rates at United Health Services (UHS) using Epic EHR data. The goal was to identify key drivers of readmission and evaluate the effectiveness of three care transition interventions across CMS-tracked conditions.

Here is the notebook:

- [Hand Written EDA](./Hand%20Written%20EDA.ipynb): Exploratory data analysis, feature engineering, and primary modeling pipeline

The final written report summarizing methodology, findings, and recommendations can be viewed here:

- [Final Project Report (PDF)](./Final%20Project%20Report%20-%20UHS.pdf)

## Overview

- Analyzed **5,200+ inpatient hospitalizations** from UHS Epic EHR data
- Evaluated three care transition interventions across CMS-tracked conditions
- Applied **inverse probability weighting** to balance treated/untreated groups, reducing standardized mean differences from 0.15 → 0.05 (risk score) and 0.20 → 0.004 (SDOH score)
- Built multivariable logistic regression models with robust standard errors
- Found **TCM within 7 days** was associated with a **7.8 percentage point reduction** in readmission probability, with the strongest effect in high-risk and under-70 patient subgroups
- Identified SDOH factors (transportation, food insecurity, housing instability) as high-priority pre-discharge intervention targets

## Methods

- Feature engineering: TCM follow-up time windows, composite transition bundle score, SDOH burden score
- Clustering: K-Modes on 13 binary social determinant flags
- Causal inference: Inverse probability weighting (IPW) for observational data
- Modeling: Multivariable logistic regression with robust standard errors

## Requirements

- Python 3.x
- Jupyter Notebook

## Dependencies

- pandas
- numpy
- scikit-learn
- matplotlib
- seaborn
- scipy

## Data

Raw data files are omitted from this repository as they contain de-identified patient records provided by UHS under a data use agreement. Analysis was conducted in compliance with applicable data privacy guidelines.

## Authors

Sophia Huang · Kendra Pinckney · Sophia Huang · Christopher Peraza · Daniil Pavelko · Binghamton University MS Data Analytics · Spring 2026

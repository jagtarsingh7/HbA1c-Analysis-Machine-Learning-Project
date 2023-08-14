# Machine Learning Project- HbA1c Analysis for Improved Diabetes Care

## Overview
This project analyzes the management of hyperglycemia in hospitalised patients and its impact on outcomes using a clinical database of 74 million encounters. The analysis focuses on the association between HbA1c measurement and early readmission, controlling for various factors. The goal is to provide insights into diabetes care during hospitalisation and suggest potential approaches for patient safety enhancement.

## Abstract
Effective hyperglycemia management in hospitalised patients significantly influences morbidity and mortality. This study analyzes a vast clinical database to assess diabetes care during hospitalisation and its relationship with HbA1c measurement. Multivariable logistic regression reveals that measuring HbA1c is associated with improved patient outcomes and lower inpatient care costs.

## Introduction
Hyperglycemia management's impact on patient outcomes is widely acknowledged. While structured protocols exist for intensive care units, inpatient management lacks standardization. This analysis examines diabetes care trends in a large clinical database to identify opportunities for improvement. The focus is on HbA1c measurement and its potential to reduce readmission rates.

## Methods
The data was preprocessed and analyzed using Python and Weka. Attributes like IDs were dropped, missing values were imputed with means, and outliers were treated using interquartile range. Skewed data was balanced to create a new dataset. StandardScaler was used for data standardization, and PCA and Random Forest were applied for feature selection. Random Forest, KNN, and Logistic Regression models were tested.

## Results
### Random Forest
- Initial accuracy: 58%
- Low recall and fscore

### Random Forest with Feature Selection
- Improved accuracy, fscore, and recall
- Features with score < 0.04 dropped
- Slight decrease in accuracy

### KNN
- Recall and fscore better than Random Forest
- Accuracy lower

### Logistic Regression
- Outperformed other models
- Higher accuracy, fscore, precision, and recall

## Discussion
Logistic Regression proved most suitable for this dataset due to its high accuracy and importance on fscore. Feature selection with PCA was effective, and accuracy and fscore were prioritized. Logistic Regression is recommended for similar datasets.

Dataset Link: [Diabetes 130-US hospitals for years 1999-2008](https://archive.ics.uci.edu/ml/datasets/Diabetes+130-US+hospitals+for+years+1999-2008)


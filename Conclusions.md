# **Conclusions**

## **Resampling**

### 1) Which model had the best balanced accuracy score?

I used four different resampling models for my analysis:
Naive random oversampling, SMOTE oversampling, Cluster Centroids undersampling, and a SMOTEENN combination over and under sampling model. In addition, I started the analysis with a simple logistic regression model. The naive random oversampling, SMOTE oversampling model, and the SMOTEENN combination sampling models produced the highest balanced accuracy score. All three models produced an identical balanced accuracy score of roughly 0.999347

### 2) Which model had the best recall score?

All four resampling models produced identical recall scores of 0.99 for both the "high_risk" and "low_risk" predictions. While the simple logistic regression model posted an overall recall rate of 0.99, the model only posted a recall rate of 0.91 for "high_risk" predictions.

### 3) Which model had the best geometric mean score?

All four resampling models produced identical geometric mean scores of 0.99. The simple logistic regression model produced the lowest geometric mean score of 0.95.

## **Ensemble Learning**

### 1) Which model had the best balanced accuracy score?

For this analysis, I used two different ensemble classifiers to predict loan risk: the Balanced Random Forest Classifier and the Easy Ensemble Classifier. Between the two, the Easy Ensemble Classifier has a significantly higher balanced accuracy score of 0.93. In comparison, the Balanced Random Forest Classifier has a balanced accuracy score of only 0.79.

### 2) Which model had the best recall score?

Once again, the Easy Ensemble Classifier model has the best recall score. The EEC total recall rate of 0.94 surpasses the BRF classifier's total recall score of 0.87. Additionally, the EEC has higher recall scores for both the "high_risk" (0.92 for EEC vs. 0.70 for BRF) and "low_risk" (0.94 for EEC vs. 0.87 for BRF) predictions.

### 3) Which model had the best geometric mean score?

The EEC has the best geometric mean score of 0.93. The BRF classifier has a lower geometric mean of 0.78, in contrast.

### 4) What are the top three features?

The top three features all appear to be related to the loan payment. Specifically, the top three features are total principal received (tot_rec_prncp), total loan payment (tot_pymnt), and total payment invoiced (tot_pymnt_inv). The most important feature for predicting loan risk appears to be the portion of the loan payment that represents the principal payment. This makes sense. As the borrower pays down more of the principal (i.e. original loan amount), the lender's potential loss on the original loan decreases. As the potential loss decreases, credit risk also decreases from the lender's perspective. 
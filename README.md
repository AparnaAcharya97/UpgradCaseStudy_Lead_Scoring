# Lead Scoring Model for X Education

## Overview

The objective of this project was to develop a lead scoring model to identify and prioritize leads most likely to convert into paying customers for X Education. The CEO has set a target lead conversion rate of approximately 80%. Our goal was to create a model that assigns lead scores such that leads with higher scores have a greater likelihood of conversion.

## Model Selection

We used a Logistic Regression model for this task due to its effectiveness in binary classification problems and its ability to provide probability scores indicating the likelihood of conversion.

## Steps and Methodology

### 1. Data Preparation

#### 1.1 Data Cleaning

- **Removed Columns:** Excluded columns with more than 3,400 null values as they were deemed to have little utility.
- **Removed Rows:** Eliminated rows with missing values in the remaining columns to ensure the quality and completeness of the dataset.

#### 1.2 Feature Engineering

- **Categorical Variables:** Transformed categorical variables into dummy variables.
  - Created binary columns for each category within the categorical features to make them suitable for logistic regression analysis.

#### 1.3 Data Scaling

- **Technique Used:** MinMaxScaler
  - Normalized the feature range to ensure that all features contribute equally to the model.

### 2. Data Splitting

- **Training and Testing Split:** Allocated 70% of the data for training the model and 30% for testing.
  - This split was essential for evaluating the model's performance on unseen data.

### 3. Feature Selection

- **Method Used:** Recursive Feature Elimination (RFE)
  - Selected the top 15 features based on their importance to the model.

### 4. Model Building and Refinement

- **Initial Model:** Built a logistic regression model using the selected features.
- **Refinement Process:**
  - Removed variables with high Variance Inflation Factor (VIF) and insignificant p-values to reduce multicollinearity and enhance model interpretability.

### 5. Model Validation

- **Initial Validation:** Used a random cutoff value to assess the model’s performance.
- **Refined Validation:**
  - Employed the Receiver Operating Characteristic (ROC) curve to determine a more reliable cutoff value for classification.

### 6. Performance Evaluation

- **Precision-Recall Curve:** Plotted to evaluate the model’s performance in terms of precision and recall.
  - Results were satisfactory, indicating effective model performance.

- **Test Data Metrics:**
  - Sensitivity
  - Specificity
  - Precision
  - Recall
  - Accuracy

  These metrics provided a comprehensive assessment of the model's effectiveness in predicting lead conversion.

## Summary

Through a structured approach involving data cleaning, feature engineering, model building, and rigorous validation, we developed a logistic regression model that aligns with X Education’s conversion goals. The final model is capable of scoring leads effectively, ensuring that leads with higher scores have a greater likelihood of converting into paying customers, thereby meeting the CEO’s target conversion rate of 80%.

## Usage

To use the model, ensure that your data is cleaned and transformed in a similar manner as described above. You can then apply the logistic regression model to score leads and prioritize those with higher conversion probabilities.




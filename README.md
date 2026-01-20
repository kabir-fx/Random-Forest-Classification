# Random Forest Classification Analysis

This directory contains an implementation of **Random Forest Classification**, an ensemble learning method that uses multiple decision trees to classify users based on their age and estimated salary.

## Dataset Overview

The model uses the `Social_Network_Ads.csv` dataset, which includes:

- **Features**:
  - `Age`: The age of the user.
  - `EstimatedSalary`: The estimated annual salary of the user.
- **Target**:
  - `Purchased`: Binary classification (0 = No, 1 = Yes) indicating if the user purchased the product.

## Implementation Steps

The implementation follows these key steps:

1.  **Data Preprocessing**:
    - Split the dataset into Training (75%) and Test (25%) sets.
    - Applied **Feature Scaling** (Standardization) to normalize `Age` and `Salary`.
2.  **Model Training**:
    - Used `sklearn.ensemble.RandomForestClassifier` with `n_estimators = 100`.
    - Criterion used: **'entropy'**.
    - Reproducibility ensured with `random_state = 0`.
3.  **Prediction and Evaluation**:
    - Predicted a new result for Age 30 and Salary $87k.
    - Evaluated the model using a **Confusion Matrix**.
4.  **Visualization**:
    - Plotted decision boundaries for both Training and Test sets to show how the ensemble of trees creates a non-linear boundary.

## Results

The Random Forest model demonstrates robust performance:

- **Accuracy**: 91% on the test set.
- **Confusion Matrix**:
  - True Negatives: 63
  - False Positives: 5
  - False Negatives: 4
  - True Positives: 28
- The model effectively captures complex, non-linear patterns in user behavior, outperforming simpler linear classifiers.

# Breast Cancer Regression Analysis

This project demonstrates a regression analysis using the Breast Cancer dataset from `scikit-learn`. The dataset, originally designed for classification, is adapted for regression by using continuous features as the target variable. The analysis evaluates multiple machine learning models, visualizes results, and explores stacking and ensemble methods for optimization.

## Project Structure

- **Data Preparation**: The `mean radius` is used as the continuous target variable, with PCA applied to reduce dimensionality.
- **Model Testing**: Evaluates four regression models:
  1. Random Forest
  2. Gradient Boosting
  3. XGBoost
  4. LightGBM
- **Optimization**:
  - Hyperparameter tuning with `GridSearchCV`.
  - Stacking regressor combining multiple models for improved performance.
- **Visualization**: 
  - Feature importance plots.
  - Residual plots to analyze prediction errors.

## Installation

### Prerequisites
Make sure you have Python 3.7+ installed. Install the required packages:

pip install pandas numpy scikit-learn xgboost lightgbm matplotlib
Dataset
The dataset is directly loaded from scikit-learn:

python
Copy code
from sklearn.datasets import load_breast_cancer
Usage
1. Data Preparation
Features are scaled using StandardScaler to normalize ranges.
PCA reduces dimensionality, retaining the 10 most significant components.
2. Model Training
The following models are trained and evaluated:

Random Forest: Baseline ensemble model for regression.
Gradient Boosting: Boosts weak learners to reduce errors.
XGBoost: High-performance gradient boosting model.
LightGBM: Lightweight boosting model optimized for speed and accuracy.
3. Stacking Regressor
Combines multiple models with a Gradient Boosting regressor as the meta-learner. This improves overall accuracy by leveraging the strengths of individual models.

4. Visualization
Feature Importances: Shows the relevance of PCA components.
Residual Plots: Highlights prediction errors and potential model biases.
5. Metrics
Mean Squared Error (MSE): Measures average prediction error.
R-squared (R²): Indicates variance explained by the model.
Accuracy Percentage: Derived from R².
Results
Metrics Overview:
Random Forest:
MSE: ~0.03
R²: ~0.86
Gradient Boosting:
MSE: ~0.025
R²: ~0.88
XGBoost:
MSE: ~0.024
R²: ~0.89
LightGBM:
MSE: ~0.023
R²: ~0.89
Stacking Regressor:
MSE: ~0.020
R²: ~0.91
Visualizations:
Feature Importance: Highlights the PCA components contributing most to predictions.
Residual Plots: Displays the distribution of errors for each model.
How to Run
Run the script to train models, evaluate them, and visualize results:


python breast_cancer_regression.py
File Overview
breast_cancer_regression.py: Main script for loading data, training models, and visualizing results.
Plots: Automatically generated during runtime:
Feature importance bar charts.
Residual scatter plots.
Future Enhancements
Add more advanced feature engineering techniques.
Test other regression algorithms (e.g., Support Vector Regressor, Neural Networks).
Perform in-depth hyperparameter tuning for all models.
Integrate cross-validation for robust evaluation.
License
This project is licensed under the MIT License. Feel free to use and modify.

Contributors
Developed by Prashasti Satpathi.


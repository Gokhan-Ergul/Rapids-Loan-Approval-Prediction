# Loan Approval Prediction - Kaggle Competition

This repository, rapids loan-approval-prediction, contains my solution for the Loan Approval Prediction competition on Kaggle. I achieved a strong result by leveraging multiple machine learning models, optimization techniques, and GPU-accelerated feature engineering.

## Overview
The goal of this competition was to predict loan approvals using a synthetic dataset generated from a deep learning model. The dataset's feature distributions are similar, but not identical, to the original Loan Approval Prediction dataset. This allowed opportunities to incorporate additional insights or techniques for improving performance.

## Approach
### 1. Feature Engineering
Feature engineering was performed using RAPIDS (cuDF and cuML libraries), enabling GPU-accelerated data preprocessing. This significantly reduced computation time and allowed for rapid iteration on feature creation and transformations.

Key steps include
- Handling missing values.
- Generating new features from existing ones.
- Normalizing and encoding categorical variables.
- Optimizing feature data types for GPU compatibility.

### 2. Models Used
I utilized an ensemble of the following models
- XGBoost
- CatBoost
- LightGBM

Each model was optimized using Optuna, an automated hyperparameter optimization framework. The optimized models were fine-tuned for maximum performance.

### 3. Model Optimization with Optuna
Optuna was used to
- Perform hyperparameter tuning for each model.
- Maximize evaluation metrics such as AUC (Area Under the Curve).

### 4. Model Ensemble
To improve performance further, I combined the predictions of all three models (XGBoost, CatBoost, and LightGBM) using a weighted ensemble approach. The weights were carefully selected based on model performance on the validation set.

### 5. Final Submission
The final predictions were generated by blending the optimized models' outputs and applying the selected weights to achieve the best possible result.

## Dataset
The competition dataset consists of train and test sets generated from a deep learning model trained on the original Loan Approval Prediction dataset. Key points about the dataset
- Feature distributions are similar to, but not identical to, the original dataset.
- Incorporating insights from the original dataset was encouraged to improve model performance.

You can explore the original dataset for additional analysis and comparison.

## Results
By combining RAPIDS-based feature engineering, hyperparameter optimization, and model ensembling, I achieved a competitive score in the competition and secured a strong ranking.

## File Structure
- `loan_approval_prediction.ipynb` Kaggle notebook containing the full implementation.
- `data` Folder containing the train and test datasets.
- `README.md` Project overview (this file).

## Technologies Used
- Python 3.10
- RAPIDS (cuDF, cuML) for GPU-accelerated data processing
- XGBoost, CatBoost, and LightGBM for machine learning models
- Optuna for hyperparameter optimization
- Kaggle for model development and testing

## How to Run
1. Clone this repository
   ```bash
   git clone httpsgithub.comusernamerapids-loan-approval-prediction.git
   cd rapids-loan-approval-prediction
   ```
2. Install dependencies
   ```bash
   conda create --name rapids-ml python=3.10
   conda activate rapids-ml
   pip install cudf cuml xgboost catboost lightgbm optuna
   ```
3. Run the notebook
   - Open `loan_approval_prediction.ipynb` in Jupyter Notebook or your preferred environment.
   - Follow the steps to reproduce the solution.

## Conclusion
This project demonstrates the power of GPU-accelerated feature engineering with RAPIDS, combined with modern machine learning techniques and hyperparameter optimization for achieving strong results in competitive machine learning tasks.

Feel free to reach out if you have any questions or suggestions!

Author [Gökhan Ergül]  
Kaggle Profile [https://www.kaggle.com/gokhanergul]  
GitHub [https://github.com/Gokhan-Ergul]


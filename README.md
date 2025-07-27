Credit Card Fraud Detection with Machine Learning

This project uses machine learning to detect fradulent transaction in credit card data. Due to imbalance in data (less ten 0.1% of data is fradulent) I've given special attention to model evaluation and class imbalance handling.

Dataset

The dataset used is from Kaggle: Credit Card Fraud Detection (https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud/data)
It contains 284,807 transactions, of which only 492 are fraudulent.

Project overview

- Sampled 10% of the data for faster experimentation
- Scaled features using `StandardScaler`
- Trained and compared:
  - Logistic Regression
  - Support Vector Machine
  - Random Forest
  - XGBoost
- Used Stratified K-Fold Cross-Validation and ROC AUC as evaluation metric
- Handled class imbalance using:
  - `scale_pos_weight` (XGBoost)
  - Baseline model comparison (`DummyClassifier`)
- Performed GridSearchCV to tune XGBoost hyperparameters
- Evaluated the best model using:
  - ROC Curve
  - Confusion Matrix
  - Classification Report

Results

- Best Model: XGBoost with tuned hyperparameters
- ROC AUC: ~0.99 on test data
- Classification report and confusion matrix show strong recall on the fraud class

Technologies Used

- Python
- Jupyter Notebook
- pandas, numpy
- scikit-learn
- xgboost

License

This is an educational project.  
The dataset is provided by Kaggle and is subject to their license.

Author

Ognjen Lukic


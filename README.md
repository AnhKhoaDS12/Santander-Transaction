
# Santander-Customer-Transaction-Prediction




## Description
+ Santander is a multi-national corporation that deal in various sectors such as Banking. They provided an anonymized dataset with 200 variables describing various charateristics that lead to a customer carrying out or not carrying out a transaction. 
+ In this project we have used machine learning algorithms for predict which customers will make a specific transaction in the future, irrespective of the amount of money transacted.
## Dataset
+ Download the dataset for custom training
+ https://www.kaggle.com/competitions/santander-customer-transaction-prediction/data

## Model Building Process
1. Data Collection
2. Exploratory Data Analysis (EDA)

+ Target Feature: transaction
+ Description: which customers will make a specific transaction in the future, irrespective of the amount of money transacted.
+ Key: 0 = did not transaction, 1 = transaction
+ All numeric features
+ Anonymous features
+ No missing values
+ There are 10.049% target values with 1 (imbalanced dataset)
+ Correlation: there is no linear relationship among the features and target but there may be some non-linear relationship that will help the model.
+ Split (Train 80% - valid 20%)
+ All features are normally distributed

3. Feature Engineering
+ Handling imbalanced dataset: use undersampling
+ Scaling down the data: Standardize features by removing the mean and scaling to unit variance.

4. Feature Selection
+ We've reduced 200 dimensions to just 2 by PCA (Principal Component Analysis)

5. Model Building
+ We use 7 algorithms (Naive Bayes, decision tree, random forests, K-NN, gradient boosting, XGBoost, LightGBM) for training and predict test set.
+ We choose LightGBM for hyperparameter training.
+ Result(valid set): accuracy(79%), f1 score (41%)
6. Evaluation
+ New data come, accuracy was approximately 0.77, model is not overfitting.
+ We still need to improve the accuracy of the model as well as the f1 score by other methods of data preprocessing and other algorithms.
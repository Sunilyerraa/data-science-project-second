**Introduction**

Customer churn occurs when a customer stops using a company's products or services.

Customer churn affects profitability, especially in industries where revenues are heavily dependent on subscriptions or other services. It is estimated that acquiring a new customer can cost up to five times more than retaining an existing one.

Therefore, customer churn analysis is essential as it can help a business by identify problems in its services (e.g. poor quality product/service, poor customer support, wrong target audience, etc.), and make correct strategic decisions that would lead to higher customer satisfaction and consequently higher customer retention.

**Objective**

The goal of this notebook is to understand and predict customer churn on the given dataset. Specifically, I will initially perform Exploratory Data Analysis (EDA) to identify and visualise the factors that contribute to customer churn. This analysis will later help me to build Machine Learning models to predict whether a customer will churn or not.

This is a typical classification problem. The task does not specify which performance metric to use for optimising our machine learning models. I decided to use recall besides calculating other metrics since correctly classifying elements of the positive class (customers who churned) is more important.

**Skills**: Exploratory Data Analysis, Data Visualisation, Data Preprocessing (Feature Selection, Encoding Categorical Features, Feature Scaling), Addressing Class Imbalance (SMOTE), Model Tuning.

**Models Used**: Logistic Regression, KNN, Gaussian NaiveBayes,Decision Trees, Random Forests, Gradient Boosting, XGBoost, AdaBoost and Multi-Layer Perceptron Classsifier

**Libraries**

I start by importing the necessary libraries and setting some parameters for the whole notebook. I will mainly use:

Pandas for handling and analysing data, Seaborn and Matplotlib for data visualization, and Scikit-learn for building Machine Learning models.

Details about the dataset
The dataset consists of 111300 observations and 31 variables. Independent variables contain information about customers. Dependent variable refers to customer status i.e. whether churned or retained

**Result**

As the problem here is to predict the customers who will leave(churn) the Business, I will give first importance to perfrmance metric such as 'Recall' on Target label 1 (Churned) followed by accuracy. If we are good at predicting which memebers leave then the metric 'Recall' is very important.
The given dataset is slightly imbalanced.I have developed various classification models after removing correlated and two more features from dataset , among those XGB classifier with hyperparamter tuning has given good results with accuracy 82.01 and Recall 0.76 on class labe =1 (customers who churned) wit slightly imbalanced dataset

After balancing the dataset the same model XGB classifier gave accuracy= 84.8 and Recall = 0.84 on class label =1 (customers who churned)

I did feature importance using different feature selection methods and developed models with most important features. Among developed models with most important features of dataset, Gradient Boosting Classifier with hyper paramter tuning produced good results with accuracy 81.6 and Recall 0.75 on slightly imbalanced dataset.

After balancing the dataset the same model Gradient Boosting classifier gave accuracy= 84.4 and Recall = 0.85 on class labe =1 (customers who churned).

Overall The Naive Bayes classifier has very good 'Recall' = 0.93(Label =1) on balanced dataset of important features on target

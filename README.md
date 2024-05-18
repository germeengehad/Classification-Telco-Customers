   # Classification Telco Customers :Project Overview
![Telco Image](https://github.com/germeengehad/Classification-Telco-Customers/blob/main/Telco-Improve-CX-Featured-Image_01-min.jpg)

 - This project aims to classify customers into churn or non-churn categories. Churn refers to customers who have discontinued their services within the last month. The goal is to assist companies in understanding the reasons behind customer churn and predicting which customers are likely to leave the company based on available data.
- I plan to conduct exploratory data analysis (EDA) on my dataset, followed by data preprocessing, feature selection, and feature engineering. Subsequently, I intend to apply various machine learning models, including logistic regression, support vector machine (SVM), naive Bayes, k-nearest neighbors (KNN), decision tree, random forest, gradient boosting, and XGBoost. Finally, I will evaluate the performance of these models and select the best-performing one for my dataset.
  
# The Data Set
- The dataset is stored in a CSV file format on this repo (above), with each row representing a unique customer and each column containing specific attributes outlined in the column metadata. In total, the dataset comprises 7043 rows (customers) and 21 columns (features). The "Churn" column serves as our target variable, indicating whether a customer has discontinued their services.
- The data set includes information about:
  -   Customers who left within the last month ( the column is called Churn)
  -  Services that each customer has signed up for ( phone, multiple lines, internet, online security, online backup, device protection, tech support, and streaming TV and movies)
  -  Customer account information ( how long they’ve been a customer, contract, payment method, paperless billing, monthly charges, and total charges)
  -  Demographic info about customers ( gender, age range, and if they have partners and dependents)
     
# EDA
- I applied an ANOVA test to ensure that all the numerical features are significant.
- I conducted a search for outliers in the dataset.
- I generated histograms to visualize the distribution of the data.
- I applied a Chi-Square test to ensure that all the categorical features are significant.

# Data Cleaning And Data Preprossing
- Handling missing values by replacing them with the median.
- Removing duplicate values from the dataset.
- Applying target encoding to encode the target column (churn).
- Converting the 'SeniorCitizen' column to object type.
- Handling skewed data by applying the Yeo-Johnson transformation.
- Dropping insignificant columns ('gender', 'PhoneService').
- Applying one-hot encoding to categorical features.

# Feature Engineering And Feature Selection
- Applying Filter Methods using correlation analysis.
- I removed ('Partner_Yes','Dependents_Yes', 'PaperlessBilling_No','tenure') from the data becuse they high correlated together.

# Model Building
- Data Preparation steps:
  1)  Data Separation as X and Y=(Churn)
  2)  Split the data into training set (70% of the data), validation set(10% of the data), and test set (20% of the data).
  3)  Handling the imbalanced data by appling undersampling to the training data
  4)  Scale the data
- I tried Eight Different Models and i used GridsearchCV to find the best parameter for my models.

# Model Performance On val Set
![model](https://github.com/germeengehad/Classification-Telco-Customers/blob/main/Screenshot%20(404).png)

# Choose The Best Model
from these outputs, I will choose the SVM model as the best model to predict this data, because it has the lowest difference between the train and test sets' accuracy
  


 
    

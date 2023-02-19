# Credit_card_fraud_detection_Sampling_techniques

In this assignment, you will be working with a dataset of credit card transactions, with the goal of building a model that can predict whether a transaction is fraudulent or not. The dataset can be found in this GitHub repository.

# Objective
Your objective is to build and evaluate multiple models using different sampling techniques to address the issue of imbalanced data. Specifically, you will evaluate the performance of each model on the following five sampling techniques:

*Random under-sampling  
*Random over-sampling  
*SMOTE (Synthetic Minority Over-sampling Technique)  
*Tomek links  
*NearMiss  

You will use the following five classifiers:

*Logistic regression  
*Decision tree  
*Random forest  
*Stochastic Gradient Descent  
*Extra trees  

For each classifier, you will evaluate its performance using each of the five sampling techniques, and report the accuracy score of the model under each combination.

# Getting Started
To get started, you should download the dataset from the GitHub repository mentioned above. The dataset consists of one CSV file, which you can load using the pandas library. You should split the data into features and target, and then split the data into training and testing sets using train_test_split from sklearn.model_selection. You can use a test size of 0.2 and a random state of 42.

You should then define the five sampling techniques and five classifiers mentioned above using the imblearn and sklearn libraries. For the sampling techniques, you should set the appropriate values for the hyperparameters of each technique. For the classifiers, you can use the default hyperparameters.

Once you have defined the sampling techniques and classifiers, you should define a dictionary to hold the samplers and models. You will use this dictionary to evaluate the performance of each model under each sampling technique.

# Sampling and Evaluation
To evaluate the performance of each model, you will use a nested loop that iterates over each sampling technique and each classifier. For each combination of sampling technique and classifier, you will undersample or oversample the training data using the appropriate sampling technique, and train the classifier on the resampled data. You should then make predictions on the test data and calculate the accuracy score of the model.

You should limit the resampled data to a sample size calculated using the formula:

# Formula Used
# n = ceil((z**2 * p * (1-p)) / (m**2))

where z is the z-value for the desired confidence level (use 1.96 for 95% confidence), p is the desired proportion of the minority class in the resampled data (use 0.5 for random under-sampling, and 0.05 for the other techniques), and m is the desired margin of error (use 0.05).

You should store the accuracy score of each model under each combination of sampling technique and classifier in a dictionary, and print the results at the end.

# Requirements
To complete this assignment, you should have a working knowledge of numpy, pandas, sklearn, and imblearn. You should also be familiar with basic machine learning concepts, such as classification and evaluation metrics.  

# Results
|                                  |           |           |           |           |           |
|----------------------------------|-----------|-----------|-----------|-----------|-----------|
| Results:                         | Sampling1 | Sampling2 | Sampling3 | Sampling4 | Sampling5 |
| M1 (Logistic Regression)         | 0.4323    | 0.9935    | 0.9935    | 0.9935    | 0.3742    |
| M2 (Decision Tree)               | 0.7097    | 0.9806    | 0.9806    | 0.9806    | 0.5484    |
| M3 (Random Forest)               | 0.6903    | 0.9935    | 0.9935    | 0.9935    | 0.7677    |
| M4 (Extra Tree)                  | 0.6065    | 0.9935    | 0.9935    | 0.9935    | 0.6516    |
| M5 (Stochastic Gradient Descent) | 0.0065    | 0.9935    | 0.9935    | 0.9935    | 0.2839    |  

# Good luck!

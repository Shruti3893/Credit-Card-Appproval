README.md

# Credit Card Appproval : Classification Project

# Context:
Credit score cards are a common risk control method in the financial industry. It uses personal information and data submitted by credit card applicants to predict the probability of future defaults and credit card borrowings. The bank is able to decide whether to issue a credit card to the applicant. Credit scores can objectively quantify the magnitude of risk. Generally speaking, credit score cards are based on historical data. Once encountering large economic fluctuations. Past models may lose their original predictive power. Logistic model is a common method for credit scoring. Because Logistic is suitable for binary classification tasks and can calculate the coefficients of each feature. In order to facilitate understanding and operation, the score card will multiply the logistic regression coefficient by a certain value (such as 100) and round it.

At present, with the development of machine learning algorithms. More predictive methods such as Boosting, Random Forest, and Support Vector Machines have been introduced into credit card scoring. However, these methods often do not have good transparency. It may be difficult to provide customers and regulators with a reason for rejection or acceptance.

# Acceptance criteria: 
Build a machine learning model to predict if an applicant is 'good' or 'bad' client, different from other tasks, the definition of 'good' or 'bad' is not given. You should use some techique, such as vintage analysis to construct you label. Also, imbalance data is a big problem in this task. Need to resolve the same for better results.

# Milestones: 
70 days to complete the Project.

# Process flow for the Project include below steps:-

## [1. Business Objective]
The Business Objective for this Project is to predict if an applicant is 'good' or 'bad' client for Credit Card Approval.

## [2. DataSet Details]
-We are provided with two sets are data which are namely Application dataset and Credit dataset.

- Application Dataset : This Dataset has ~4 lakh entries and 18 columns which has all the required data of the client/customer of the bank who has applied for Credit Card.

- Credit Dataset : This dataset has our Target Variable. Dimensions of the data are seen to have 3 columns and approx ~10lakh entries. 

[application_record.csv](https://github.com/Shruti3893/Credit-Card-Appproval/blob/main/application_record.csv) - Link for Application Dataset.

[credit_record.csv](https://github.com/Shruti3893/Credit-Card-Appproval/blob/main/credit_record.csv) - Link for Credit Dataset.

## [3. Exploratory Data Analysis]

### 1) Data Visualization:
- For getting Initial Overview of Dataset I choose to get Pandas Profiling Report. Below is the link for the same.

https://github.com/Shruti3893/Credit-Card-Appproval/blob/main/Pandas_Profiling_Credit_Card_Data.html

- Basic Visualizations are done in the Jupyter notebook which includes Univariate, Bivariate and Multivariate analysis of clean data.

### 2) Data Analysis:
- I did Missing Value Treatment on some features of Application Dataset. 
- I eliminated duplicates among the columns. 
- I dealt with some misclassified/misinterpreted data in some columns. 
- Treated Outlier for some columns to get better results.
- Checked Correlation among variables using heatmap.

### 3) Data Preprocessing:
- Dummified some categorical varibales. 
- All the columns are standardized before Train-Test split.
- For treating imbalanced data, I used SMOTE algorithm for increasing minority class entries.

### 4) Feature Selection:
I checked feature importance both graphically and analytically to come up with the list of desired columns for final model.

## [4. Model Building]
- I tried building various models with multiple algorithms such as 
1) Logistic Regression
2) Decision Tree Classifier
3) Random Forest Classifier
4) KNeighbors Classifier 
5) SVC

- I also tried building models with multiple meta algorithms such as 
1) XGBoost Classifier
2) CatBoost Classifier
3) LGBM Classifier 

- Based on the Classification report, I chose the best model as XGBoost Classifier for the project. It gave highest Accuracy, Precision, Recall and F1-score.

## [5. Model Evaluation]
For model evaluation, I checked the performance of the model on test data and results turned out to be good.

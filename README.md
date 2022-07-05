# Titanic - Machine Learning from Disaster
# Introduction
This is a basic machine learning competition on Kaggle,It is an active competition with 7,600 submissions
The aim of the dataset is to predict survivability of passengers on titanic

Link: https://www.kaggle.com/competitions/titanic/overview
# Dataset Details

Train fle : 891 rows and 11 features

Test file : 418 rows and 10 features

Features: passenger Id, survived(dependent variable), P class, Name, Sex, Age, SibSp(no. of Sibling/spouses on board), Parch(no. of parents/children on board), Ticket, Fare, Cabin, Embarkment

Evaluation : by accuracy score 

# Work Flow
Data cleaning : 
* dropped these features based on my intuition as they do not affect the survivability of a person.  - Passenger Id, Name, Ticket, Cabin
* Filled missing values ( Age and fare) by using mean value

Visualization:
* used Bar Graphs to understand the survivability based on gender,Ticket class,embarkment
* Heat map to find corelation b/w data

Pre-processing:
* Converting categorical variables using LabelEncoder for Sex, dummies for Embarkment section
* Scaling the data using standard scalar.

Model:
* Random forests (depth = 5 , n = 1000)
* Logistic Regression 

# Result


|Model |Accuracy |Rank
|--------|---------|-------|
|logistic regression |0.77033|9000|
|Random forests with robust scaler |0.77751|4211|
|Random forest with Knn imputation& SS|0.78708|2193|
|Random forests with mean age val & SS|0.79425|855|

SS - standard scaler

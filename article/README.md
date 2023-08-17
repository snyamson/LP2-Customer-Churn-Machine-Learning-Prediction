![diversity-people-digital-device-communication-concept](https://github.com/snyamson/LP2-Customer-Churn-Machine-Learning-Prediction/assets/58486437/572bb419-d562-494b-add2-4d0c4aaaf1c7)
# Unlocking Insights: Decoding Telecommunication Customer Churn Through Machine Learning

# Introduction
In the dynamic and ever-evolving landscape of the telecommunications industry, customer churn has become a critical challenge for service providers. The ability to predict and understand customer churn can significantly impact business success, customer retention strategies, and ultimately, the bottom line. 
In this project, we embark on an exciting journey to explore and analyze customer churn within the Vodafone network service using the CRISP-DM (Cross-Industry Standard Process for Data Mining) framework. 
Our aim is to leverage data-driven insights to identify key factors influencing churn, build predictive models, and develop actionable recommendations that can help Vodafone proactively retain valuable customers and enhance their overall service offerings.

# Business Understanding
In the dynamic and ever-evolving landscape of the telecommunications industry, customer churn has become a critical challenge for service providers. The ability to predict and understand customer churn can significantly impact business success, customer retention strategies, and ultimately, the bottom line. 

In this project, we embark on an exciting journey to explore and analyze customer churn within the Vodafone network service using the CRISP-DM (Cross-Industry Standard Process for Data Mining) framework. Our aim is to leverage data-driven insights to identify key factors influencing churn, build predictive models, and develop actionable recommendations that can help Vodafone proactively retain valuable customers and enhance their overall service offerings.

# Project Structure
- [Importation](#importation)
- [EDA (Exploratory Data Analysis)](#eda-exploratory-data-analysis)
- [Data Quality Assessment](#data-quality-assessment)
- [Hypothesis Testing](#hypothesis-testing)
- [Feature Engineering](#feature-engineering)
- [Model Building](#model-building)
- [Model Evaluation](#model-evaluation)
- [Conclusion](#conclusion)

# Importation
Import necessary libraries

import pyodbc

from dotenv import dotenv_values

import numpy as np

import pandas as pd

import matplotlib.pyplot as plt

import plotly.express as px

import plotly.io as pio

import missingno as msno

import scipy.stats as stats

from sklearn.impute import SimpleImputer

from sklearn.preprocessing import LabelEncoder, StandardScaler, OneHotEncoder

from sklearn.compose import ColumnTransformer

from sklearn.model_selection import train_test_split, GridSearchCV, RandomizedSearchCV, cross_validate

from sklearn.linear_model import LogisticRegression

from sklearn.ensemble import RandomForestClassifier, GradientBoostingClassifier

from sklearn.naive_bayes import GaussianNB

from sklearn.neighbors import KNeighborsClassifier

from sklearn.tree import DecisionTreeClassifier

from sklearn.svm import SVC

from sklearn.metrics import classification_report, confusion_matrix

from imblearn.over_sampling import SMOTE

# Data Loading
In this project, I navigate through a dataset dispersed across three distinct sources, harnessing each for valuable insights.

The initial segment, spanning the first 3000 records, resides within a remote database. I access this data remotely using the pyodc library.

The second 2000 records await in OneDrive, with the name "Telco-churn-second-2000.xlsx." This file serves as our test dataset, an essential piece in evaluating our analysis.

Lastly, the GitHub repository houses the final component – "LP2_Telco-churn-last-2000.csv."

![lp2 Data Loading](https://github.com/snyamson/LP2-Customer-Churn-Machine-Learning-Prediction/assets/58486437/2f197ab3-2c38-42fc-8862-f08e7cc09c33)

# EDA (Exploratory Data Analysis)

Your EDA content goes here...

---

## Data Quality Assessment

Following data gathering from various sources, a comprehensive assessment was conducted to evaluate quality issues both visually and programmatically.

During the preliminary dataset exploration, several data quality issues were identified, and they are summarized below:


1. Accuracy:
   - Most of the categorical columns in the first DataFrame use True to represent Yes and False to represent No, creating inconsistency among the three datasets.


2. Validity:
   - In the second and third datasets, the TotalCharges column is of object data type instead of float, which should contain numerical values.


3. Consistency:
   - Inconsistent values in the categorical columns across the three data sets.

   
4. Completeness:
   - Missing data points in the Churn column (Target) and other columns in the first dataset.


---

## Hypothesis Testing

**Null Hypothesis (H0)**

The monthly subscription cost (MonthlyCharges) has no significant effect on customer churn (Churn) from the Vodafone network service.

**Alternate Hypothesis (H1)**

The monthly subscription cost (MonthlyCharges) has a significant effect on customer churn (Churn) from the Vodafone network service.


**UNIVARIATE:**

1. **Distribution of Churn:** What is the proportion of customers who have churned versus those who have not churned?

2. **Distribution of Tenure:** How is the duration of customer subscriptions (tenure) distributed among all customers?

3. **Distribution of Senior Citizen Status:** What is the distribution of senior citizen status among all customers?

**BIVARIATE:**

4. **Distribution of Monthly Charges across Churn:** How does the monthly charges vary between customers who have churned and those who have not?

5. **Relationship between Churn and Customer Tenure:** Is there a correlation between customer tenure and the likelihood of churning?

6. **Distribution of Churn across Contract Types:** How does the proportion of churn vary across different contract types (month-to-month, one year, two-year)?

7. **Impact of Online Security Service on Churn:** Does the presence or absence of online security service influence customer churn rates?

8. **Impact of Online Backup Service on Churn:** How does the presence or absence of online backup service affect customer churn rates?

**MULTIVARIATE:**

9. **Impact of Internet Service Type on Monthly Charges and Churn:** How does the type of internet service (DSL, Fiber Optic, None) influence monthly charges and customer churn? Are Fiber Optic customers paying significantly higher charges compared to DSL customers, and does this affect their likelihood of churning?



---

## Feature Engineering

Your feature engineering content goes here...

---

## Model Building

Your model building content goes here...

---

## Model Evaluation

Your model evaluation content goes here...

---

## Conclusion

Your conclusion content goes here...

## Conclusion {#conclusion}

Your conclusion content goes here...



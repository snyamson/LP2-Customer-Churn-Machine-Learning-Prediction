# Unlocking Insights: Decoding Telecommunication Customer Churn Through Machine Learning

![article head image](https://github.com/snyamson/LP2-Customer-Churn-Machine-Learning-Prediction/assets/58486437/dac2bcb3-0004-4122-8875-24a5e3e2d482)

# Introduction

In the dynamic and ever-evolving landscape of the telecommunications industry, I have encountered a critical challenge – customer churn. The ability to predict and understand customer churn can significantly impact business success, customer retention strategies, and ultimately, the bottom line. In this project, I embark on an exciting journey to explore and analyze customer churn within the Vodafone network service using the CRISP-DM (Cross-Industry Standard Process for Data Mining) framework. My aim is to leverage data-driven insights to identify key factors influencing churn, build predictive models, and develop actionable recommendations that can help Vodafone proactively retain valuable customers and enhance their overall service offerings.

# Problem Statement

In my exploration of the telecommunications industry, I've identified that customer churn poses a crucial challenge for service providers like Vodafone. The loss of customers not only impacts revenue but also signifies potential gaps in customer satisfaction and service quality. My goal is to delve into this challenge, seeking answers to pivotal questions: What are the underlying reasons behind customer churn? How can I effectively predict when a customer might churn? Through the application of data-driven methodologies and predictive modeling, I intend to provide Vodafone with the insights they need to create proactive strategies for customer retention, thereby improving their service and ensuring continued business success.

# Project Structure

# Importation

<code>
#Import necessary libraries
#Connect to server
import pyodbc
from dotenv import dotenv_values

#Data manipulation
import numpy as np
import pandas as pd

#Visualization
import matplotlib.pyplot as plt
import plotly.express as px
import seaborn as sns

#Correlation
import phik

#Visualize missing values
import missingno as msno

#Hypothesis testing
import scipy.stats as stats

#Impute
from sklearn.impute import SimpleImputer

#Machine Learning
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

#Class Imbalance
from imblearn.over_sampling import SMOTE
</code>

# Data Loading

In this project, I navigate through a dataset dispersed across three distinct sources, harnessing each for valuable insights. The initial segment, spanning the first 3000 records, resides within a remote database. I access this data remotely using the pyodc library. The second 2000 records await in OneDrive, with the name "Telco-churn-second-2000.xlsx". This file serves as our test dataset, an essential piece in evaluating our analysis. Lastly, the GitHub repository houses the final component – "LP2_Telco-churn-last-2000.csv".

# Data Understanding: Peering Into the Crystal Ball

As I delve into the heart of the CRISP-DM framework, the first step takes me on a journey of data understanding. Like a crystal ball revealing hidden truths, I meticulously explore the dataset, deciphering its structure, quirks, and nuances. This phase equips me with a profound understanding of the raw material at hand, setting the stage for meaningful analysis.

![imgonline-com-ua-twotoone-wZbJgJ3tPcOcbw](https://github.com/snyamson/LP2-Customer-Churn-Machine-Learning-Prediction/assets/58486437/45962a4e-6c59-40d0-9f6d-9d9f812c8f7d)
The dataset, sourced from different origins, consists of three different DataFrames. The first dataset, comprising 3000 entries and 21 columns, The second dataset, designed as a test dataset, features 2000 entries and 20 columns. This dataset has similar features to the first and the third but missing the target feature "Churn". The third and final dataset, also containing 2043 entries and 21 columns. Some of the features investigated are gender, SeniorCitizen, Partner, Dependents, tenure, InternetService, Contract, and PaymentMethod.

# Data Preparation: Polishing the Rough Diamond

Just as a skilled jeweler expertly cuts and polishes a rough diamond, I embark on the data preparation phase. Here, I clean, transform, and shape the data into a refined form, ready for analysis. This process is akin to sculpting, where each stroke ensures the data's quality, consistency, and accuracy.

Following data gathering from various sources, a comprehensive assessment was conducted to evaluate quality issues both visually and programmatically. Several data quality issues were identified, and they are summarized below:

Most of the categorical columns in the first DataFrame use True to represent Yes and False to represent No, creating inconsistency among the three datasets.

In the second and third datasets, the TotalCharges column is of object data type instead of float, which should contain numerical values.
Inconsistent values in the categorical columns across the three data sets.
Missing data points in the Churn column (Target) and other columns in the first dataset.

# Exploratory Data Analysis (EDA): Unveiling the Secrets

In the EDA phase, I don the hat of an explorer, navigating through the data's landscape. Like an archaeologist unraveling the mysteries of an ancient civilization, I uncover patterns, correlations, and insights hidden within the data. Visualizations become my tools, helping me translate raw numbers into compelling narratives.

I came up with a hypothesis that is to be proved by the data.

**Null Hypothesis (H0):** The monthly subscription cost (MonthlyCharges) has no significant effect on customer churn (Churn) from the Vodafone network service.

**Alternate Hypothesis (H1):** The monthly subscription cost (MonthlyCharges) has a significant effect on customer churn (Churn) from the Vodafone network service.

Questions that guided the test and the analysis are:

- How is the duration of customer subscriptions (tenure) distributed among all customers?
- Is there a correlation between customer tenure and the likelihood of churning?
- How does the proportion of churn vary across different contract types (month-to-month, one year, two-year)?
- How does the type of internet service (DSL, Fiber Optic, None) influence monthly charges and customer churn? Are Fiber Optic customers paying significantly higher charges compared to DSL customers, and does this affect their likelihood of churning?

To facilitate analysis and address the investigation's questions, numerous data quality issues were rectified. Primarily, the first and third datasets were concatenated to form a comprehensive dataset. During the data cleaning phase, a dictionary was crafted to map Boolean and None values to more meaningful categories. This mapping was applied across all three datasets to replace values appropriately. Subsequently, the first and third datasets were merged and labeled as "train," while the content of the second dataset was duplicated and named "test." This rigorous data preprocessing laid a solid foundation for further analysis and model development.

![function](https://github.com/snyamson/LP2-Customer-Churn-Machine-Learning-Prediction/assets/58486437/f1abc6d4-98bc-4e74-bb7b-908b623d8d41)

![more on cleaning](https://github.com/snyamson/LP2-Customer-Churn-Machine-Learning-Prediction/assets/58486437/80c49675-f983-4693-966e-a33be8c390de)

![imgonline-com-ua-twotoone-Q1RD7OjKCmEDHl](https://github.com/snyamson/LP2-Customer-Churn-Machine-Learning-Prediction/assets/58486437/eb3fc8b5-e615-4cf1-8ba5-b300b13975c0)

From the output above the train DataFrame contains `5043 entries` with `21 columns`, while the test DataFrame contains `2000 entries` with `20 columns`. The columns represent various customer attributes.

The data appears to have some missing values in the `TotalCharges` column, with `5035 non-null values` (8 data points) in the train DataFrame. The missing values will be handled properly during the data preprocessing stage.

# Hypothesis Testing

In this hypothesis, I'm keen on comparing the means of Monthly Charges between two independent groups: customers who have churned (Churn = "Yes") and customers who have not churned (Churn = "No"). To achieve this, I opted for the independent samples t-test since I'm comparing the mean Monthly Charges of two distinct groups – churned and non-churned customers. Importantly, the Monthly Charges for each customer are unrelated and independent of whether or not other customers have churned. By employing the t-test, I can determine if there exists a significant difference in the average Monthly Charges between these two groups. This approach sheds light on the influence of Monthly Charges on customer churn dynamics.

![hy test](https://github.com/snyamson/LP2-Customer-Churn-Machine-Learning-Prediction/assets/58486437/95f4c1b2-6618-4da9-a3cb-7e6e8d8e3f1e)

The statistical analysis revealed a calculated statistic of `14.65`, coupled with an impressively low p-value of about `1.26e-47`. With these results in hand, I am confident in rejecting the null hypothesis and firmly asserting that Monthly Charges wield a considerable influence on customer churn. The notably low p-value suggests that the observed link between Monthly Charges and churn is highly improbable to have happened by chance, thereby enhancing the strength of our findings. This practically translates to a significant and tangible connection between a customer's monthly bill and their likelihood of churning from the service.

# Investigating the questions

Delving into the questions at hand, we unveil the following insights:

# How is the duration of customer subscriptions (tenure) distributed among all customers?

![dist of tenure](https://github.com/snyamson/LP2-Customer-Churn-Machine-Learning-Prediction/assets/58486437/4444494d-e1d2-40d6-9ebb-e0f2788a0575)

Within the dataset, customer tenure spans from 0 to 72 months, averaging around 32.58 months and exhibiting a dispersion of roughly 24.53 months around the mean. Notably, customer tenures cluster within the ranges of 0 to 20 and 60 to 72 months, with 25% having tenures of 9 months or less and 75% within 56 months.

Illustrated by the histogram chart, customer tenure's distribution in the Vodafone network service ranges from 0 to 72 months, showcasing two focal points: one around 0 to 20 months, indicating new customers, and another around 60 to 72 months, highlighting long-standing loyalty. This suggests a significant portion of customers maintain relatively brief service tenure.

To glean insights into how tenure affects churn behavior, an examination of tenure alongside Churn status will unravel customer retention patterns and illuminate factors influencing churn decisions.

# Is there a correlation between customer tenure and the likelihood of churning?

![rel btn churn and tenure](https://github.com/snyamson/LP2-Customer-Churn-Machine-Learning-Prediction/assets/58486437/b4212e95-2d7b-4e9e-9834-bdc701d50e2f)

The graph depicts a notable trend: the highest number of customer churn instances with the Vodafone network service occurs within the initial months of their association with the company. This inclination can be attributed to the possibility that customers are more prone to dissatisfaction during their initial period when they are still acquainting themselves with the company and its services.

The exhibited graph showcases a distribution skewed to the right, indicating an uneven spread of customer tenure. The majority of churns transpire in the initial months, tapering towards the distribution's extremes.

To attain a precise churn rate assessment, a deeper dive into contract types will be undertaken for further analysis.

# How does the proportion of churn vary across different contract types (month-to-month, one year, two-year)?

![contract types](https://github.com/snyamson/LP2-Customer-Churn-Machine-Learning-Prediction/assets/58486437/9251a401-d77f-4a03-a188-e6aa4132b8dc)

The graph clearly indicates that customers with month-to-month contracts exhibit the highest churn rate at 43.1%, compared to the lower churn rates of 11.6% for one-year contracts and 2.4% for two-year contracts. This points to a trend where customers with shorter contract durations are more likely to churn, possibly due to dissatisfaction or more enticing alternatives. Notably, the majority of churned customers are associated with month-to-month contracts, further emphasizing this contract-based influence on customer churn.

# How does the type of internet service (DSL, Fiber Optic, None) influence monthly charges and customer churn? Are Fiber Optic customers paying significantly higher charges compared to DSL customers, and does this affect their likelihood of churning?

![int service](https://github.com/snyamson/LP2-Customer-Churn-Machine-Learning-Prediction/assets/58486437/667d5587-8340-4836-8adb-f5020a7a7fe6)

The group bar graph reveals a noteworthy contrast in monthly charges between DSL and fiber optic users, with the latter paying substantially higher fees. This divergence likely arises from the superior speed and reliability of fiber optic service. However, an intriguing trend emerges as the graph also underscores a significant disparity in churn rates between these two groups. Fiber optic customers exhibit a higher likelihood of churning, possibly due to their higher payment and subsequent elevated expectations. This underscores the intricate relationship between internet service type, monthly charges, and customer churn, emphasizing the importance of tailored service offerings based on customer preferences and needs.

# Feature Engineering: Crafting the Perfect Puzzle

Venturing into the realm of feature engineering, I metaphorically embrace the role of a puzzle architect, meticulously selecting and shaping features akin to assembling seamless puzzle pieces. Just as a puzzle takes form through thoughtful curation, I engineer attributes that harmonize with the overarching narrative. This transformative phase converts raw attributes into meaningful variables, thus amplifying the predictive prowess of upcoming models. During this phase, I adeptly managed missing value imputation via the SimpleImputer, computed correlations between the target feature (Churn) and other variables, encoded categorical attributes, executed preprocessing by employing techniques such as SMOTE to address class imbalance, and culminated the process by splitting the training dataset into train and validation sets.

# Model Building: Building Bridges to the Future

With a robust foundation in place, I transition to the model building phase, reminiscent of crafting bridges that extend into the future. Equipped with an arsenal of machine learning algorithms, I engineer and train predictive models that tap into the invaluable insights residing in the data. This phase encapsulates a symphony of precision and creativity, wherein each meticulous stride propels me closer to the realm of accurate customer churn prediction. Within this realm, I meticulously assess seven diverse models for churn prediction: Logistic Regression, Gaussian Naive Bayes, Random Forest Classifier, KNeighbors Classifier, Decision Tree Classifier, Gradient Boosting Classifier, and Support Vector Classifier (SVC). These models are subjected to rigorous performance evaluation through cross-validation to ensure the robustness of generated metrics, with accuracy serving as the pivotal yardstick for evaluation.

![imgonline-com-ua-twotoone-2olLpUySov](https://github.com/snyamson/LP2-Customer-Churn-Machine-Learning-Prediction/assets/58486437/8fa16f41-8c4b-48aa-8c7b-2a2a0f3b8a5c)

Among the evaluated models, the Random Forest Classifier emerges as the top performer with the highest accuracy of 85.48%. Given that accuracy is a pivotal metric for the project, opting for the Random Forest Classifier is a strategic decision to ensure precise customer churn predictions in upcoming test dataset scenarios. The blend of this high accuracy and the model's interpretability positions the Random Forest Classifier as an optimal solution for achieving the project's objective of identifying churn customers. My selection of the Random Forest Classifier is driven by the intention to harness its predictive prowess for informed and accurate determinations in shaping customer retention strategies.

# Model Evaluation: Separating Diamonds from the Rough

In the pivotal phase of model evaluation, I assume the role of a meticulous jeweler, adept at discerning between polished diamonds and mere imitations. Through exhaustive testing and validation, I gauge the model's efficacy, engaging in a process of relentless refinement where only the most accurate and robust contenders emerge victorious.

A comprehensive scrutiny of the Random Forest Classifier unfolds, wherein the validation set serves as the touchstone for identifying its peak performance. Central to this assessment is an in-depth analysis of the model's capabilities, meticulously dissected through the lens of the confusion matrix. This matrix yields a granular breakdown of the model's predictions, facilitating informed judgments about its efficacy.

|                                                                                                                                                          |                                                                                                                |
| -------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- |
| ![confusion matrix bef](https://github.com/snyamson/LP2-Customer-Churn-Machine-Learning-Prediction/assets/58486437/516eb7a0-246d-45da-9289-596e2a338a43) | True Positive (TP): 649 <br> True Negative (TN): 108 <br> False Negative (FN): 92 <br> True Negative (TN): 634 |

The model's performance metrics showcase impressive results: an accuracy of 85.48%, precision of 85.7% in predicting "Churn," a remarkable 87.6% recall for identifying "Churn," and an outstanding F1-score of 93%. This balance between precision and recall underscores the model's robustness. The subsequent decision to undertake hyperparameter tuning reflects our unwavering commitment to optimizing performance, aligning seamlessly with the business objectives. This strategic move aims to further enhance accuracy and deliver precise predictions on the upcoming test dataset, bolstering my approach to effective customer churn management.

# Model Improvement

In this stage, I undertake hyperparameter tuning using RandomizedSearchCV on a Random Forest Classifier model. This process involves exploring a predefined parameter grid and utilizing the Accuracy-score as the evaluation metric.

![hyperparameter](https://github.com/snyamson/LP2-Customer-Churn-Machine-Learning-Prediction/assets/58486437/76ad36fe-3402-4f76-9bdc-cbaa1f146b88)

Following hyperparameter tuning, the Random Forest Classifier was optimized. This refined model showcases an impressive accuracy of around 87.45%, an enhancement from the initial 85.48%, underlining its robustness.

This substantial improvement highlights the potency of hyperparameter tuning in elevating model performance for accurate customer churn prediction.

|                                                                                                                                                         |                                                                                                               |
| ------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- |
| ![confusion matrix af](https://github.com/snyamson/LP2-Customer-Churn-Machine-Learning-Prediction/assets/58486437/c56387b7-2438-4f27-bab0-afe1f3e527ac) | True Positive (TP): 651 <br> True Negative (TN): 96 <br> False Negative (FN): 90 <br> True Negative (TN): 646 |

With the completion of hyperparameter tuning, the slight adjustments in the confusion matrix exemplify the model's refined predictive prowess, reflecting heightened accuracy in accurately categorizing instances of customer churn and non-churn.

# Future Predictions

Upon fine-tuning the model's hyperparameters, it was employed to predict Churn classes within the test dataset.

![churn pred](https://github.com/snyamson/LP2-Customer-Churn-Machine-Learning-Prediction/assets/58486437/5a192eb0-b3ea-4198-bcb8-b7703bc00bbe)

The prediction outcomes revealed 1472 instances correctly classified as Not Churn, and 528 instances accurately labeled as Churn. This signifies the model's ability to effectively distinguish Churn and Not Churn customers within the test set.

As the model's accuracy undergoes continuous refinement, its performance is anticipated to consistently improve, yielding even more precise predictions over time.

# Conclusion: Insights Unveiled

As I conclude this journey, armed with insights garnered from data exploration, model building, and methodological prowess, I am ready to unveil a collection of actionable recommendations for for telecommunications like Vodafone. Just as an artist reveals a masterpiece, I offer Vodafone a fresh perspective on their customer retention strategies, enriched by the layers of this data-driven expedition.

The distilled recommendations are as follows:

**1. Tailor Pricing Strategies:** The analysis underscores a correlation between higher monthly charges and increased customer churn. To enhance retention, Vodafone could explore balanced pricing strategies, aligning revenue generation with customer satisfaction and perceived value.

**2. Enhance Early Customer Experience:** Elevated churn rates during initial months highlight the significance of early customer experience. Prioritizing onboarding processes, service quality, and prompt issue resolution can heighten satisfaction and loyalty during this pivotal phase.

**3. Promote Long-Term Contracts:** Higher churn rates among month-to-month contract customers warrant attention. Encouraging longer-term contracts through incentives and benefits could foster commitment and reduce churn.

**4. Leverage Additional Services:** Services like Online Security and Backup influence churn rates. Amplifying these offerings to address customer needs can aid in retention by providing value-added solutions.

**5. Monitor Fiber Optic Offering:** Close scrutiny of Fiber Optic service is imperative due to its high charges and churn rate. Continuous refinement and support will align premium costs with customer expectations.

**6. Personalized Customer Engagement:** Employ insights from churn analysis for personalized engagement strategies. Customized communication, offers, and targeted marketing based on tenure, contract type, and preferences can bolster loyalty and mitigate churn.

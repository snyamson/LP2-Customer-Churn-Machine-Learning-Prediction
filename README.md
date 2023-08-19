# 💼 Customer Churn Classification Prediction Project
<<<<<<< HEAD

=======
>>>>>>> 4424420fea2b2ea8b19809369883f5c5ab801226
![customer-churn-image](https://github.com/snyamson/LP2-Customer-Churn-Machine-Learning-Prediction/assets/58486437/5b18de22-53a4-4cee-a858-129b75ceb137)
In the dynamic and ever-evolving landscape of the telecommunications industry, customer churn has become a critical challenge for service providers. The ability to predict and understand customer churn can significantly impact business success, customer retention strategies and increase customer service satisfaction.

## Project Overview

This project follows the CRISP-DM (Cross-Industry Standard Process for Data Mining) framework to explore and analyze customer churn within the Vodafone network service. The aim is to leverage data-driven insights to identify key factors influencing churn, build predictive models, and develop actionable recommendations that can help Vodafone proactively retain valuable customers and enhance their overall service offerings.

## 📑 Table of Contents
<<<<<<< HEAD

- [Project Overview](#project-overview)
- [Project Structure](#project-structure)
- [Data Dictionary](#data-dictionary)
- [Project Highlights](#project-highlights)
- [Summary](#summary)
- [Hypothesis Investigated](#hypothesis-investigated)
  - [Results](#results)
- [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
- [Model Selection](#model-selection)
- [Model Evaluation (Confusion Matrix)](#model-evaluation-confusion-matrix)
- [Classification Metrics Score](#classification-metrics-score)
- [Recommendations](#recommendations)
- [Getting Started](#getting-started)
- [License](#license)
- [Author](#author)

## Project Structure📂

- `code/`: Contains the dataset used for analysis and the Jupyter notebook detailing the data exploration, preprocessing, and model building steps.
- `article/`: Holds project-related article.
- `customer churn analysis dashboard.pbix`: The file for the deployed Power BI dashboard.
- `LICENSE`: Project license.
- `README.md`: Project overview, links, highlights, and information.

## Data Dictionary

| Field            | Description                                                                                                      |
| ---------------- | ---------------------------------------------------------------------------------------------------------------- |
| Gender           | Whether the customer is a male or a female                                                                       |
| SeniorCitizen    | Whether a customer is a senior citizen or not                                                                    |
| Partner          | Whether the customer has a partner or not (Yes, No)                                                              |
| Dependents       | Whether the customer has dependents or not (Yes, No)                                                             |
| Tenure           | Number of months the customer has stayed with the company                                                        |
| Phone Service    | Whether the customer has a phone service or not (Yes, No)                                                        |
| MultipleLines    | Whether the customer has multiple lines or not                                                                   |
| InternetService  | Customer's internet service provider (DSL, Fiber Optic, No)                                                      |
| OnlineSecurity   | Whether the customer has online security or not (Yes, No, No Internet)                                           |
| OnlineBackup     | Whether the customer has online backup or not (Yes, No, No Internet)                                             |
| DeviceProtection | Whether the customer has device protection or not (Yes, No, No internet service)                                 |
| TechSupport      | Whether the customer has tech support or not (Yes, No, No internet)                                              |
| StreamingTV      | Whether the customer has streaming TV or not (Yes, No, No internet service)                                      |
| StreamingMovies  | Whether the customer has streaming movies or not (Yes, No, No Internet service)                                  |
| Contract         | The contract term of the customer (Month-to-Month, One year, Two year)                                           |
| PaperlessBilling | Whether the customer has paperless billing or not (Yes, No)                                                      |
| Payment Method   | The customer's payment method (Electronic check, mailed check, Bank transfer(automatic), Credit card(automatic)) |
| MonthlyCharges   | The amount charged to the customer monthly                                                                       |
| TotalCharges     | The total amount charged to the customer                                                                         |
| Churn            | Whether the customer churned or not (Yes or No)                                                                  |

# Project Highlights🚀
=======
- [Project Overview](#project-overview)
- [Project Structure](#project-structure)
- [Data Dictionary](#data-dictionary)
- [Project Highlights](#project-highlights)
- [Summary](#summary)
- [Hypothesis Investigated](#hypothesis-investigated)
  - [Results](#results)
- [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
- [Model Selection](#model-selection)
- [Model Evaluation (Confusion Matrix)](#model-evaluation-confusion-matrix)
- [Classification Metrics Score](#classification-metrics-score)
- [Recommendations](#recommendations)
- [Getting Started](#getting-started)
- [License](#license)
- [Author](#author)

## Project Structure📂

- `code/`: Contains the dataset used for analysis and the Jupyter notebook detailing the data exploration, preprocessing, and model building steps.
- `article/`: Holds project-related article.
- `customer churn analysis dashboard.pbix`: The file for the deployed Power BI dashboard.
- `LICENSE`: Project license.
- `README.md`: Project overview, links, highlights, and information.

## Data Dictionary
  | Field           | Description                                                          |
|-----------------|----------------------------------------------------------------------|
| Gender          | Whether the customer is a male or a female                          |
| SeniorCitizen   | Whether a customer is a senior citizen or not                       |
| Partner         | Whether the customer has a partner or not (Yes, No)                 |
| Dependents      | Whether the customer has dependents or not (Yes, No)                |
| Tenure          | Number of months the customer has stayed with the company           |
| Phone Service   | Whether the customer has a phone service or not (Yes, No)           |
| MultipleLines   | Whether the customer has multiple lines or not                      |
| InternetService | Customer's internet service provider (DSL, Fiber Optic, No)        |
| OnlineSecurity  | Whether the customer has online security or not (Yes, No, No Internet) |
| OnlineBackup    | Whether the customer has online backup or not (Yes, No, No Internet) |
| DeviceProtection| Whether the customer has device protection or not (Yes, No, No internet service) |
| TechSupport     | Whether the customer has tech support or not (Yes, No, No internet) |
| StreamingTV     | Whether the customer has streaming TV or not (Yes, No, No internet service) |
| StreamingMovies | Whether the customer has streaming movies or not (Yes, No, No Internet service) |
| Contract        | The contract term of the customer (Month-to-Month, One year, Two year) |
| PaperlessBilling| Whether the customer has paperless billing or not (Yes, No)        |
| Payment Method  | The customer's payment method (Electronic check, mailed check, Bank transfer(automatic), Credit card(automatic)) |
| MonthlyCharges  | The amount charged to the customer monthly                         |
| TotalCharges    | The total amount charged to the customer                            |
| Churn           | Whether the customer churned or not (Yes or No)                     |


#  Project Highlights🚀
>>>>>>> 4424420fea2b2ea8b19809369883f5c5ab801226

- Utilized the CRISP-DM framework to thoroughly analyze customer churn in the Vodafone network service.
- Conducted exploratory data analysis to uncover insights and patterns within the dataset.
- Built predictive models using machine learning algorithms like Random Forest Classifier.
- Implemented hyperparameter tuning to optimize model performance.
- Developed a Power BI dashboard for interactive visualization of key findings.
- Published an insightful article detailing the project and its results.

## Summary

<<<<<<< HEAD
| Code | Name                                     |             Published Article             |                                                                                                                                                          Deployed App |
| ---- | ---------------------------------------- | :---------------------------------------: | --------------------------------------------------------------------------------------------------------------------------------------------------------------------: |
| LP 2 | Customer Churn Classification Prediction | [Read Article](https://your-article-link) | [View Dashboard](https://app.powerbi.com/view?r=eyJrIjoiOWE0MGNhMDgtMDdmYS00ZTVmLWJjY2MtNGRjNzVkZDlhMmM2IiwidCI6IjQ0ODdiNTJmLWYxMTgtNDgzMC1iNDlkLTNjMjk4Y2I3MTA3NSJ9) |

## Hypothesis Investigated

=======
| Code      | Name        | Published Article |  Deployed App |
|-----------|-------------|:-------------:|------:|
| LP 2      | Customer Churn Classification Prediction |  [Read Article](https://your-article-link) | [View Dashboard](https://app.powerbi.com/view?r=eyJrIjoiOWE0MGNhMDgtMDdmYS00ZTVmLWJjY2MtNGRjNzVkZDlhMmM2IiwidCI6IjQ0ODdiNTJmLWYxMTgtNDgzMC1iNDlkLTNjMjk4Y2I3MTA3NSJ9) |

## Hypothesis Investigated
>>>>>>> 4424420fea2b2ea8b19809369883f5c5ab801226
**Null Hypothesis (H0)** :The monthly subscription cost (MonthlyCharges) has no significant effect on customer churn (Churn) from the Vodafone network service.

**Alternate Hypothesis (H1)** : The monthly subscription cost (MonthlyCharges) has a significant effect on customer churn (Churn) from the Vodafone network service.

### Results
<<<<<<< HEAD

| Test Conducted               | T-Statistic        | P-Value                |
| ---------------------------- | ------------------ | ---------------------- |
| Independent Samples T - Test | 14.650610568422312 | 1.2575465113545793e-47 |

The statistical analysis yielded a calculated statistic of `14.65`, accompanied by a remarkably low p-value of approximately `1.26e-47`. With this statistical outcome, we confidently reject the null hypothesis and conclude that Monthly Charges exert a substantial influence on customer churn. The p-value indicates that the observed relationship between Monthly Charges and churn is highly unlikely to occur by chance, reinforcing the robustness of our findings.
=======
|Test Conducted | T-Statistic | P-Value |
| --------------| --------------- | ---------| 
| Independent Samples T - Test | 14.650610568422312 | 1.2575465113545793e-47 | 

The statistical analysis yielded a calculated statistic of `14.65`, accompanied by a remarkably low p-value of approximately `1.26e-47`.  With this statistical outcome, we confidently reject the null hypothesis and conclude that Monthly Charges exert a substantial influence on customer churn. The p-value indicates that the observed relationship between Monthly Charges and churn is highly unlikely to occur by chance, reinforcing the robustness of our findings. 
>>>>>>> 4424420fea2b2ea8b19809369883f5c5ab801226

## Exploratory Data Analysis (EDA)📊

A snapshot of the conducted exploratory data analysis, aimed at addressing pivotal business inquiries during the analysis process.

<<<<<<< HEAD
| ![churn and contract](https://github.com/snyamson/LP2-Customer-Churn-Machine-Learning-Prediction/assets/58486437/7884caa5-e04e-4b72-95b3-c2d54b93bcc4)         | ![churn and security](https://github.com/snyamson/LP2-Customer-Churn-Machine-Learning-Prediction/assets/58486437/b5c8f74a-c978-47bb-9dee-21a90a6c029b)       |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| ![monthly charges with churn](https://github.com/snyamson/LP2-Customer-Churn-Machine-Learning-Prediction/assets/58486437/47e35bf3-7170-4091-b114-1c069ed3bd5a) | ![rel btn churn and tenure](https://github.com/snyamson/LP2-Customer-Churn-Machine-Learning-Prediction/assets/58486437/d4aae51b-e3e6-43be-a5e3-92076136beec) |

=======
| ![churn and contract](https://github.com/snyamson/LP2-Customer-Churn-Machine-Learning-Prediction/assets/58486437/7884caa5-e04e-4b72-95b3-c2d54b93bcc4) | ![churn and security](https://github.com/snyamson/LP2-Customer-Churn-Machine-Learning-Prediction/assets/58486437/b5c8f74a-c978-47bb-9dee-21a90a6c029b) |
|-----------------------|-----------------------|
| ![monthly charges with churn](https://github.com/snyamson/LP2-Customer-Churn-Machine-Learning-Prediction/assets/58486437/47e35bf3-7170-4091-b114-1c069ed3bd5a) | ![rel btn churn and tenure](https://github.com/snyamson/LP2-Customer-Churn-Machine-Learning-Prediction/assets/58486437/d4aae51b-e3e6-43be-a5e3-92076136beec) |


>>>>>>> 4424420fea2b2ea8b19809369883f5c5ab801226
## Model Selection

![model per](https://github.com/snyamson/LP2-Customer-Churn-Machine-Learning-Prediction/assets/58486437/f5522617-3f6f-4239-9a39-694cc6aac32d)
The `Random Forest Classifier` stands out as the best-performing model due to its highest accuracy among the evaluated models `(85.48%)`. As accuracy is a key performance metric for our project, selecting the Random Forest Classifier ensures that we prioritize correctly predicting customer churn in our future predictions on the test dataset.

## Model Evaluation (Confusion Matrix)📉

<<<<<<< HEAD
| Before Hyperparameter Tunning                                                                                                                            | After Hyperparameter Tunning                                                                                                                            |
| -------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------- |
| ![confusion matrix bef](https://github.com/snyamson/LP2-Customer-Churn-Machine-Learning-Prediction/assets/58486437/ee7c2c25-02bc-4374-b4b4-632a832bd68e) | ![confusion matrix af](https://github.com/snyamson/LP2-Customer-Churn-Machine-Learning-Prediction/assets/58486437/4f16a6fb-990f-4c41-8ecf-6e15668dc3bf) |

## Classification Metrics Score

| Metric    | Score  |
| --------- | ------ |
| Accuracy  | 87.39% |
| Precision | 86.8%  |
| Recall    | 87.8%  |
| F1        | 93.5%  |
=======
| Before Hyperparameter Tunning                                                                                                                                     | After Hyperparameter Tunning                                                                    |
| ---------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------ |
| ![confusion matrix bef](https://github.com/snyamson/LP2-Customer-Churn-Machine-Learning-Prediction/assets/58486437/ee7c2c25-02bc-4374-b4b4-632a832bd68e) | ![confusion matrix af](https://github.com/snyamson/LP2-Customer-Churn-Machine-Learning-Prediction/assets/58486437/4f16a6fb-990f-4c41-8ecf-6e15668dc3bf) |

## Classification Metrics Score
| Metric   | Score |
| -------- | -------|
| Accuracy | 87.39% |
| Precision | 86.8% |
| Recall | 87.8% |
| F1 | 93.5% |
>>>>>>> 4424420fea2b2ea8b19809369883f5c5ab801226

## Recommendations

1. **Tailor Pricing Strategies:** The analysis reveals that higher monthly charges are associated with an increased likelihood of customer churn. To enhance customer retention, Vodafone can explore competitive pricing strategies that balance revenue generation with customer satisfaction, ensuring that the cost aligns with the value perceived by customers.

2. **Enhance Early Customer Experience:** Early months of customer tenure exhibit a higher churn rate, suggesting that customer experience in the initial stages is vital. Focusing on improving onboarding processes, service quality, and addressing customer concerns during this crucial period can enhance customer satisfaction and loyalty.

3. **Promote Long-Term Contracts:** The analysis indicates that customers with month-to-month contracts have a significantly higher churn rate compared to those with one-year or two-year contracts. Encouraging customers to opt for longer-term contracts through incentives and benefits can potentially reduce churn rates and foster customer commitment.

4. **Leverage Additional Services:** The presence of Online Security and Online Backup services has shown to impact churn rates. Strategically promoting and enhancing these services can play a role in reducing churn rates by providing value-added features that address customer needs and concerns.

5. **Monitor and Adjust Fiber Optic Offering:** Given the higher monthly charges and elevated churn rate among Fiber Optic customers, closely monitor customer satisfaction and service quality for this group. Continuously fine-tune offerings and support to ensure that the premium cost of Fiber Optic service aligns with customer expectations.

6. **Personalized Customer Engagement:** Utilize customer insights from the churn analysis to develop personalized engagement strategies. Tailored communication, offers, and targeted marketing campaigns based on customer tenure, contract type, and service preferences can enhance customer loyalty and mitigate churn.

<<<<<<< HEAD
## Getting Started🏁
=======
##  Getting Started🏁
>>>>>>> 4424420fea2b2ea8b19809369883f5c5ab801226

1. Clone this repository: `git clone https://github.com/snyamson/LP2-Customer-Churn-Machine-Learning-Prediction.git`
2. Navigate to the project directory: `LP2-Customer-Churn-Machine-Learning-Prediction`
3. Explore the Jupyter notebooks for detailed steps and code execution.
4. Check out the Power BI dashboard for interactive visualizations.
5. Read the published article for a comprehensive understanding of the project.

<<<<<<< HEAD
## License📜

This project is licensed under the [MIT License](LICENSE).

## Author✍️
=======
##  License📜

This project is licensed under the [MIT License](LICENSE).

##  Author✍️
>>>>>>> 4424420fea2b2ea8b19809369883f5c5ab801226

Solomon Nyamson

Connect with me on LinkedIn: [LinkedIn Profile](https://www.linkedin.com/in/solomon-nyamson/)

---

Feel free to star ⭐ this repository if you find it helpful!

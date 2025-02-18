Lead Scoring Model for X Education
-------------

Objective
The primary objective of this project is to improve the lead conversion rate for X Education, an online education company, from the current 30% to 80% by building a logistic regression model. 
The model assigns a score between 0 to 100 to incoming leads, helping the sales and marketing teams prioritize high-potential leads and improve overall conversions. 
This project aims to provide a scalable and adaptable solution to meet the company's future needs.

Data Overview
The dataset contains lead information collected through various sources such as API submissions, landing pages, and organic traffic.
Key attributes include user demographics, source of traffic, lead activity, and preferences.


--------------
Data Size:

Train set: 6314 records (70%)
Test set: 2706 records (30%)
The dataset has a mild imbalance with a 5:8 ratio of converted to non-converted leads.


--------------
Data Cleaning and Preprocessing:

Handling Missing Values:

Categorical columns: Replaced missing values with the mode or grouped categories (e.g., renaming).
Numerical columns: Imputed missing values using median or mean.
Outlier Treatment: Capped values at the 99th percentile to remove outliers caused by bots or spam.
Standardization: Scaled numerical variables using StandardScaler to optimize the logistic regression performance.

Feature Selection:
Dropped irrelevant or redundant columns (e.g., "Tags", "Last Activity").
Used Recursive Feature Elimination (RFE) to select the top 15 predictive variables from the dataset.

Exploratory Data Analysis (EDA):

Found that leads originated primarily from APIs and landing pages, with most traffic coming from Google, direct traffic, and organic search.
Observed that unemployed leads and those seeking better career prospects constituted a significant portion of converted leads.
Identified areas for improvement, such as the value of the free e-book and the performance of Olark chat conversions.

Model Building:

Initially, 34 variables were used to train the logistic regression model using the statsmodels library.
Iteratively removed insignificant variables, reducing the feature set to 9 significant predictors with low collinearity (VIF < 5).
Optimized the model's performance by tuning the threshold for recall and precision. A cut-off of 0.28 was found to deliver the best recall while maintaining high accuracy.

Lead Scoring:

Developed a formula to assign a lead score between 0 to 100 based on the model's predictions, enabling prioritization of high-potential leads.


-----------------
Final Suggestions

Optimize Sales Focus: The sales team should concentrate on high-priority leads (score > 75) to maximize resource efficiency and improve conversion rates.

Enhance Marketing Campaigns: Redirect investments toward high-performing channels like Google Ads and organic search, and revamp the free e-book to provide more value to potential leads.

Improve Chat Experience: Train representatives to better engage users via Olark chat or use AI chatbots to improve real-time support and increase conversion rates.


------------------
Results
The final model explains 83% of the variance in the data.

It achieves optimal recall (75%) and precision(71%) with minimal false positives, ensuring better resource allocation and higher conversion potential.

By focusing on high-priority leads and refining user engagement strategies, the company can effectively achieve its target of an 80% conversion rate.

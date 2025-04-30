Lead Scoring Model for X Education
-------------------

Objective:
The goal of this project was to help X Education, an online learning platform, improve its lead conversion rate from 30% to 80%. To achieve this, I built a logistic regression model that assigns a score (0–100) to each incoming lead. This score helps the sales and marketing teams focus their efforts on the most promising leads, ultimately improving conversions and efficiency.

-------------------
About the Data:
The dataset includes lead information from various sources such as API submissions, landing pages, and organic web traffic. It contains user demographics, behavior, source of traffic, and preferences.

Train Set: 6314 records (70%)
Test Set: 2706 records (30%)
Lead Conversion Ratio: Mildly imbalanced at 5:8 (converted vs. non-converted)

-------------------
Data Cleaning & Preprocessing:

Missing Values:

- Categorical data: Filled using mode or grouped similar values.
- Numerical data: Imputed with mean or median.
- Outliers: Capped extreme values at the 99th percentile to reduce noise from spam/bot traffic.
- Scaling: Applied StandardScaler to standardise numerical variables.

Feature Selection:

- Dropped irrelevant features like "Tags" and "Last Activity".
- Used Recursive Feature Elimination (RFE) to select the 15 most relevant variables, then narrowed down to 9 strong predictors with low multicollinearity (VIF < 5).

Exploratory Data Analysis (EDA):

- Most leads came from landing pages and APIs, with high traffic from Google, direct visits, and organic search.
- Unemployed individuals and those seeking career growth were more likely to convert.
- Identified opportunities to improve areas like free resources (e.g., e-books) and Olark chat performance.

-------------------
Model Building:

- Started with 34 features, then reduced to 9 significant ones based on statistical relevance and multicollinearity checks.
- Used the statsmodels library to build and refine the logistic regression model.
- Tuned the classification threshold to optimize performance. A cutoff of 0.28 provided the best balance of recall (75%) and precision (71%).
  
-------------------
Lead Scoring System:
- Converted the model’s output into a score from 0 to 100 for each lead. This helps the sales team prioritise follow-ups more effectively.

-------------------
Key Recommendations:

- Sales Efficiency: Focus on leads scoring above 75 for higher conversion potential.
- Marketing Strategy: Invest more in effective channels like Google Ads and organic search. Improve the perceived value of free resources.
- Customer Engagement: Train chat representatives or integrate AI chatbots to improve user interaction and support.

-------------------
Results:

- The model explains 83% of the variance in lead conversions.
- Achieves 75% recall and 71% precision, minimizing false positives.
- The lead scoring approach provides a scalable way to optimize sales and marketing efforts, helping the company move toward its 80% conversion goal.

🎯 Lead Scoring Model for X Education

✅ Objective:
The goal was to help X Education, an online learning platform, increase its lead conversion rate from 30% to 80%. I built a logistic regression model that assigns each lead a score from 0 to 100, enabling the sales and marketing teams to prioritize high-potential leads and boost conversion efficiency.

📊 About the Data:
The dataset includes lead information from API submissions, landing pages, and organic traffic—covering demographics, behavior, and source details.

- 🧪 Train Set: 6314 records (70%)
- 🧪 Test Set: 2706 records (30%)
- ⚖️ Conversion Ratio: Mildly imbalanced at 5:8 (converted vs. non-converted)

🛠️ Data Cleaning & Preprocessing:
- Categorical features: Filled missing values using mode or by grouping similar categories
- Numerical features: Imputed using mean/median
- Outliers: Capped extreme values at the 99th percentile to reduce noise
- Scaling: Applied StandardScaler to normalize numeric columns

🔍 Feature Selection:
- Removed irrelevant fields like "Tags" and "Last Activity"
- Used Recursive Feature Elimination (RFE) to pick the top 15 variables
- Final model retained 9 key predictors with low multicollinearity (VIF < 5)

📈 Exploratory Data Analysis (EDA):
- The majority of leads came via landing pages and APIs
- Top traffic sources: Google, direct traffic, and organic search
- Higher conversion seen among unemployed leads and those seeking career advancement
- 🚧 Improvement areas identified: free e-books and Olark chat performance

🧠 Model Building:
- Started with 34 variables, narrowed down to 9 significant predictors
- Built using the statsmodels library
- Optimized threshold to 0.28 for best trade-off between recall and precision

- 🔁 Recall: 75%
- 🎯 Precision: 71%

📉 Lead Scoring System:
- Converted model outputs into a 0–100 score for each lead.
- 🔝 This allows the sales team to focus efforts on high-scoring leads for better outcomes.

💡 Key Recommendations:
Sales Focus: Prioritize leads scoring above 75 for maximum ROI

Marketing Strategy:
- Shift investments to better-performing channels like Google Ads and organic search
- Improve the value of free resources, like downloadable e-books

User Engagement:
- Train chat agents or deploy AI chatbots to enhance real-time conversations

✅ Results:
- Model explains 83% of the variance in lead conversions
- Achieves 75% recall and 71% precision, reducing false positives
- The lead scoring model is a scalable and strategic tool to help the company reach its 80% conversion goal

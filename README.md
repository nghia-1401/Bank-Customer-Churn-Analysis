# Churn analysis and customer retention strategies in banking industry
## 1. Project Overview
This project involves an in-depth analysis of a bank's customer dataset to identify the key factors influencing customer churn. Based on these insights, a Machine Learning model is developed to predict the future probability of a customer leaving. Finally, the project proposes specific and actionable business strategies aimed at improving customer retention rates.
## 2. Business Context: NeoBank Europe
NeoBank Europe is a digital bank headquartered in Luxembourg with the ambition of conquering the European market. For its launch strategy, NeoBank focused on three of the Eurozone's largest and most dynamic economies: France, Spain, and Germany. They launched a unified marketing campaign across all three nations, expecting an easily scalable business model.
However, after two years of operation, while the total number of users is still growing, a recent business report revealed a worrying trend that breaks management's initial expectations: the operational efficiency across the three core markets is decreasing, specifically, the customer churn rate is quite high, significantly impacting overall profitability.
## 3. Data Source
https://www.kaggle.com/datasets/radheshyamkollipara/bank-customer-churn/data  
The dataset used in this project is Bank Customer Churn Prediction, sourced from Kaggle.   
The data includes 10,000 customer records with demographic and financial information, such as:  
- CreditScore: Customer's credit score.
- Geography: Country (France, Spain, Germany).
- Gender: Gender.
- Age: Age.
- Tenure: Length of time as a bank customer (in years).
- Balance: Account balance.
- NumOfProducts: Number of bank products used.
- HasCrCard: Whether the customer has a credit card.
- IsActiveMember: Whether the customer is an active member.
- EstimatedSalary: Estimated salary.
- Complain: Whether the customer has complained.
- Satisfaction Score: Customer satisfaction score (after complaint resolution).
- Card Type: Type of credit card owned (e.g., Gold, Silver, Platinum).
- Exited: Target Variable - Whether the customer has churned (1) or not (0).
## 4. Tools and Libraries
- Programming Language: Python
- Environment: Google Colab
- Data Analysis & Processing Libraries:
  + Pandas: Reading, writing, and manipulating tabular data.
  + NumPy: Support for mathematical computations and array handling.
- Visualization Libraries:
  + Matplotlib: Creating basic, static plots.
  + Seaborn: Creating more aesthetic and complex statistical visualizations.
- Machine Learning Library:
  + Scikit-learn: Building, training, and evaluating machine learning models.
## 5. Execution Workflow
Step 1. Exploratory Data Analysis (EDA): Checking data structure, information, and descriptive statistics.  
Step 2. Data Cleaning & Preprocessing: Handling missing values (if any), normalization, and data encoding.    
Step 3. Deep Dive Visualization & Analysis: Using charts to uncover relationships and the main factors influencing the churn rate.    
Step 4. Model Building: Training a Logistic Regression model to predict customer churn probability.     
Step 5. Model Evaluation: Measuring model performance using metrics like Accuracy, Precision, Recall, F1-score, and the Confusion Matrix. Step 6. Conclusion & Recommendations: Summarizing key insights and proposing specific business strategies. 
## 6. Key Analytical Findings
- Overall Churn Rate: Approximately 20.4% of customers in the dataset have churned, which is a significant figure.
- Key Predictors: Complaint (Complain) is the most important factor in predicting churn. Additionally, Age and Active Status (IsActiveMember) are also critical factors.
- Demographics:
  + Geography: Customers in Germany have a significantly higher churn rate (32.4%).
  + Gender: The female churn rate (25.1%) is noticeably higher than the male rate (16.5%).
  + Age: The middle-aged group (41-60 years old) has the highest churn rate.
- Behavior & Products:
  + Inactive Members: Inactive customers (IsActiveMember = 0) have a much higher churn rate.
  + Number of Products: Customers using 3 or 4 products have an almost absolute churn rate. This is an unusual finding that requires deeper investigation.
  + Balance: Customers who left typically had a higher average account balance.
## 7. Predictive Model Results   
A Logistic Regression model was built to predict the probability of churn.   
- Accuracy: The model achieved an accuracy of ~99.85% on the test set.
- Precision, Recall, F1-Score: These metrics all reached very high, near-absolute values (1.00).   
## 8. Strategic Recommendations   
1. Focus on High-Risk Groups   
- Customers in Germany: Deploy special care campaigns and satisfaction surveys to understand the root causes.  
- Age Group 41-60: Introduce financial products suitable for this life stage (retirement, investment) and organize financial management workshops.  
2. Improve Experience and Engagement   
- Inactive Customers: Run "re-engagement" campaigns with personalized offers.  
- High-Product Users: Urgently investigate the reason for the near-100% churn rate in the group using 3-4 products. Temporarily halt cross-selling of the 3rd and 4th product until the cause is determined.  
3. Build an Early Warning System   
- Apply the developed predictive model to score the churn risk for the entire customer base monthly.  
- Create a list of the highest-risk customers for the customer service team to proactively contact and intervene before they decide to leave.   
4. Prioritize Based on Customer Lifetime Value (CLTV)  
- Among high-risk customers, prioritize resources to retain those with the highest CLTV (e.g., large balances, long tenure).  

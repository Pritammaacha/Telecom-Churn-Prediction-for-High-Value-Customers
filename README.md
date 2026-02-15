Telecom Churn Prediction for High-Value Customers
Project Overview
In the competitive telecommunications industry, the cost of acquiring a new customer is 5 to 10 times higher than retaining an existing one. This project focuses on predicting churn for high-value customers—the top 20% of users who generate approximately 80% of total revenue—within the Indian and Southeast Asian markets.

Business Objective
Predict Churn: Identify high-risk customers likely to leave in the upcoming month.

Identify Indicators: Determine specific behavioral patterns, such as declining usage or shifting recharge habits, that precede churn.

Strategic Recommendations: Provide actionable insights to help the business intervene during the "Action Phase" to improve retention.

Technical Workflow
1. Data Definition and Preparation
The Four-Month Window:

Months 6 and 7 (Good Phase): Established baseline customer behavior.

Month 8 (Action Phase): The critical period where customer experience may decline and behavior shifts.

Month 9 (Churn Phase): Used to tag churners based on usage metrics.

High-Value Filtering: The analysis is restricted to customers who recharged an amount greater than or equal to the 70th percentile of the average recharge amount in the Good Phase.

Churn Tagging: Customers with zero incoming or outgoing calls and zero mobile data usage in Month 9 are classified as Churn = 1.

2. Modeling Approach
To address high dimensionality and significant class imbalance (churn rates are typically 5-10%), the following strategy was implemented:

Dimensionality Reduction: Utilized Principal Component Analysis (PCA) to manage the extensive feature set and reduce multicollinearity.

Handling Class Imbalance: Applied techniques such as SMOTE or adjusted class weights to ensure the model accurately identifies the minority churn class.

Model Selection:

Predictive Power: Employed advanced classifiers like Random Forest or XGBoost, optimized specifically for high Sensitivity (Recall) to catch as many potential churners as possible.

Interpretability: Used Logistic Regression to identify key drivers of churn, such as drops in local outgoing minutes of usage.

Key Results and Recommendations
Primary Drivers: A significant decrease in usage (MOU) and recharge frequency in Month 8 were identified as the strongest predictors of impending churn.

Business Strategy: Recommended proactive retention offers, such as targeted discounts or loyalty bonuses, specifically triggered when a high-value customer's usage drops below a statistically significant threshold.


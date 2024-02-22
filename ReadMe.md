## Case Study: Customer Attrition in Bank Credit Card Services.

Data Source: https://www.kaggle.com/datasets/sakshigoyal7/credit-card-customers

### Exploratory Data Analysis

This report presents an analysis of customer attrition within a dataset comprising 10,127 customer records from a credit card company. The dataset includes demographic data, credit card usage information, and a binary indicator for customer attrition. The overall attrition rate across all customers in this dataset is 16.06%. This analysis seeks to identify factors contributing to customer attrition by examining distribution and attrition rates across various categorical dimensions including Gender, Education Level, Marital Status, Income Category, and Card Category.

#### Analysis by Gender
- Female Customers: Represent 53% of the total customer base, with an attrition rate of 17.36%, which is higher than the overall average attrition rate of 16.06%.
- Male Customers: Account for 47% of the total customer base, with an attrition rate of 14.62%, which is lower than the overall average.

#### Analysis by Education Level
- Doctorate: Shows the highest attrition rate at 21.06%, significantly above the overall average.
- Post-Graduate: Follows with an attrition rate of 17.83%.
- Uneducated, Graduate, and High School: Present attrition rates close to the overall average, with Graduate at 15.57%, High School at 15.20%, and Uneducated at 15.94%.
- College: Has a slightly lower attrition rate of 15.20%.
- Unknown: Education level shows an attrition rate of 16.85%, slightly above the overall average.

#### Analysis by Marital Status
- Unknown: Marital status exhibits the highest attrition rate at 17.22%.
- Single: Customers have an attrition rate of 16.94%, which is above the overall average.
- Divorced: Customers show an attrition rate close to the overall average at 16.18%.
- Married: Customers have the lowest attrition rate of 15.13%, below the overall average.

#### Analysis by Income Category
- Less than $40K: Holds the highest attrition rate of 17.19%, slightly above the overall average.
- $120K+: Also shows a higher attrition rate of 17.33%.
- Unknown: Income category has an attrition rate of 16.82%, which is slightly above the overall average.
- $80K - $120K: Presents an attrition rate of 15.77%.
- $40K - $60K: Shows a lower attrition rate of 15.14%.
- $60K - $80K: Exhibits the lowest attrition rate among all categories at 13.48%.

#### Analysis by Card Category
- Platinum: Cardholders have the highest attrition rate at 25%, significantly above the overall average, but it's important to note the small sample size (20 customers).
- Gold: Cardholders experience an attrition rate of 18.10%, also above the overall average.
- Blue: The most common card category, with 93% of the total customers, shows an attrition rate of 16.10%, slightly above the overall average.
- Silver: Cardholders have a lower attrition rate of 14.77%.

#### Analysis of the numeric features. Based on the correlation matrix, there are several conclusions that can be draw regarding factors that appear to be correlated with customer attrition:
- Months_Inactive_12_mon: There is a positive correlation (0.15) between the number of months a customer has been inactive in the last 12 months and attrition. This suggests that customers who are not actively using their credit cards are more likely to leave the company.
- Contacts_Count_12_mon: There is also a positive correlation (0.20) with the number of contacts or interactions a customer has with the company in the last 12 months. This could indicate that higher interaction might be due to issues or problems customers are facing, which could lead to attrition.
- Total_Relationship_Count: There is a negative correlation (-0.15) which suggests that customers who have more products or services with the company are less likely to attrit. This could be a sign of stronger loyalty or engagement with the company.
- Total_Revolving_Bal: There is a notable negative correlation (-0.26) between the total revolving balance on a customer's account and attrition. Customers with higher revolving balances, which may reflect their usage of the credit card, appear less likely to attrit.
- Total_Trans_Ct: There is a strong negative correlation (-0.37) with the total number of transactions, indicating that customers who make more transactions are less likely to attrit.
- Total_Ct_Chng_Q4_Q1: The negative correlation (-0.29) here suggests that customers who have shown a decrease in the number of transactions from Q4 to Q1 are more likely to attrit.
- Avg_Utilization_Ratio: There is a negative correlation (-0.18) with attrition, indicating that customers with a higher utilization ratio of their credit card limits are less likely to leave.
- Total_Trans_Amt: There is also a negative correlation (-0.17) with the total amount of transactions, supporting the idea that higher credit card usage is associated with lower attrition rates.
- Total_Amt_Chng_Q4_Q1: The negative correlation (-0.16) suggests that customers whose transaction amounts have decreased from Q4 to Q1 are more prone to attrition.
- Credit_Limit: The negative correlation (-0.02) is quite weak, indicating there might not be a strong direct relationship between the credit limit assigned to the customer and their likelihood to attrit.

The strongest correlations with attrition are related to inactivity and engagement. Customers who are less active and engage less with the company through transactions or revolving balances are more likely to attrit. Conversely, customers who have a higher number of transactions and a higher utilization ratio are less likely to leave.

These correlations can help identify at-risk customers and inform strategies to improve customer retention, such as encouraging increased usage of credit card services, maintaining revolving balances, and addressing issues that lead to increased customer contacts.

### Summary
In synthesizing the insights from both categorical and correlation analyses, it's possible to conclude that the following factors have significant relationships with customer attrition rates:
- Gender: Female customers are observed to have a higher attrition rate compared to male customers.
- Education Level: Those with Doctorate degrees show the highest attrition rates, indicating a potential link between higher education levels and propensity to attrit.
- Marital Status: Customers with an unknown marital status and those who are single tend to have higher attrition rates than their married or divorced counterparts.
- Income Category: There is a higher attrition rate observed among customers with incomes at the lower (<$40K) and higher (>$120K+) ends of the spectrum. This may suggest that financial challenges or unmet service expectations could be driving attrition in these groups.
- Card Category: Platinum and Gold cardholders have higher attrition rates, possibly due to dissatisfaction or unfulfilled expectations among customers with higher service demands.
- Customer Engagement: A higher number of transactions, larger revolving balances, and a higher credit utilization ratio are associated with lower attrition rates. Customers who engage more with the company's products and services are less likely to leave.
- Inactivity: Customers who have been inactive for more extended periods or who show a decrease in transaction amounts or counts from Q4 to Q1 are more likely to attrit. This suggests that maintaining customer engagement is crucial for retention.
- Interactions with Company: An increased number of contacts with the company correlates with higher attrition, which could reflect underlying issues that if unresolved, contribute to customer departure.

The combined analysis underscores the importance of active engagement and utilization of credit card services as protective factors against attrition. It also highlights the need for targeted retention strategies that consider not just demographic factors, but also customer behavior and interaction patterns. Strategies such as personalized communication, tailored financial products, proactive engagement initiatives, and enhanced customer service can be particularly effective for segments identified as having higher attrition risks.
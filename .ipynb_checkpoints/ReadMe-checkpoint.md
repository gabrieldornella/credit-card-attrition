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

### Summary - Exploratory Data Analysis
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

### Classification models

After an initial data exploration phase, I created another notebook (CreditCardChurn_ML) that proceeds with a structured approach to build machine learning models aimed at predicting customer churn for a credit card company.

Here's a breakdown of the steps followed:

#### Data Loading, Initial Exploration and Basic Feature Engineering

The process begins with loading the credit card churn dataset into a DataFrame. 
The Basic Feature Engineering step involves normalizing certain features to make them more suitable for modeling. Basic feature engineering aims to enhance the dataset's quality and make it more conducive to effective model training.

#### Splitting the Data

The dataset is divided into training and testing sets using the train_test_split function, allocating 70% of the data for training and 30% for testing. This split ensures that there's a sufficient amount of data for learning while also retaining a separate subset for unbiased model evaluation. Stratification is used to maintain consistent class proportions between the training and testing sets, and a random_state is set for reproducible results.

#### Advanced Feature Engineering

For preprocessing, I initialize a ColumnTransformer to apply OneHotEncoder to categorical variables and StandardScaler to numerical features. This ensures categorical data is transformed into a numerical format and all features are normalized for the machine learning algorithms.

#### Preparing a Dataframe for Results Storage
A dedicated DataFrame is prepared to store the results of different model evaluations. This systematic approach allows for easy comparison of model performance metrics, facilitating the selection of the best-performing model for prediction tasks.

#### Establishing a Baseline Model

A simple Logistic Regressionl model was created to serve as the baseline, providing a performance benchmark for more complex models.
This baseline is critical for understanding the incremental value offered by advanced modeling techniques and feature engineering.

#### Model Training and Hyperparameter Optimization

Three machine learning models were trained and evaluated: Logistic Regression, Support Vector Machine (SVM), and Decision Trees.
Each model is subjected to hyperparameter optimization to fine-tune its performance. This optimization is guided by cross-validation techniques to ensure the models' generalizability.
I also tested different threshold values for each model.

#### Feature importance

The feature importance analysis revealed distinct predictors that contribute to customer retention and attrition. The Decision Tree model identified the number of transactions (num__Total_Trans_Ct) as the most significant feature, suggesting a higher number of transactions correlates with decreased churn risk. Conversely, the Logistic Regression model highlighted the total transaction amount (num__Total_Trans_Amt) as a critical indicator, with larger transaction amounts increasing the likelihood of churn. These insights imply that while the frequency of customer engagement via transactions tends to enhance customer loyalty, the transaction size itself may be an attrition risk factor, potentially indicating customer satisfaction or pricing issues.

Further examination of the Logistic Regression model coefficients provided nuanced understandings of churn risk. Positive coefficients, such as those associated with the cat__Income_Category_$120K+, indicate factors that increase churn probability, while negative coefficients, like those for number of transactions (num__Total_Trans_Ct), suggest protective factors against churn. These results enable targeted strategies focusing on customer segments more likely to churn and inform the design of personalized retention programs aimed at mitigating these risks. 

#### Final Model Comparison and Recommendation
The models were compared based on their performance metrics, including accuracy, precision, recall, and the F1 score. This comprehensive evaluation helps identify the most effective model for predicting credit card churn. Special emphasis is placed on the recall metric, given the high cost associated with failing to identify potential churners.

##### Choosing the Right Metric

For predicting the risk of losing a customer, especially with imbalanced data, the F1 score seens a good choice because it balances Precision and Recall, thus providing a more holistic view of the model's performance across both classes.
If the credit card company decides to focus on intervention programs where the cost of false positives (wasted resources on customers not at risk) is significantly less than the cost of false negatives (missing a customer who churns), then prioritizing Recall might also be justifiable.

##### Models Performance

Here's a ranking of the models based on their F1 scores, with a secondary consideration given to Recall when F1 scores are close:

###### SVM with Threshold 0.50 (Model 5)
- F1: 0.785950, Recall: 0.733607, ROC_AUC: 0.964798
- Best balance of F1 and Recall with the highest F1 score among the models.

######  DecisionTree with Threshold 0.25 (Model 7)
- F1: 0.805911, Recall: 0.838115, ROC_AUC: 0.915220
- Second highest F1 score, very high Recall.

###### SVM with Threshold 0.25 (Model 4)
- F1: 0.772556, Recall: 0.842213, ROC_AUC: 0.964798
- High Recall, but slightly lower F1 compared to the SVM model with a threshold of 0.50.

###### DecisionTree with Threshold 0.50 (Model 8)
- F1: 0.801262, Recall: 0.780738, ROC_AUC: 0.915220
- Slightly lower F1 and Recall than the top models, but still very competitive.

###### DecisionTree with Threshold 0.70 (Model 9)
- F1: 0.796117, Recall: 0.756148, ROC_AUC: 0.915220
- Good F1 and Recall, slightly lower than the other top models.

###### LogisticRegression with Threshold 0.25 (Model 1)
- F1: 0.678182, Recall: 0.764344, ROC_AUC: 0.915084
- Lower F1 than the top models but has a high Recall.

###### SVM with Threshold 0.75 (Model 6)
- F1: 0.706918, Recall: 0.575820, ROC_AUC: 0.964798
- Lower Recall compared to other models but has a decent F1 score.

###### LogisticRegression with Threshold 0.50 (Model 2)
- F1: 0.634731, Recall: 0.543033, ROC_AUC: 0.915084
- Lower F1 and Recall than most other models.

###### Baseline Model (Model 0)
- F1: 0.633094, Recall: 0.540984, ROC_AUC: 0.914939
- Similar performance to LogisticRegression Model 2 but is the baseline for comparison.

###### LogisticRegression with Threshold 0.70 (Model 3)
- F1: 0.514936, Recall: 0.370902, ROC_AUC: 0.915084
- The lowest F1 and Recall among the models, making it the least favorable based on the criteria.

This ranking prioritizes models with a higher F1 score as the primary metric for a balanced evaluation between Precision and Recall. The Recall metric is used to differentiate between models with similar F1 scores, considering the specific context of predicting customer churn where identifying as many true positives as possible may be particularly valuable.

#### Conclusion

The comprehensive analysis conducted on the credit card customer dataset has shed valuable light on the multifaceted nature of customer attrition. It has elucidated a number of key demographic and behavioral factors that correlate with the likelihood of a customer discontinuing service. Among these, the engagement metrics such as the number of transactions and total revolving balance stand out as pivotal factors. Notably, higher engagement correlates inversely with attrition, underscoring the importance of active customer relationships in retention strategies.

The feature importance analysis has been particularly revealing, identifying concrete variables that can inform proactive measures. For instance, it highlighted that transaction frequency (num__Total_Trans_Ct) is inversely related to churn, while transaction amount (num__Total_Trans_Amt) showed a positive relationship, providing actionable insights for targeted customer interventions.

In selecting the optimal predictive model for churn, the SVM with a threshold of 0.50 emerged as the frontrunner, exhibiting a superior balance of precision and recall encapsulated by the highest F1 score. This model stands as the most capable in our analysis for identifying potential churners without excessively misclassifying loyal customers, a balance that is crucial for the cost-effective allocation of retention resources.

The analysis also underscores the need for a nuanced approach to customer retentio, strategies that encourage increased card usage and consistent engagement could be key to reducing churn rates.

This study serves as a foundation for the credit card company to refine its retention strategies. By leveraging the insights gleaned from the data, the company can not only anticipate and mitigate potential churn but also foster a more loyal and engaged customer base. The findings of this study provide a clear direction for evolution, pointing towards the immense value of data-driven decision-making in the realm of customer relationship management.
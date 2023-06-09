# Predict Customer Personality to Boost Marketing Campaign using Machine Learning

## Introduction
In this project we need to predict customer personality through marketing campaign performed by company. We need to analyze the conversion rate based on income, spending and age; customer personality for marketing retargeting and cluster analysis. To predict and analyze it I used python for data science in Jupyter Notebook.

## Feature Engineering
In this stage we need to add some new columns to analyze the relation with conversion rate. The columns we need to add are:
- Age Category
- Total Amount Spent
- Total Accepted Campaign
- Total Transaction
- Conversion Rate

## EDA: Conversion Rate Analysis based on Income, Spending and Age
At this stage, we analyze the relationship between the feature "conversion rate" and "income" or "age". The data exploration results indicate that as income increases, there is a tendency for customers to have higher expenses and larger total expenditures on our platform. However, this trend is not observed in other features such as age.

Recommendation: We can target customers with an income of 60 million or more for marketing campaigns, focusing on those with a conversion rate above 10%. But what about other customer segments? Is there anything we can do for them?

## Data Cleaning & Preprocessing
- Handle Missing Values
- Handle Duplicated Values
- Feature Encoding
- Standardization

## Data Modeling
In this project, for data modeling we focused on clustering using K-Means Clustering. To find and evaluate the number of the best cluster we use Elbow Method and Shilouette Score.

<img src="/img/elbow.png" alt="Gambar" width="450" height="300"> <img src="/img/shilouette.png" alt="Gambar" width="450" height="300">

From the chart above, we found that the optimal number of clusters is 4, which effectively separates each cluster with the most optimal distance.

## Customer Personality Analysis
### Cluster Analysis
From the 4 cluster we got before, there are some insight and information about the clusters:
1. Low Spender
  - This group is dominated by older adults (>55 years) and middle-aged adults (36-55 years), most of whom are married and have one child.
  - They visit the website quite frequently, second only to Cluster 1, with a median of 5 visits per month. However, they often search for promotions and each person buys a promotion twice a month (median).
  - However, this group has the second lowest total income and expenditure compared to other clusters, with a total annual income of IDR 57 million and annual expenditure of IDR 506K.

2. Risk of Churn
  - This group is the largest group with 900 users, dominated by middle-aged adults (36-55 years), most of whom are married and have one child.
  - In terms of income and expenditure, this group has the lowest monthly income and expenditure, with a total annual income of IDR 33.4 million and annual expenditure of IDR 57K.
  - Despite that, this group visits the website most frequently, with a median of 7 visits per month. However, they rarely make transactions or use promotions in their transactions.
  - They also have a low response rate to campaigns compared to other clusters, as most of them come through organic means.

3. Mid Spender
  - This group is dominated by older adults (>55 years) and middle-aged adults (36-55 years), most of whom are married and have 0-1 child.
  - They have the second highest total income and expenditure compared to other clusters, with a total annual income of IDR 68 million and annual expenditure of IDR 1.1 million.
  - Although they visit the website less frequently, this group is the most responsive to our campaigns and they use promotions the most, with an average of 3 promo usages per month.

4. High Spender
  - This group is the smallest with 137 users, dominated by older adults (>55 years) and middle-aged adults (36-55 years), most of whom are unmarried and do not have children.
  - In terms of income and expenditure, this group has the highest monthly income and expenditure, with a total annual income of IDR 80 million and annual expenditure of IDR 1.2 million.
  - This cluster has a significant number of non-organic users who respond to campaigns, but they have the lowest number of promo usages compared to other clusters.
  - This group has the highest conversion rate for purchasing our products, and we should not lose them.


### Recommendation and Potential Impact
- Recommendation
  1. Continue monitoring transactions and retention from the High Spender group. Focus on improving services to ensure customer loyalty and reduce the risk of churn.
  2. For the Mid Spender group, conduct further analysis to identify ways to increase their transactions. Provide personalized recommendations and optimize promotions specifically for this segment to encourage them to make more purchases on the platform.
  3. For the Low Spender and Risk of Churn groups, analyze further to understand how to improve the conversion ratio from website visits to transactions. They have a high number of visits but low transaction rates, which could be due to mismatched products or prices.

- Potential Impact
  1. By focusing on monitoring the High Spender group, we can maintain a potential GMV of IDR 176 million.
  2. If we optimize promotions for the Mid Spender group (assuming a 50% cost reduction), we can reduce costs by IDR 50 million.

By implementing these recommendations, we can enhance customer engagement, increase conversions, and maximize the potential revenue from each customer segment.

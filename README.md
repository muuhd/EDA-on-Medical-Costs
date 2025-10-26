# EDA-on-Medical-Costs

## **Project Overview**
This project explores factors that influence the medical costs of beneficiaries. We aim to identify relationships and trends between beneficiary characteristics, such as age, BMI and smoking status, with their medical cost.

## **Dataset Information**
Source: Artificial dataset meant for practice use only

Rows: 1340

Columns: PersonID, age, sex, bmi, children, smoker, region, charges

## **Data Preparation**
- Remove missing data
- Standardise gender entries ("M"/"F" to "male"/"female)
- Remove outliers based on medical cost

## **Visualisations and Insights**
1. Correlation between Age and Charges
<img width="1748" height="1358" alt="image" src="https://github.com/user-attachments/assets/751824d1-13f4-4db2-9759-7b50ee9f9330" />

Insights:

Positive correlation observed between these 2 factors. Older beneficiaries tend to be charged higher as compared to younger beneficiaries. This could be likely due to older beneficiaries having underlying medical conditions that develop as they age, driving up medical costs due to additional medication and care needed. Small cluster between age 18-25 among the residuals also seen, anomaly could be due to injuries sustained from high-risk activities such as sports.


2. Average medical charge by smoking status
<img width="1915" height="1401" alt="image" src="https://github.com/user-attachments/assets/740362f4-1acf-49ef-ada7-3c1d86a8cab1" />

Insights:

Large difference (2.5x) of the mean medical charges between non-smokers and smokers. This large difference could be a result of health risks associated with smoking, leading to additional medical care in treatments for diseases like bronchitis. Graph also highlights a positive correlation between smoking status and medical charges.


3. Heatmap of mean charges by age and bmi
<img width="3000" height="2100" alt="image" src="https://github.com/user-attachments/assets/7be6472e-8767-4e67-ae5b-879b39181077" />

Insights:

Mean medical charges are still higher for older beneficiaries compared to younger ones, as seen in visualisation 1. Interesting observation where at different age ranges, different weight classes hold the highest mean medical charges (more notably Normal BMI for age 50-59). This hints that being more "unhealthy" does not necessarily mean one is charged higher. Likewise, medical charges go beyond BMI and other variables must be considered such as the type of treatment. Hence, we should not rely on BMI alone to estimate the medical costs.


4. Decision tree
<img width="3975" height="2004" alt="image" src="https://github.com/user-attachments/assets/d78a9e3b-1a40-49f5-a98f-1b804967a8ac" />

Insights:

"Charges" is the most important predictor, making it the root node. Comparing the features, “bmi” occurs the most frequently as a basis as compared to “age” which makes it a more significant feature in prediction. In the leaf nodes, the gini value is relatively low, signalling more confident predictions. We also see an overwhelming difference between the classes within the node which highlights the confidence in assigning the appropriate class. However, we should note that majority of the leaf nodes have the same class: “no smoke”. This could highlight that the dataset used may have a disproportionate amount of non-smokers compared to smokers, potentially skewing the predictions for smokers.



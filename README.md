# Prodigy InfoTech Data Science Internship Task 2

![Screenshot 2025-04-25 233229](https://github.com/user-attachments/assets/d8590a22-0f33-4712-8868-fdb7caa41280)

I am excited to share my second task as a Data Science Intern at Prodigy InfoTech. In this project, I performed data cleaning and exploratory data analysis (EDA) on the Titanic dataset from Kaggle. The goal was to uncover relationships between variables, identify patterns, and highlight trends within the data using statistical analysis and visualizations.

# 1. Introduction

The sinking of the RMS Titanic on April 15, 1912, remains one of the most infamous maritime disasters in history. Of the estimated 2,224 passengers and crew aboard, more than 1,500 died, making it one of the deadliest commercial peacetime maritime disasters in modern history.

This analysis explores the factors that influenced survival rates among passengers, using data science techniques to uncover patterns and relationships within the dataset. We will perform a step-by-step analysis, including data cleaning, exploratory data analysis, variable relationship analysis, and pattern identification.

The Titanic dataset contains demographic and travel information for passengers, including variables such as:

• Passenger class (Pclass)  
• Sex  
• Age  
• Number of siblings/spouses aboard (SibSp)  
• Number of parents/children aboard (Parch)  
• Passenger fare (Fare)  
• Survival status (Survived: 0 = No, 1 = Yes)  


# 2. Data Acquisition and Preparation

In this step, we acquire the Titanic dataset and prepare it for analysis. The dataset is split into training and testing sets to facilitate machine learning applications, though our focus will be on exploratory analysis.

The dataset contains information about 887 passengers from the Titanic. For analysis purposes, we split the data into:

**• Training set: 709 passengers  
• Test set: 178 passengers**

![image](https://github.com/user-attachments/assets/99f2e15f-9c2a-408c-9571-1234fd09ecae)
Figure 2.1: Distribution of passengers across different classes


![image](https://github.com/user-attachments/assets/91e9354c-f27c-4c4f-b6af-8197ed430742)
Figure 2.2: Gender distribution of passengers

The raw data shows that the majority of passengers were in 3rd class, and there were more male passengers than female passengers. This initial observation will be important when we analyze survival rates later.


# 3. Data Cleaning and Feature Engineering

Data cleaning is a crucial step in any data analysis project. In this step, we handle missing values, create new features, and convert categorical variables to appropriate formats for analysis.

The dataset we are working with has no missing values, which is convenient for our analysis. In real-world scenarios, the Titanic dataset often has missing values in Age, Cabin, and Embarked columns that would need to be handled.

**Feature Engineering**
To enhance our analysis, we create several new features:

**1. Family Size:** Calculated as the sum of siblings/spouses and parents/children aboard, plus the passenger themselves.  
**2. Is Alone:** A binary indicator of whether the passenger is traveling alone (1) or with family (0).  
**3. Age Groups:** Passengers categorized into age bands (Child, Teenager, Young Adult, Adult, Senior).  
**4. Fare Groups:**  Fare values divided into quartiles (Low, Medium-Low, Medium-High, High).  


![image](https://github.com/user-attachments/assets/c2068e13-e790-4f48-bae4-0b1d1b9e6020)
Figure 3.1: Distribution of family sizes among passengers


![image](https://github.com/user-attachments/assets/be742c75-51e3-418f-997b-df9d3864d810)
Figure 3.2: Distribution of passengers across different age groups


The feature engineering process has created several new variables that will help us better understand the factors affecting survival. For example, we can now analyze survival rates by family size and age group, which may reveal interesting patterns.


# 4. Exploratory Data Analysis (EDA)

Exploratory Data Analysis (EDA) is a critical step in understanding the dataset and identifying patterns. In this section, we explore the distributions of individual variables and their relationships with survival.

The overall survival rate among passengers in the training dataset was 38.79%, indicating that approximately 38% of passengers survived the disaster.

![image](https://github.com/user-attachments/assets/8f3b7ceb-4e14-42be-a3fb-7056be449cee)
Figure 4.1: Overall survival distribution


![image](https://github.com/user-attachments/assets/5935ef96-fc2f-43ca-bae6-e3d2b7493562)
Figure 4.2: Survival rate by passenger class

The analysis shows a clear pattern: 1st class passengers had the highest survival rate (64.12%), followed by 2nd class (48.97%), and 3rd class (24.11%). This suggests that social class played a significant role in survival chances.

![image](https://github.com/user-attachments/assets/59f58b3a-d156-4106-b6db-00b0e02b71d1)
Figure 4.3: Survival rate by gender

The analysis reveals a dramatic difference in survival rates between genders: females had a 75.10% survival rate, while males had only a 17.63% survival rate. This reflects the "women and children first" protocol that was followed during the evacuation.


![image](https://github.com/user-attachments/assets/45a2c2f9-27b4-4ec0-9182-fb8dfe2d36c4)
Figure 4.4: Survival rate by age group

The analysis shows that children had the highest survival rates, followed by teenagers and young adults. This is consistent with the "women and children first" maritime protocol.


![image](https://github.com/user-attachments/assets/d930647d-0cb0-4f1a-baa4-b321250a0971)
Figure 4.5: Correlation matrix of key variables


**The correlation analysis reveals several significant relationships:**
• Sex and Survival: 0.57 correlation, indicating females had much higher survival rates.  
• Pclass and Survival: -0.35 correlation, showing that higher class passengers (lower Pclass values) had better survival rates.  
• Age and Survival: -0.04 correlation, indicating a slight tendency for younger passengers to survive.  
• Fare and Survival: 0.26 correlation, suggesting passengers who paid higher fares had better survival chances.  



# 5. Variable Relationship Analysis

In this section, we delve deeper into the relationships between different variables and survival, examining how these factors interacted to influence survival outcomes.

![image](https://github.com/user-attachments/assets/71b1108f-4314-4f9a-87d4-110ae6627d1c)
Figure 5.1: Survival rates by gender and class

**The analysis reveals a striking interaction between gender and class:**
**• Female 1st class passengers: 97.53% survival rate  
• Female 2nd class passengers: 96.72% survival rate  
• Female 3rd class passengers: 48.74% survival rate  
• Male 1st class passengers: 33.71% survival rate  
• Male 2nd class passengers: 14.29% survival rate  
• Male 3rd class passengers: 13.45% survival rate** 

This stark contrast highlights the combined effects of gender bias and class privilege during the disaster. Female first-class passengers had an almost guaranteed survival rate, while male third-class passengers had the lowest chances of survival.



![image](https://github.com/user-attachments/assets/aad00e87-9e54-4dd3-a772-d259ba2acf63)
Figure 5.2: Survival rate by family size

**The analysis reveals an interesting non-linear relationship between family size and survival:
• Passengers traveling alone: 31.55% survival rate  
• Small families (2-4 members): 58.48% survival rate  
• Large families (5+ members): 14.81% survival rate**

Passengers traveling in small family groups had the highest survival rates, while those in large families had the lowest. This might be because small families could stay together during evacuation, while larger families may have been separated or faced more difficulties finding space in lifeboats.


![image](https://github.com/user-attachments/assets/c627d2b5-1ea4-4d32-9e07-83fe5e057601)
Figure 5.3: Relationship between age, fare, and survival

The scatter plot shows the relationship between age, fare, and survival. We can observe that passengers who paid higher fares generally had better survival chances, regardless of age. However, there is a concentration of survivors among younger passengers and those who paid higher fares.

# 6. Pattern and Trend Identification
Based on our analysis, we can identify several key patterns and trends in the Titanic dataset that influenced passenger survival.


![image](https://github.com/user-attachments/assets/d992b908-b357-4cd0-81ea-9942fe5ea4e6)
Figure 6.1: Significance of identified patterns affecting survival


**Feature Importance**
To quantify the importance of different features in predicting survival, we can use a machine learning model like Random Forest. The feature importance scores indicate how much each feature contributes to the prediction of survival.

![image](https://github.com/user-attachments/assets/50e2f8ef-ab23-4fcf-bae7-c1bd3a77123a)
Figure 6.2: Feature importance for survival prediction

The feature importance analysis confirms our findings from the exploratory analysis:
1. Gender (Sex): The most important factor, accounting for about 28% of the predictive power.  
2. Fare: The second most important factor, accounting for about 23% of the predictive power.  
3. Age: The third most important factor, accounting for about 22% of the predictive power.  
4. Passenger Class (Pclass): The fourth most important factor, accounting for about 8% of the predictive power.  
5. Family Size: The fifth most important factor, accounting for about 5% of the predictive power.

These results align with the patterns identified in our exploratory analysis, confirming that gender, fare, and age were the most significant factors in determining survival outcomes.



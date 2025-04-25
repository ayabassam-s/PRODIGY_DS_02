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

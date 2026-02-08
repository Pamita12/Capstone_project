## Contents
1. [Group Information](#group-information)
2. [Project Name](#project-name)
3. [Project Purpose](#project-purpose)
4. [Business Benefits](#business-benefits)
5. [Appendix](#appendix)
   - [Preliminary Dashboard in Power BI](#1-preliminary-dashboard-in-power-bi)
   - [RCS dataset](#2-rcs-dataset)
   - [Exploratory Data Analysis (EDA)](#3-exploratory-data-analysis-eda)
   - [Business Case and Project Charter](#4-business-case-and-project-charter)
   - [Machine Learning Predictions](#5-machine-learning-predictions)

## Group Information:
- **Project Sponsor**: Sean Bridgeman
- **Project Coordinator**: Prof. Manjari Maheshwari 
- **Core Team Members (5-person team):**
    - Eddie Morgan (Team Lead)
    - Diego Moreno
    - Sofia Alfaro
    - Pamela Gatica
    - Yazan Al Shash
## Project Name
- **Retention Framework Insights**
## Project Purpose
- This project is designed to help a local company in Tecumseh, ON, understand how users move through their learning journey.
- By analyzing where users drop off and how they engage, our final dashboard may give clear insights to improve retention, help with better decision making and show possible opportunities to make the learning experience more engaging and effective. 
- The data was sourced through a third party (Halight) via Athena; an AWS SQL Server.
## Business Benefits
- Benefit 1: Improve user retention by identifying drop-off points and enabling targeted engagement strategies.
- Benefit 2: Support data-driven decision-making for product and customer strategy teams through weekly lifecycle insights.
- Benefit 3: Increase efficiency by automating user journey reporting and reducing manual analysis time.
- Benefit 4: Discover growth opportunities by uncovering patterns in user behavior and lifecycle progression.
## Appendix:
The deliverables for our Capstone Project are listed down below:


### 1. _**Preliminary Dashboard in Power BI**_
    - Displays insights about user engagement metrics, such as:
      - Online users (Current Month vs Last Month and Last Year)
      - Average Daily Engagement Score over time
      - Total & Average Lifetimes per User

### 2. _**RCS dataset**_

    - A Command-Separated-Value (CSV) flat file comprising of 30 variables and 856 observations
    - Some notable variables used in our analysis include:
      - _avg_daily_engagement_score_
      - _total_lifetimes_
      - _client_name_
      - _region_name_
      - _month_date_
      - _online_users_
      - _survey completions_

### 3. **_Exploratory Data Analysis (EDA)_**
    - Used EDA to summarize the characteristics of the dataset, detect patterns/relationships, and identify outliers.
    - Assessed various Machine Learning methods to make future predictions on the project for the Winter session.

### 4. **_Business Case and Project Charter_**
    - This section outlines the purpose, justification, and structure of the project.
    - It defines the problem being addressed, project objectives, expected benefits, constraints, and risks.
    - It also establishes the project scope, key stakeholders, and high-level plan that will guide the development process.
  
### 5. **_Machine Learning Predictions_**
    - In this section, we apply three machine learning techniques to classify engagement levels (high vs. low) and to forecast engagement trends for 2026 using historical data.
    - The models and techniques used include:
        - Seasonal Naive Forecasting for projecting future engagement trends
        - K-Means Clustering for identifying engagement patterns
        - Logistic Regression for predicting high and low engagement 
 
 
 


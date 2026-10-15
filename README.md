# Customer Churn Prediction using The Complete Journey Dataset

A business analytics project that explores customer shopping behavior and predicts which customers may stop shopping at a retailer. Using **The Complete Journey Dataset**, this project combines data analysis, dashboards, and machine learning to identify customer trends and support better business decisions.

**Project website:** [Explore the project](https://sites.google.com/student.upm.edu.my/group-6-complete-journey/introduction)

## Project Overview

Customer churn happens when customers stop buying from a business. Understanding why customers become less active can help businesses improve their services, marketing strategies, and customer retention.

This project analyzes retail shopping data to answer questions such as:

- What products do customers buy most often?
- How do sales and shopping patterns change over time?
- How do customers respond to marketing campaigns and coupons?
- Which customers may be at risk of becoming inactive?

The project covers **data cleaning, exploratory data analysis, dashboard visualization, data modeling, customer churn prediction, and business recommendations**.

## Dataset

The project uses **The Complete Journey Dataset**, which contains approximately one year of shopping activity from **2,469 households**.

| Data | What it contains |
| --- | --- |
| Transactions | Purchases, quantities, spending, and dates |
| Products | Product categories, brands, and departments |
| Demographics | Available customer details, such as age, income, and household size |
| Marketing campaigns | Campaign information and customer participation |
| Coupons | Promotional offers and coupon redemptions |

**Source:** [The Complete Journey Dataset Documentation](https://bradleyboehmke.github.io/completejourney/articles/completejourney.html)

## Tools and Techniques

| Area | Tools / Techniques |
| --- | --- |
| Data analysis | Excel, data cleaning, Exploratory Data Analysis (EDA) |
| Data visualization | Dashboards, charts, and Key Performance Indicators (KPIs) |
| Data modeling | Star schema and multidimensional modeling |
| Machine learning | RapidMiner, Naive Bayes, Support Vector Machine (SVM), k-Nearest Neighbors (kNN) |

## Project Workflow

### 1. Data Cleaning and Exploratory Data Analysis (EDA)

The data was prepared and explored to understand customer purchasing behavior. This involved checking data quality, handling missing values, organizing information, and identifying useful patterns.

The analysis focused on:

- Customer participation in marketing campaigns.
- Frequently purchased products and product categories.
- Weekly sales trends and customer spending.
- Coupon usage and customer engagement.

**Key finding:** Campaign Type A had the strongest participation among the campaign types analyzed. Soft drinks were also among the frequently purchased products shown in the analysis.

[View EDA and Marketing Campaign Dashboard](https://sites.google.com/student.upm.edu.my/group-6-complete-journey/task-1)

### 2. Sales Dashboard and Data Modeling

A sales dashboard was developed to turn transaction data into charts and business insights. A **star schema** was also used to organize data for easier reporting and analysis.

The dashboard presents:

- Revenue and sales quantity.
- Sales performance by product category and department.
- Sales trends over time.
- Store performance and discount patterns.

[View Sales Dashboard and Data Model](https://sites.google.com/student.upm.edu.my/group-6-complete-journey/task-2)

### 3. Customer Churn Prediction

Machine learning was used to classify customers based on shopping activity. For this project, customers who shopped in **15 or fewer weeks** during a 52-week period were labeled **Churn**, while those active for more than 15 weeks were labeled **Loyal**.

Three models were compared:

| Model | Accuracy (70/30 train-test split) | Accuracy (10-fold cross-validation) |
| --- | ---: | ---: |
| Naive Bayes | 73.15% | 72.05% |
| Support Vector Machine (SVM) | 84.26% | 96.68% |
| k-Nearest Neighbors (kNN) | **99.52%** | **99.20%** |

**Result:** kNN achieved the highest reported accuracy in the project evaluation. These are academic results based on the project's definition of churn; they do not establish how well the models would perform on new real-world data.

[View Churn Prediction Models and Results](https://sites.google.com/student.upm.edu.my/group-6-complete-journey/task-3)

### 4. Business Recommendations

The findings were used to suggest practical ways a retailer could improve sales and retain customers, including:

- Promoting products with strong sales performance.
- Reviewing discounts and marketing campaigns.
- Investigating stores with lower sales performance.
- Using customer behavior trends to guide retention strategies.

[View Business Recommendations](https://sites.google.com/student.upm.edu.my/group-6-complete-journey/task-4)

## My Contributions

I focused mainly on **Exploratory Data Analysis (EDA) and dashboard development**. My contributions included:

- Analyzing customer purchasing patterns, campaign engagement, and churn-related trends.
- Identifying useful insights from the data and presenting them in a clear way.
- Designing and developing dashboards with charts and key business metrics.
- Explaining dashboard findings to make the results easier to understand and use in business discussions.

## Project Resources

The full analysis, dashboards, and project results are available here:

- [Project Introduction](https://sites.google.com/student.upm.edu.my/group-6-complete-journey/introduction)
- [Data Cleaning and EDA](https://sites.google.com/student.upm.edu.my/group-6-complete-journey/task-1)
- [Sales Dashboard and Data Modeling](https://sites.google.com/student.upm.edu.my/group-6-complete-journey/task-2)
- [Churn Prediction and Model Results](https://sites.google.com/student.upm.edu.my/group-6-complete-journey/task-3)
- [Business Recommendations](https://sites.google.com/student.upm.edu.my/group-6-complete-journey/task-4)

## What I Learned

This project helped me improve my skills in **data analysis, dashboard development, and data storytelling**. I learned how to turn large amounts of customer data into clear insights and how analytics can support business decisions, including improving customer retention.

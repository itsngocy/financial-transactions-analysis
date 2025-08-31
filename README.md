# Financial Transactions Analysis

## Project Overview

This project focuses on cleaning, transforming, and analyzing a large dataset of financial transactions. The goal is to prepare high-quality, structured data for deeper business insights and potential applications in customer behavior analysis and financial reporting.

The data used in this project includes transaction records, customer details and card information from a banking institution throughout the 2010s. 

You can find the dataset [here](https://www.kaggle.com/datasets/computingvictor/transactions-fraud-datasets/data)

**The workflow includes:**

- Data Preprocessing: cleaning and standardizing raw datasets using Python.
- Implementing a Star Schema with fact and dimension tables.
- Using SQL Server `BULK INSERT` to load cleaned csv data.
- Creating dashboards in Power BI for transaction, user and merchant analytics. 

**Objectives:**

- Understand spending patterns across card types, transaction types and time periods.
- Profile users based on demographics, income, debt and credit scores.
- Analyze merchants by transaction volume and geographical distribution.
  
## Data Structure

<img width="925" height="710" alt="image" src="https://github.com/user-attachments/assets/06134cea-9546-48f9-bf93-4734362c38dd" />

- **Fact Table**: `fact transaction`: transaction details

- **Dimension Tables**:
  - `dim_user`: user demographic and financial attributes
  - `dim_card`: card details
  - `dim_merchant`: merchant details
  - `dim_mcc`: merchant category code definitions
  - `dim_date`: calendar attributes
 
## Dashboards
  
  Created 3 dashboards using Power BI
  
  - **Overview**
    <img width="1563" height="835" alt="image" src="https://github.com/user-attachments/assets/f17abf75-1597-488f-8a16-cf6cdbbd796d" />

  - **User & Card Insight**
   <img width="1570" height="828" alt="image" src="https://github.com/user-attachments/assets/ac0672a8-31cb-4c8e-8190-7b41b6f64e45" />

  - **Merchant & Merchant Category**
    <img width="1578" height="841" alt="image" src="https://github.com/user-attachments/assets/f0b3815d-810f-433e-9d3e-8a3650665554" />

## Key Findings

**1. Overview**

- Mastercard contributes the largest share (**50.35%**) of total spending, followed by Visa (**38.22%**).
- Transaction amounts remain stable throughout the year with slight drops in February and November.
- Swipe transactions generate the highest volume and amount but also hae the highest error rate.

**2. User & Card Insight**

- Mastercard is the most popular among users (**52.21%**) and the majority of users hold Debit cards (**57.13%**), while Prepaid cards are least common (**9.4%**).
- Users aged 30 - 50 have the highest debt ratio, while from aged 60 and onwards, debt ratio significantly drops.
- Users with Credit Score < 600 show high debt, classifying them into High Risk, users with medium-to-high scores are more evenly distributed.
- Higher credit scores generally correlate with higher yearly income, though a few low-score outliers still show significant income.

**3. Merchant & Merchant Cateogry**

- Top merchant categories: Money Transfer leads with **53.1M** transaction volume, Wholesale Clubs and Tolls & Bridges follow next.
- Transaction volume is heavily concentrated in the United States, particularly in California, New York and Texas; Europe and Asia have fewer but notable clusters of merchant activity.
- The top 5 merchants contribute a significant share of total transaction value, showing strong dependency on a few categories. 

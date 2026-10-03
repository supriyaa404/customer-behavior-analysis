# Customer Shopping Behavior Analysis

An end-to-end **Data Analytics project** that analyzes customer shopping behavior using Python, PostgreSQL, and Power BI. The project covers data cleaning, exploratory data analysis, SQL-based business analysis, and interactive dashboard development.

## Overview

This project analyzes **3,900 customer purchase records** to identify patterns in:

* Customer spending behavior
* Product preferences
* Customer segments
* Subscription behavior
* Discounts and promotions
* Shipping preferences
* Revenue contribution across age groups

The objective is to convert raw transactional data into **actionable business insights** that can support marketing, customer retention, and product strategies. 

---

## Dataset

| Attribute      | Details                            |
| -------------- | ---------------------------------- |
| Records        | 3,900                              |
| Columns        | 18                                 |
| Data Type      | Customer shopping/transaction data |
| Database       | PostgreSQL                         |
| Missing Values | 37 values in `Review Rating`       |

### Key Features

* **Customer Information:** Age, Gender, Location, Subscription Status
* **Purchase Information:** Item Purchased, Category, Purchase Amount, Season, Size, Color
* **Shopping Behavior:** Discount Applied, Previous Purchases, Frequency of Purchases, Review Rating, Shipping Type 

---

## Tools & Technologies

* **Python** – Data loading, cleaning, EDA, and feature engineering
* **Pandas** – Data manipulation
* **Jupyter Notebook** – Analysis environment
* **PostgreSQL** – Database storage and SQL analysis
* **SQL** – Business-oriented data analysis
* **Power BI** – Interactive dashboard and visualization
* **Git & GitHub** – Version control and project sharing

---

## Project Workflow

```text
Raw Dataset
     ↓
Python Data Loading
     ↓
Data Exploration & EDA
     ↓
Data Cleaning
     ↓
Feature Engineering
     ↓
PostgreSQL Database
     ↓
SQL Business Analysis
     ↓
Power BI Dashboard
     ↓
Business Insights
```

---

## 1. Data Loading & Exploration

The dataset was loaded into Python using **Pandas**.

Initial analysis included:

* Dataset structure using `df.info()`
* Statistical analysis using `df.describe()`
* Null-value analysis
* Data consistency checks
* Understanding customer and purchase attributes

---

## 2. Data Cleaning

The following preprocessing steps were performed:

* Handled missing values in `Review Rating`
* Missing ratings were imputed using the **median rating of the respective product category**
* Standardized column names to `snake_case`
* Checked for redundant columns
* Removed `promo_code_used` after identifying its redundancy with `discount_applied` 

---

## 3. Feature Engineering

Additional features were created to improve the analysis:

* `age_group` – Customer age categories
* `purchase_frequency_days` – Purchase frequency represented in days

These features were later used for customer and revenue analysis. 

---

## 4. SQL Analysis

The cleaned dataset was loaded from Python into **PostgreSQL** for structured business analysis.

Key SQL analyses included:

1. Revenue by gender
2. High-spending customers using discounts
3. Top 5 products based on average rating
4. Standard vs. Express shipping comparison
5. Subscribers vs. non-subscribers
6. Products with the highest percentage of discounted purchases
7. Customer segmentation into **New, Returning, and Loyal**
8. Top 3 products within each category
9. Relationship between repeat purchases and subscriptions
10. Revenue contribution by age group 

---

## 5. Power BI Dashboard

An interactive **Power BI dashboard** was created to visually communicate the analysis and make the results easier to understand.

### Dashboard Focus

* Revenue analysis
* Customer demographics
* Product performance
* Subscription behavior
* Customer segments
* Discount behavior
* Age-group analysis
* Shopping and shipping patterns

The dashboard converts the SQL analysis into interactive business visualizations. 

### Dashboard Preview

> Add your Power BI dashboard screenshot here.

```markdown
![Power BI Dashboard](images/dashboard.png)
```

---

## Key Results & Business Insights

The analysis provides insights into:

* Revenue contribution across different customer groups
* Purchasing behavior of subscribers and non-subscribers
* Products receiving high customer ratings
* Discount-dependent products
* Repeat-buyer behavior
* Revenue contribution by age group
* Differences between shipping types
* New, returning, and loyal customer segments

These insights can be used to support decisions related to **customer retention, subscriptions, discounts, product marketing, and targeted campaigns**. 

---

## Project Structure

```text
customer-shopping-analysis/
│
├── data/
│   └── customer_shopping_behavior.csv
│
├── notebooks/
│   └── customer_behavior_analysis.ipynb
│
├── sql/
│   └── customer_analysis.sql
│
├── dashboard/
│   └── customer_behavior_dashboard.pbix
│
├── images/
│   └── dashboard.png
│
├── report/
│   └── Customer_Shopping_Behavior_Analysis.pdf
│
└── README.md
```

---

## How to Run

### 1. Clone the repository

```bash
git clone https://github.com/yourusername/customer-shopping-analysis.git
cd customer-shopping-analysis
```

### 2. Install Python dependencies

```bash
pip install pandas numpy matplotlib seaborn jupyter
```

### 3. Run the Jupyter Notebook

```bash
jupyter notebook
```

Open the analysis notebook and run the cells sequentially.

### 4. Set up PostgreSQL

Create a PostgreSQL database and load the cleaned dataset.

Then execute the SQL queries from:

```text
sql/customer_analysis.sql
```

### 5. Open the Power BI Dashboard

Open:

```text
dashboard/customer_behavior_dashboard.pbix
```

in **Power BI Desktop**.

---

## Skills Demonstrated

* Data Cleaning & Preprocessing
* Exploratory Data Analysis (EDA)
* Python & Pandas
* SQL
* PostgreSQL
* Feature Engineering
* Business Analysis
* Data Visualization
* Power BI Dashboard Development
* Business Insight Generation

---

## Business Recommendations

Based on the analysis, the report proposes:

* Promoting benefits for subscribers
* Rewarding repeat customers through loyalty programs
* Reviewing discount strategies while considering margins
* Promoting highly rated and frequently purchased products
* Using high-revenue customer groups for targeted marketing 

---

## Conclusion

This project demonstrates a complete **data analytics workflow**, from raw customer transaction data to cleaned datasets, SQL-based business analysis, and an interactive Power BI dashboard.

It showcases how **Python, SQL, and Power BI** can be combined to transform raw data into meaningful business insights and support data-driven decision-making.

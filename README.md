# 🛍️ Customer Shopping Behavior Analysis

## 📌 Overview

This project analyzes **customer shopping behavior** to uncover purchasing patterns, customer segments, product performance, and factors influencing revenue.

The project follows an end-to-end **data analytics workflow**, starting with data loading and cleaning in Python, followed by exploratory data analysis, PostgreSQL-based SQL analysis, Power BI dashboard development, and business reporting.

The analysis covers **3,900 customer purchases across 18 data columns**, including customer demographics, purchasing behavior, discounts, subscriptions, shipping preferences, and product ratings.

---

## 🎯 Project Objectives

The main objectives of this project are to:

* Understand customer purchasing behavior
* Identify high-value customer segments
* Analyze revenue across customer groups
* Evaluate the impact of discounts and subscriptions
* Identify top-performing and highly rated products
* Analyze shipping and purchasing patterns
* Generate actionable business insights through dashboards and reports

---

## 📊 Dataset

The dataset contains **3,900 customer purchase records** and **18 columns** covering customer demographics and shopping behavior.

Key attributes include:

* Customer ID
* Age
* Gender
* Category
* Item Purchased
* Purchase Amount
* Review Rating
* Shipping Type
* Discount Applied
* Subscription Status
* Previous Purchases
* Frequency of Purchases

The dataset initially contained missing values in the **Review Rating** column, which were handled during data preparation.

---

## 🛠️ Tools & Technologies

| Tool                 | Purpose                                           |
| -------------------- | ------------------------------------------------- |
| **Python**           | Data loading, cleaning, EDA & feature engineering |
| **Pandas**           | Data manipulation and preprocessing               |
| **PostgreSQL**       | SQL-based business analysis                       |
| **Power BI**         | Interactive dashboard development                 |
| **Gamma**            | Business presentation                             |
| **Jupyter Notebook** | Python analysis environment                       |
| **GitHub**           | Project documentation and version control         |

---

# 🔄 Project Workflow

## 1. Data Loading

The dataset was imported into Python using **Pandas** and initially examined to understand its structure, data types, descriptive statistics, and missing values.

```python
import pandas as pd

df = pd.read_csv("customer_shopping_behavior.csv")
```

---

## 2. Exploratory Data Analysis

Initial EDA was performed to understand the dataset and identify potential data-quality issues.

The analysis included:

* Dataset structure and information
* Descriptive statistics
* Missing-value analysis
* Unique-value analysis
* Distribution and category exploration

---

## 3. Data Cleaning & Feature Engineering

The dataset was prepared for further analysis by:

* Handling missing **Review Rating** values using category-level median imputation
* Standardizing column names
* Renaming columns for easier analysis
* Creating **Age Groups**
* Converting purchase-frequency categories into numerical day values
* Identifying redundant columns
* Removing the `promo_code_used` column after comparing it with `discount_applied`

Feature engineering included the creation of:

* `age_group`
* `purchase_frequnency_days`

---

## 4. PostgreSQL & SQL Analysis

The cleaned dataset was loaded into **PostgreSQL** for structured business analysis.

The project includes **10 SQL business questions**, covering areas such as:

* Revenue by gender
* High-value customers using discounts
* Top-rated products
* Shipping-type spending
* Subscriber vs. non-subscriber spending
* Discount rates by product
* Customer segmentation
* Top products within each category
* Repeat buyers and subscription behavior
* Revenue contribution by age group

For example, customer segmentation was created using previous purchase behavior:

```sql
CASE 
    WHEN previous_purchases = 1 THEN 'New'
    WHEN previous_purchases BETWEEN 2 AND 10 THEN 'Returning'
    ELSE 'Loyal'
END
```

Window functions such as `ROW_NUMBER()` were also used to identify the top products within each category.

---

# 📊 Power BI Dashboard

An interactive **Power BI dashboard** was developed to visualize the results of the analysis.

The dashboard focuses on:

* Customer purchasing behavior
* Revenue analysis
* Product performance
* Customer segmentation
* Subscription behavior
* Shipping preferences
* Discounts and purchasing patterns

**Power BI Dashboard:**
`[Add your Power BI report link here]`

**Dashboard Preview:**
`[Add dashboard screenshot here]`

---

# 📈 Key Results & Insights

The analysis generated several business insights.

### Customer & Revenue Analysis

Female customers generated slightly higher total revenue than male customers, highlighting a potential opportunity for gender-based marketing analysis.

### Discount Behavior

Customers who used discounts while spending above the average purchase amount were identified as **high-value discount users**, providing a potential target segment for personalized promotions.

### Product Performance

Products such as **Blouse, Dress, and Shirt** appeared among the highly rated products in the analysis.

### Shipping Behavior

Customers using **Express Shipping** had an average purchase amount of approximately **$65**, compared with approximately **$58** for Standard Shipping.

### Subscription Analysis

The analysis identified differences in spending, revenue contribution, and repeat purchasing behavior between subscribers and non-subscribers.

### Customer Segmentation

Customers were segmented into:

* **New Customers** – 50%
* **Returning Customers** – 35%
* **Loyal Customers** – 15%

This segmentation can help businesses design targeted retention and conversion strategies.

---

# 📑 Business Report

A structured business report was created to summarize the analytical findings and translate the data into business-oriented insights.

The report focuses on:

* Customer behavior
* Revenue drivers
* Product performance
* Subscription impact
* Customer segmentation
* Strategic opportunities

---

# 🎞️ Business Presentation

A professional presentation was created using **Gamma** to communicate the analysis and recommendations in a concise business format.

The presentation covers:

1. Dataset Overview
2. Data Preparation
3. Revenue Analysis
4. Discount Behavior
5. Product Ratings
6. Shipping Analysis
7. Subscription Impact
8. Customer Segmentation
9. Strategic Recommendations

---

# 💡 Business Recommendations

Based on the analysis, the project highlights opportunities to:

* **Increase subscription adoption** through exclusive customer benefits
* **Strengthen loyalty programs** to encourage repeat purchases
* **Use targeted marketing** for high-value customer segments
* **Promote highly rated products** in marketing campaigns
* **Focus on converting New Customers into Returning Customers and Returning Customers into Loyal Customers**

---

# 📁 Project Structure

```text
Customer-Shopping-Behavior-Analysis/
│
├── data/
│   └── customer_shopping_behavior.csv
│
├── python/
│   └── customer_shopping_behavior_analysis.ipynb
│
├── sql/
│   └── customer_behavior_sql_queries_business_insights.sql
│
├── powerbi/
│   └── customer_behavior_dashboard.pbix
│
├── report/
│   └── customer_behavior_report.pdf
│
├── presentation/
│   └── Customer-Shopping-Behavior-Analysis.pptx
│
└── README.md
```

---

# ▶️ How to Run

## 1. Clone the Repository

```bash
git clone <your-github-repository-url>
cd Customer-Shopping-Behavior-Analysis
```

## 2. Install Python Libraries

```bash
pip install pandas numpy matplotlib seaborn sqlalchemy psycopg2-binary jupyter
```

## 3. Run the Python Notebook

Open:

```text
python/customer_shopping_behavior_analysis.ipynb
```

Run the notebook to perform:

* Data loading
* EDA
* Data cleaning
* Feature engineering
* PostgreSQL data integration

## 4. Set Up PostgreSQL

1. Install PostgreSQL.
2. Create a database.
3. Configure the PostgreSQL connection.
4. Load the cleaned dataset into the database.
5. Execute the SQL queries provided in the `sql` folder.

## 5. Open Power BI

Open:

```text
powerbi/customer_behavior_dashboard.pbix
```

Refresh the data if required and explore the interactive dashboard.

## 6. View the Report & Presentation

Open the files in the `report` and `presentation` folders to review the final business findings and recommendations.

---

# 🚀 Skills Demonstrated

**Python • Pandas • Exploratory Data Analysis • Data Cleaning • Feature Engineering • SQL • PostgreSQL • Power BI • Data Visualization • Business Analysis • Customer Segmentation • Data Storytelling • Business Reporting**

---

## 👤 Author

**[Your Name]**

[GitHub](your-github-profile-link)
[LinkedIn](your-linkedin-profile-link)


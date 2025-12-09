Customer Shopping Behavior Analysis
📝 Overview

This project analyzes customer shopping behavior using a complete end-to-end data analytics workflow.
It includes Python-based data cleaning, SQL analysis in PostgreSQL, and an interactive Power BI dashboard.
The goal is to uncover insights that help improve sales strategy, customer segmentation, and retention.

📂 Dataset

The dataset contains 3,900 customer transactions with attributes such as:

Customer ID

Age, Gender

Item Purchased

Product Category

Purchase Amount (USD)

Review Rating

Color, Size

Season, Location

Previous Purchases

Payment Method

Subscription Status

🛠️ Tools & Technologies
Tool	Purpose
Python (Jupyter Notebook)	Data loading, EDA, cleaning, feature engineering
Pandas / NumPy	Data manipulation & preprocessing
PostgreSQL + pgAdmin	Database storage & SQL analysis
SQL	Analytical queries for insights
Power BI	Building interactive dashboard & KPIs
GitHub	Version control & documentation
🚀 Project Workflow
1️⃣ Data Loading (Python)

Imported dataset using pandas

Previewed structure: df.head(), df.info()

Checked and fixed missing values

Normalized column names

2️⃣ Exploratory Data Analysis

Performed:

Summary statistics

Value counts

Distribution checks

Outlier and missing value detection

3️⃣ Data Cleaning & Feature Engineering

Key steps:

Imputed missing review ratings

Converted column types

Created age_group using binning

Prepared cleaned DataFrame for SQL loading

4️⃣ Store Clean Data in PostgreSQL

Created database: customer_behavior

Created table: customer

Loaded cleaned data using SQLAlchemy

5️⃣ SQL Analysis (PostgreSQL / pgAdmin)

Queries answered:

✔️ Total revenue by gender
✔️ Customers using discounts vs. average spend
✔️ Top 5 products by review rating
✔️ Customer segmentation (New, Returning, Loyal)
✔️ Revenue contribution by age group
✔️ Purchase trends by category
✔️ Subscription vs. non-subscription behavior

Example query:

SELECT "Gender",
       SUM("Purchase Amount (USD)") AS revenue
FROM customer
GROUP BY "Gender";

6️⃣ Power BI Dashboard

Created KPIs:

Average Purchase Amount

Average Review Rating

Total Customers

Dashboard visuals included:

📌 Revenue by Category
📌 Sales by Category
📌 Subscription Status Breakdown
📌 Sales by Age Group
📌 Top Product Performance

(Insert dashboard screenshot here)

⭐ Key Insights

Average customer spend is ≈ $59.76

Average rating is 3.75

Adults & Middle-aged customers contribute the most revenue

Subscribers spend more than non-subscribers

Discount users still maintain high spending

Top-rated items align strongly with high sales

▶️ How to Run This Project
1. Clone the Repository
git clone https://github.com/yourusername/customer-shopping-behavior-analysis.git

2. Install Python Requirements
pip install pandas numpy sqlalchemy psycopg2

3. Open Jupyter Notebook
jupyter notebook

4. Set Up PostgreSQL

Create database customer_behavior

Update credentials in notebook

Run all SQL queries in pgAdmin

5. Open Power BI Dashboard

Load dashboard.pbix using Power BI Desktop

📎 Project Structure
├── data/
│   └── customer_shopping_behavior.csv
├── notebooks/
│   └── Customer_Shopping_Behavior_Analysis.ipynb
├── sql/
│   └── customer_queries.sql
├── dashboard/
│   └── powerbi_dashboard.pbix
├── README.md

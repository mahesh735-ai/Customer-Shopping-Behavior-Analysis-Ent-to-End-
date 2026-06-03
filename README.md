# Customer-Shopping-Behavior-Analysis-Ent-to-End-
🛍️ Analyzed 3,900 customer transactions using Python, PostgreSQL, and Power BI to uncover customer behavior, spending patterns, product preferences, and subscription trends. 🔍 Conducted data cleaning, feature engineering, and SQL-based business analysis, then 📊 developed an interactive Power BI dashboard to drive data-informed retail decisions. 
# 🛍️ Customer Shopping Behavior Analysis

> An end-to-end Data Analytics project analyzing 3,900 customer transactions to uncover insights on spending patterns, product preferences, and subscription behavior.

---

## 📌 Project Overview

A leading retail company wanted to better understand its customers' shopping behavior to improve **sales**, **customer satisfaction**, and **long-term loyalty**.

**Business Question:**
> *How can the company leverage customer shopping data to identify trends, improve customer engagement, and optimize marketing and product strategies?*

---
![Power BI Dashboard](https://github.com/mahesh735-ai/Customer-Shopping-Behavior-Analysis-Ent-to-End-/blob/main/Dashboard_Screenshot.png?raw=true)

## 🗂️ Project Structure

```
customer-behavior-analysis/
│
├── 📓 Customer_Behavior_analysis.ipynb     # Python EDA & Data Cleaning
├── 🗄️ Customer_behavior_project.sql        # PostgreSQL Business Queries
├── 📊 Customer_Behavior_Dashboard.pbix     # Power BI Interactive Dashboard
├── 📄 Customer_Shopping_Behavior_Analysis.pdf   # Project Report
├── 📑 Customer-Shopping-Behavior-Analysis.pptx  # Presentation Deck
├── 🗃️ customer_shopping_behavior.csv       # Raw Dataset
└── 📘 README.md
```

---

## 🛠️ Tools & Technologies

| Tool | Purpose |
|------|---------|
| **Python (Pandas)** | Data cleaning, EDA, Feature Engineering |
| **PostgreSQL** | Business SQL queries & advanced analysis |
| **Power BI** | Interactive dashboard & KPI visualization |
| **SQLAlchemy** | Python → PostgreSQL connection |
| **Jupyter Notebook** | Development environment |

---

## 📊 Dataset Summary

- **Rows:** 3,900 customer records  
- **Columns:** 18 features  
- **Key Features:** Customer demographics, purchase details, shopping behavior  
- **Missing Data:** 37 null values in `review_rating` (handled with category-wise median imputation)

---

## 🐍 Section 1 — Python: EDA & Data Cleaning

### Steps Performed:
1. **Data Loading** — Imported CSV using `pandas`
2. **Initial Exploration** — `df.info()`, `df.describe(include='all')`, `df.isnull().sum()`
3. **Smart Imputation** — Filled missing `review_rating` with **category-wise median** (not global median)
4. **Column Standardization** — Renamed all columns to `snake_case`
5. **Feature Engineering:**
   - `age_group` — Created 4 segments using `pd.qcut()` (Young Adult, Adult, Middle-aged, Senior)
   - `purchase_frequency_days` — Converted text frequency to numeric days using `.map()`
6. **Redundancy Check** — Verified `discount_applied == promo_code_used` → dropped `promo_code_used`
7. **Database Export** — Loaded cleaned DataFrame to PostgreSQL via `SQLAlchemy`


---

## 🗄️ Section 2 — PostgreSQL: Business Queries

### Business Questions Answered:

| # | Question | SQL Concept |
|---|----------|-------------|
| Q1 | Revenue by Gender | `GROUP BY + SUM` |
| Q2 | High-spend discount users | Subquery |
| Q3 | Top 5 products by rating | `AVG + ROUND + LIMIT` |
| Q4 | Standard vs Express shipping spend | `WHERE IN + GROUP BY` |
| Q5 | Subscriber vs Non-subscriber revenue | `COUNT + AVG + SUM` |
| Q6 | Products with highest discount rate | `CASE WHEN + percentage calc` |
| Q7 | Customer segmentation (New/Returning/Loyal) | `CTE + CASE WHEN` |
| Q8 | Top 3 products per category | `CTE + ROW_NUMBER() OVER (PARTITION BY)` |
| Q9 | Repeat buyers & subscription rate | `WHERE filter + GROUP BY` |
| Q10 | Revenue by age group | `GROUP BY + SUM` |


---

## 📊 Section 3 — Power BI Dashboard

### Dashboard Features:
- **3 KPI Cards** — Total Customers, Avg Purchase Amount, Avg Review Rating
- **Donut Chart** — % of Customers by Subscription Status
- **Column Charts** — Revenue & Sales by Category
- **Bar Charts** — Revenue & Sales by Age Group
- **Interactive Slicers** — Filter by Subscription Status, Gender, Category, Shipping Type
---

## 💡 Key Business Insights

1. **Clothing dominates** — Highest revenue ($104K) and sales volume (1,737 units)
2. **Young Adults are top spenders** — Generate maximum revenue ($62K); prime marketing target
3. **Subscription gap** — Only **27%** customers subscribed; massive growth opportunity
4. **Outerwear underperforms** — Lowest revenue ($19K) and sales (324 units); needs attention
5. **Express shipping = higher spend** — Express customers spend ~3.5% more than Standard
6. **Loyal customers dominate** — 3,116 out of 3,900 customers are loyal; retention is strong
7. **Repeat buyers not subscribing** — 2,518 repeat buyers are unsubscribed; subscription offer needs improvement

---

## 📋 Business Recommendations

- 🎯 **Boost Subscriptions** — Introduce exclusive subscriber-only discounts and early access
- 🏆 **Loyalty Rewards** — Create a tiered loyalty program to retain and upsell loyal customers
- 🚀 **Express Shipping Push** — Promote express delivery; high-spend customers prefer it
- 📦 **Outerwear Strategy** — Run targeted discount campaigns or reconsider inventory allocation
- 👥 **Youth Marketing** — Focus campaigns on Young Adults (18–35) for maximum revenue impact

---

## 🚀 How to Run This Project

### 1. Python (Jupyter Notebook)
```bash
pip install pandas sqlalchemy psycopg2
jupyter notebook Customer_Behavior_analysis.ipynb
```

### 2. PostgreSQL
```sql
-- Create database
CREATE DATABASE customer_behavior;
-- Then run: Customer_behavior_project.sql
```

### 3. Power BI
- Open `Customer_Behavior_Dashboard.pbix` in Power BI Desktop
- Update PostgreSQL connection credentials if needed

---

## 📁 How to Add Screenshots

1. Create a `screenshots/` folder in your repo
2. Upload your screenshots with these names:
   - `python_eda.png`
   - `sql_queries.png`
   - `powerbi_dashboard.png`
3. The images will automatically appear in this README

---

## 👤 Author

**Mahesh Thakare**
- 📧 Connect on [LinkedIn](www.linkedin.com/in/mahesh-thakare-75817b2a7
)
- 💻 GitHub: [github.com/](https://github.com/mahesh735-ai)

---

## 📄 License

MIT License — feel free to use and modify.

---
*Built with Python • PostgreSQL • Power BI*



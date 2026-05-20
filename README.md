# Customer_Behaviour_analysis_Project

<img width="500" height="290" alt="image" src="https://github.com/user-attachments/assets/209d015b-b3ce-4120-8a05-415a91793c1a" />

<img width="500" height="290" alt="image" src="https://github.com/user-attachments/assets/ee9c935e-31ca-4c25-95e6-118d3f74324b" />


# 🛒 Customer Behaviour Analysis

> A complete end-to-end data analysis project using **Python**, **SQL Server**, and **Power BI** on a retail e-commerce dataset to uncover purchase patterns, optimize marketing strategies, and increase customer lifetime value.

---

## 📌 Project Overview

| Field | Details |
|---|---|
| **Dataset** | Retail / E-commerce (Customer Transaction Level) |
| **Records** | ~5,000 Customers |
| **Tools Used** | Python · SQL Server · Power BI |
| **Goal** | Understand customer behavior to drive business decisions |

---

## ❓ Business Problem

> *How can a retail company understand customer purchasing behavior to increase revenue, improve retention, and optimize marketing?*

- 📉 Low customer retention — who are one-time vs. frequent buyers?
- 📣 Are discount campaigns actually effective?
- 🏷️ Which product categories and payment methods perform best?
- 👥 How to segment customers (New / Returning / Loyal)?

---

## 🔧 Tools & Technologies

```
Python      →  Data cleaning & EDA (pandas)
SQL Server  →  Business queries & analysis
Power BI    →  Interactive dashboards & visualization
```

---

## 🐍 Phase 1 — EDA with Python

### What I Did & Why

| Step | What | Why |
|---|---|---|
| **Data Loading** | `pd.read_csv()` | Bring raw data into structured DataFrame |
| **Data Exploration** | `df.info()`, `df.describe()`, `df.isnull().sum()` | Understand structure, types & missing values early |
| **Category Correction** | Mapping dictionary for Item ↔ Category | Categories were inconsistent — ensures accurate grouping |
| **Missing: Size** | Electronics→"Not Applicable", Clothing→mode | Different categories need different business logic |
| **Missing: Review Rating** | Product-level mean (not global avg) | Keeps ratings realistic — advanced imputation technique |
| **Missing: Purchase Amount** | Mean imputation | Maintains product-level pricing consistency |
| **Missing: Previous Purchases** | Filled with 0 | Missing = no prior purchase; critical for loyalty analysis |
| **Duplicate Removal** | Identified by Customer ID | Prevents double-counting in analysis |
| **Column Standardization** | `str.replace(" ","_")` + `str.lower()` | Makes columns SQL-friendly and BI-ready |
| **SQL Export** | `pyodbc` + `sqlalchemy` | Move clean data for advanced querying |

---

## 🗄️ Phase 2 — SQL Server Analysis

### Key Questions Answered

| # | Question | Key Finding |
|---|---|---|
| 1 | Which category generates highest revenue? | **Electronics — $378,785** |
| 2 | Do discounts increase purchase value? | Yes — Avg. $202.73 (discount) vs $167.16 (no discount) |
| 3 | Revenue by gender? | Male: $358K · Female: $304K · Other: $223K |
| 4 | Customers using discount but spending above average? | 10 customers identified |
| 5 | Top 5 products by review rating? | Gloves (3.86), Sandals (3.84), Boots (3.82) |
| 6 | Best shipping type by revenue? | Standard ($366K) · Express ($364K) |
| 7 | Do subscribers spend more? | Yes — $250.99 avg vs $152.33 non-subscribers |
| 8 | Top discount-used products? | Laptop (51.75%), Phone (51.46%) |
| 9 | Customer segmentation? | Loyal: 3,034 · Returning: 1,332 · New: 477 |
| 10 | Top products per category? | Shirt (Clothing) · Phone (Electronics) · Shoes (Footwear) |
| 11 | Repeat buyers likely to subscribe? | No — 70% repeat buyers are unsubscribed |
| 12 | Revenue by age group? | 51+ leads with $354,427 |

---

## 📊 Phase 3 — Power BI Dashboard

### Dashboard KPIs
```
Total Customers: 5K    |    Unique Items: 29    |    Avg Review: 3.63
Total Spend: $886.60K  |    Average Spend: $183.07
```

### Charts Built
- 🍩 Revenue by Gender (Donut)
- 📊 Revenue by Category (Bar)
- 🚚 Shipping Type Analysis (Bar)
- 🌦️ Revenue by Season (Column)
- 📍 Average Revenue by Location (Clustered Bar)
- 🎂 Revenue by Age Distribution (Donut)
- 💳 Revenue by Payment Method (Bar)
- ⭐ Top & Bottom 5 Items by Rating
- 💰 Top & Bottom 5 Items/Locations by Revenue

---

## 💡 Key Insights

- 🏆 **Electronics dominates** revenue — prioritize inventory & promotions
- 💳 **Subscribers spend 64% more** than non-subscribers
- 👴 **Age 51+** is the highest revenue-generating segment
- ❄️ **Winter, Summer & Spring** drive 73%+ of seasonal revenue
- 🎯 **Debit Card, Cash & Credit Card** are top payment preferences
- 🔁 **Loyal customers (3,034)** form the core customer base

---

## 📁 Project Structure

```
Customer-Behaviour-Analysis/
│
├── 📓 EDA_Python.ipynb          # Data cleaning & exploration
├── 📄 SQL_Queries.sql           # All 12 business queries
├── 📊 PowerBI_Dashboard.pbix    # Interactive dashboard
├── 📑 Final_Report.pdf          # Detailed project report
├── 📽️ Presentation.pdf          # Project presentation slides
└── 📋 README.md                 # You are here
```

---

## 🧠 What I Learned

- ✅ Real-world **data cleaning** requires domain knowledge, not just code
- ✅ **Category-specific imputation** is better than global statistics
- ✅ SQL is powerful for **business-oriented questions** on clean data
- ✅ Power BI dashboards make insights **accessible to non-technical** stakeholders
- ✅ End-to-end projects build **analytical thinking**, not just tool skills

## 👤 Author

**Aman Singh Rawat**  
📧 amanrawat7610@gmail.com  
🔗 [LinkedIn](linkedin.com/in/aman-singh-rawat-330803229)

--

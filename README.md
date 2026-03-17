# 💳 Credit Card Financial Dashboard — Power BI Project

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![CSV](https://img.shields.io/badge/Dataset-CSV-green?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge)

---

## 📌 Project Overview

This project presents an **end-to-end Credit Card Financial Analytics Dashboard** built using **Power BI**, backed by **SQL** for data preparation and **CSV datasets** for raw data ingestion. The dashboard provides deep insights into credit card customer behavior, transaction patterns, revenue streams, and demographic segmentation — enabling data-driven decisions for financial institutions.

The project is split into **two interactive reports**:
- 📊 **Credit Card Customer Report** — Focuses on customer demographics, income, and behavioral patterns.
- 💰 **Credit Card Transaction Report** — Focuses on transaction volumes, revenue by category, expenditure types, and acquisition costs.

---

## 🗂️ Repository Structure

```
credit-card-analysis/
│
├── 📄 Credit Card Analylis.pdf          # Exported PDF report of the dashboard
├── 📊 Credit Card Analysis.pbix         # Power BI project file
├── 🗃️ SQL Query - Financial Dashboard Data.sql  # SQL queries for data prep
├── 📁 cc_add.csv                        # Additional credit card data
├── 📁 credit_card.csv                   # Core credit card transactions dataset
├── 📁 cust_add.csv                      # Additional customer data
├── 📁 customer.csv                      # Core customer demographics dataset
└── 📄 README.md                         # Project documentation
```

---

## 📊 Dashboard 1 — Credit Card Customer Report

<img width="859" height="496" alt="Screenshot 2026-03-17 151200" src="https://github.com/user-attachments/assets/2ee7c8c7-eee6-4da4-ae44-09d023b03bac" />

> Analyzes **who** the customers are and **how** they behave.

### 🔢 Key KPIs
| Metric | Value |
|---|---|
| Average Customer Age | 46.3 |
| Customer Satisfaction Score (CSS) | 3.2 |
| Total Interest Earned | 7.8M |
| Total Income | 575.9M |

### 📈 Visuals Included
- **Revenue vs Gender** — Line chart showing weekly revenue trend split by gender (Male vs Female).
- **Age Group Distribution** — Bar chart segmenting customers into 20–30, 30–40, 40–50, 50–60, 60+ buckets.
- **Top 5 States** — Revenue comparison across TX, NY, CA, FL, NJ by gender.
- **Salary Group Analysis** — Revenue distribution across High, Mid, and Low income brackets.
- **Marital Status** — Revenue split for Married, Single, and Unknown categories.
- **Dependent Count** — Revenue by number of dependents (0–4).
- **Revenue by Customer Job** — Table with Sum of Revenue, Sum of Income, and Sum of Interest Earned per job category (Blue-collar, Businessman, Govt, Retirees, Self-employed, White-collar).
- **Card Category Split (F/M)** — Silver, Gold, Blue, Platinum breakdown.

### 🔍 Key Insights
- The **40–50 age group** generates the highest revenue (~11M–14M).
- **Married customers** account for the largest revenue share (~13M–15M).
- **TX and NY** are the top-performing states.
- **Businessmen** have the highest total interest earned (~2.5M), followed by **White-collar** (~1.4M).
- **High salary group** contributes significantly more revenue (~22M) vs Low (~10M).

---

## 💰 Dashboard 2 — Credit Card Transaction Report

<img width="883" height="516" alt="Screenshot 2026-03-17 151214" src="https://github.com/user-attachments/assets/72147cfa-c5cc-442f-81a7-99a9cac8384e" />

> Analyzes **what** customers are spending on and **how much** revenue is generated per segment.

### 🔢 Key KPIs
| Metric | Value |
|---|---|
| Total Transaction Amount | 44.5M |
| Total Revenue | 55.3M |
| Total Interest Earned | 7.8M |
| Total Transaction Count | 655.7K |

### 📈 Visuals Included
- **QTR Revenue & Total Transaction Count** — Combo bar + line chart showing quarterly trends (Q1–Q4).
- **Revenue by Expenditure Type** — Bills (14M), Entertainment (10M), Fuel (9M), Grocery (9M), Food (8M), Travel (6M).
- **Revenue by Education** — Graduate (22M), High School (11M), Unknown (8M), Uneducated (8M), Post-Graduate (3M), Doctorate (2M).
- **Revenue by Customer Job** — Businessman (17M) leads, followed by White-collar (10M).
- **Revenue by Use Chip** — Swipe (35M) vs Chip (17M) vs Online (3M).
- **Customer Acquisition Cost by Card** — Blue (46M), Silver (6M), Gold (2M), Platinum (1M).
- **Card Category Revenue Table** — Platinum, Gold, Silver, Blue breakdown of Revenue, Transaction Amount, and Interest Earned.

### 🔍 Key Insights
- **Q3** had the highest revenue (~14.2M) and transaction count (~166.6K).
- **Swipe** is the dominant payment method, accounting for ~64% of revenue.
- **Blue card** has the highest customer acquisition cost (~46M) but also the highest revenue base.
- **Bills** are the top expenditure category, suggesting most cardholders use credit for essential expenses.
- **Graduate-educated** customers generate the most revenue (~22M).

---

## 🗄️ Data Sources

| File | Description |
|---|---|
| `credit_card.csv` | Core transaction-level data — card type, transaction amount, fees, interest |
| `customer.csv` | Customer demographics — age, gender, income, job, education, marital status |
| `cc_add.csv` | Supplementary credit card data (weekly/incremental updates) |
| `cust_add.csv` | Supplementary customer records (weekly/incremental updates) |

---

## 🛠️ Tools & Technologies

| Tool | Purpose |
|---|---|
| **Power BI Desktop** | Dashboard creation, DAX measures, data modeling |
| **SQL (MySQL / PostgreSQL)** | Data extraction, transformation, and loading (ETL) |
| **CSV Files** | Raw data storage and ingestion |
| **DAX** | Custom measures and calculated columns in Power BI |

---

## ⚙️ SQL Workflow

The file `SQL Query - Financial Dashboard Data.sql` handles:
1. **Database & Table Creation** — Defining schema for credit card and customer tables.
2. **Data Import** — Loading CSV data into SQL tables.
3. **Incremental Data Load** — Inserting weekly/additional data from `cc_add.csv` and `cust_add.csv`.
4. **Pre-processing** — Aggregations and joins used as a foundation before Power BI import.

---

## 📐 Data Model (Power BI)

The Power BI data model follows a **Star Schema** design:
- **Fact Table:** `credit_card` (transactions)
- **Dimension Table:** `customer` (demographics)
- **Relationship:** Joined on `client_num` (Customer ID)

---

## 🚀 How to Run This Project

### Prerequisites
- Power BI Desktop (latest version)
- MySQL / PostgreSQL (optional, for SQL setup)

### Steps
1. **Clone this repository**
   ```bash
   git clone https://github.com/your-username/credit-card-analysis.git
   cd credit-card-analysis
   ```

2. **Set up the database** *(optional)*
   - Open `SQL Query - Financial Dashboard Data.sql` in your SQL client.
   - Run the script to create tables and load CSV data.

3. **Open Power BI**
   - Launch `Credit Card Analysis.pbix` in Power BI Desktop.
   - If needed, update the data source path to point to your local CSV files.
   - Click **Refresh** to load data.

4. **Explore the Dashboards**
   - Use the **quarter filters** (Q1–Q4) and **date range slicer** to explore trends.
   - Use the **gender**, **card category**, and other slicers for deeper segmentation.

---

## 📅 Filters & Interactivity

Both dashboards support:
- 📆 **Date Range Slicer** — Filter by specific date ranges (Jan 2023 – Dec 2023).
- 📊 **Quarter Toggle** — Q1, Q2, Q3, Q4 buttons for quarterly drill-down.
- 👤 **Gender Filter** — F / M toggle.
- 💳 **Card Category Filter** — Silver, Blue, Gold, Platinum.

---

## 📌 Business Use Cases

- **Risk Assessment** — Identify high-interest, high-debt customer segments.
- **Customer Segmentation** — Target marketing based on job, education, and income.
- **Revenue Optimization** — Focus on high-revenue states, card categories, and expenditure types.
- **Churn Prevention** — Monitor satisfaction scores and usage patterns.
- **Product Strategy** — Evaluate card category performance (Blue vs Platinum, etc.).

---

## 🙋 Author

**Your Name**
- 🔗 [LinkedIn](https://linkedin.com/in/your-profile)
- 💻 [GitHub](https://github.com/your-username)
- 📧 your.email@example.com

---

## 📃 License

This project is licensed under the **MIT License** — feel free to use, modify, and distribute with attribution.

---

> ⭐ If you found this project helpful, please consider giving it a star on GitHub!

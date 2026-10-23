# 🛍️ IKEA Gifting: Customer Analytics & RFM Segmentation

*An end-to-end data analytics project using SQL, Python, and Power BI.*

---

## ⚠️ Disclaimer

**IKEA Gifting** is a fictional company created for this educational analytics project. It is not affiliated with, endorsed by, or representative of the real IKEA corporation.

All financial figures, customer counts, and business metrics presented in this project are derived from a public, anonymized transactional dataset and do not reflect IKEA's actual business performance. Any IKEA-inspired visual branding used in the dashboard is for illustrative and storytelling purposes only.

---

## 📌 Project Overview

This project simulates a real-world analytics engagement for a fictional UK-based gifting and home decor e-commerce business, **IKEA Gifting**.

The objective is to transform raw transactional data into a decision-ready business intelligence solution using an end-to-end data analytics workflow. The project combines SQL for data cleaning and validation, Python for customer analytics and segmentation, and Power BI for interactive visualization and reporting.

The analysis focuses on understanding customer value, identifying customers at risk of becoming inactive, evaluating purchasing patterns, and developing actionable recommendations to improve customer retention.

The project follows a business-first approach, connecting technical analysis to practical business questions and measurable outcomes.

---

## 🧠 Analytical Approach

The project begins by defining the business problem and establishing clear analytical requirements before working with the data.

Rather than focusing solely on technical implementation, the workflow connects each stage of the analysis to specific business questions. Data quality issues are investigated and addressed before customer metrics are calculated, helping ensure that the resulting insights are meaningful and reliable.

The Online Retail II dataset provides an opportunity to work with real-world transactional data containing challenges such as inconsistent date formats, duplicate transactions, invalid values, and missing customer identifiers.

---

## 🎯 Business Problem

The business wants to identify its most valuable customers and reduce customer churn by recognizing customers who may be at risk of leaving.

Without a structured view of customer value and purchasing behavior, retention efforts can become reactive rather than targeted.

The goal is to develop a data-driven customer analytics framework that helps the business understand customer segments, evaluate revenue contribution, identify inactivity patterns, and make informed customer engagement decisions.

## ❓ Business Questions

* 👥 Who are the most valuable customers, and how much revenue do they contribute?
* ⚠️ Which customers have become inactive and may be at risk of churning?
* 📅 How do customer value and retention trends change across months, quarters, and years?
* 🌍 How does customer value and churn vary across geographic markets?
* 💰 Which customer segments contribute the greatest share of revenue?
* 🎯 What targeted actions can help improve customer engagement and retention?
* 📊 How can customer analytics support better business decisions?

---

## 🔍 Key Findings

The analysis highlights several important patterns in customer value, inactivity, and revenue performance.

* 🏆 **Customer Value Concentration:** Champions account for approximately **22% of customers while contributing close to 68% of total revenue**, highlighting the importance of high-value customer relationships.
* ⚠️ **Customer Churn:** The observed churn rate is approximately **50.86%**, using a 90-day inactivity threshold.
* 💎 **Customer Value Differences:** Average customer value varies considerably across segments, with Champions contributing substantially more monetary value than Lost customers.
* 🎁 **Seasonal Revenue Trends:** Revenue shows noticeable peaks during the fourth quarter, consistent with seasonal purchasing patterns often associated with gifting products.

These findings illustrate the potential value of customer segmentation and retention analysis in understanding business performance.

---

## 📂 Data Source

**Dataset:** Online Retail II
**Source:** UCI Machine Learning Repository
**Original Contributor:** Daqing Chen
**Period Covered:** December 2009 – December 2011
**Dataset Size:** Approximately 1,067,371 raw transaction records across two sheets
**License:** Creative Commons Attribution 4.0 International, as specified by the dataset source.

The Online Retail II dataset contains anonymized transactional data from a UK-based, non-store online retailer selling giftware and other products for various occasions.

It includes transaction-level information that supports customer behavior analysis, sales performance evaluation, and customer segmentation.

🔗 **Dataset:** https://archive.ics.uci.edu/dataset/502/online+retail+ii

---

## 🛠️ Tools & Technologies

| Tool                  | Purpose                                                                                                                     |
| --------------------- | --------------------------------------------------------------------------------------------------------------------------- |
| 🗄️ SQL Server / SSMS | Data import, cleaning, deduplication, validation, and exploratory querying across more than one million transaction records |
| 🐍 Python             | RFM calculations, customer scoring, segmentation, and churn flagging                                                        |
| 🧮 Pandas             | Data manipulation, transformation, and analytical calculations                                                              |
| 📓 Jupyter Notebook   | Interactive Python development and analysis                                                                                 |
| 📊 Power BI Desktop   | Interactive dashboards and business intelligence reporting                                                                  |
| 📐 DAX                | Measures for customer counts, revenue totals, churn percentage, and average customer value                                  |

---

## 💡 Core Concepts Demonstrated

### 1. 📈 RFM Analysis

RFM analysis evaluates customers using three dimensions:

* **Recency:** How recently a customer made a purchase.
* **Frequency:** How often a customer makes purchases.
* **Monetary Value:** How much a customer spends.

These metrics help quantify customer value and compare purchasing behavior across different customer groups.

### 2. 👥 Customer Segmentation

Customers are grouped into meaningful segments based on their RFM scores.

The six segments used in this analysis are:

* 🏆 Champions
* 💎 Loyal Customers
* ⚠️ At Risk
* 🆕 New Customers
* 🔔 Needs Attention
* 💤 Lost Customers

This segmentation helps distinguish high-value customers from customers who may require additional engagement.

### 3. 🚨 Churn Definition and Flagging

A fixed inactivity threshold is applied to identify customers who have not purchased within the selected period.

A 90-day threshold is used to flag potentially inactive customers and investigate possible retention opportunities.

### 4. 🧹 Data Quality Management

The data preparation process addresses several real-world data quality challenges, including:

* Mixed date formats
* Invalid data type conversions
* Duplicate transactions
* Missing customer identifiers
* Data validation and consistency checks

SQL techniques, including window functions and conversion functions, support data cleaning and validation.

### 5. 🏗️ Business Intelligence Data Modeling

A unified analytical dataset connects transaction-level information with customer segmentation results, enabling consistent reporting across multiple Power BI dashboard pages.

### 6. 🎨 Interactive Dashboard Design

Power BI features such as slicers, bookmarks, interactive filters, and multi-page navigation make it easier to explore customer segments, revenue trends, and business performance.

---

## 🔄 Project Workflow

### Step 1: 📋 Business Requirements Document

Defined the business problem, project scope, key business questions, analytical definitions, and success criteria before beginning the data analysis.

### Step 2: 🗄️ SQL — Data Cleaning & Exploration

* Imported both raw dataset sheets into SQL Server.
* Inspected the source data and corrected data types.
* Investigated mixed date formats affecting a substantial portion of the dataset.
* Standardized dates using SQL conversion functions.
* Identified and removed **32,907 exact duplicate rows**.
* Examined missing customer identifiers and invalid values.
* Validated row counts and data consistency throughout the cleaning process.

### Step 3: 🐍 Python — RFM Analysis & Customer Segmentation

* Loaded the cleaned transactional data into Pandas.
* Calculated Recency, Frequency, and Monetary value for each customer.
* Assigned RFM scores on a scale of 1 to 5 for each dimension.
* Classified **5,881 customers into six customer segments**.
* Applied a 90-day inactivity threshold to flag potentially churned customers.
* Prepared customer-level analytical outputs for business intelligence reporting.

### Step 4: 📊 Power BI — Dashboard Development

* Combined customer segmentation results with transaction-level data.
* Prepared a unified dataset for dashboard reporting.
* Developed a three-page interactive Power BI report.
* Created measures for revenue, customer counts, churn percentage, and average customer value.
* Added filters, navigation, and interactive visual elements to support business exploration.

---

## 📊 Dashboard Structure

### 🏠 Page 1 — Home

Provides an introduction to the project and navigation to the main report pages.

Includes a glossary explaining key concepts such as Recency, Frequency, Monetary Value, and Churn Percentage.

### 📈 Page 2 — Business Overview

Provides a high-level view of customer and revenue performance.

**Key Performance Indicators:**

* Total Customers
* Total Revenue
* Churn Percentage
* Average Customer Value

**Visualizations and Features:**

* Revenue and customer view toggle
* Customer segment breakdowns
* Revenue contribution by segment
* Monthly, quarterly, and yearly trends
* Interactive filtering by date, country, customer segment, and churn status

### 🎯 Page 3 — RFM Analysis

Focuses on customer value and segment-level performance.

**Key Visualizations:**

* Customer count by segment
* Revenue contribution by segment
* Average Recency, Frequency, and Monetary scores
* Average customer value by segment
* Customer churn percentage trends over time

The dashboard enables users to explore customer segments and understand how purchasing behavior and customer value differ across groups.

---

## 💻 Sample SQL: Handling Mixed Date Formats

The following SQL example demonstrates how to standardize dates stored in different formats using SQL Server conversion functions.

```sql
SELECT
    Invoice,
    StockCode,
    Description,
    Quantity,
    COALESCE(
        TRY_CONVERT(datetime2, InvoiceDate, 120),
        TRY_CONVERT(datetime2, InvoiceDate, 105)
    ) AS InvoiceDate,
    TRY_CONVERT(decimal(10,2), Price) AS Price,
    Customer_ID,
    Country
INTO dbo.RetailCombined
FROM dbo.[Year 2009-2010];
```

**How it works:**

* `TRY_CONVERT()` attempts to convert the date using the specified format.
* Style `120` supports the `yyyy-mm-dd hh:mi:ss` format.
* Style `105` supports the `dd-mm-yyyy` date format.
* `COALESCE()` returns the first successful conversion.
* `TRY_CONVERT()` returns `NULL` when a value cannot be converted.

This approach helps standardize inconsistent date values before further analysis. The query assumes the source column names and data types match the database schema.

---

## 🐍 Sample Python: RFM Scoring

The following Python code demonstrates quintile-based scoring for Recency, Frequency, and Monetary value.

```python
rfm['R_Score'] = pd.qcut(
    rfm['Recency'],
    5,
    labels=[5, 4, 3, 2, 1]
).astype(int)

rfm['F_Score'] = pd.qcut(
    rfm['Frequency'].rank(method='first'),
    5,
    labels=[1, 2, 3, 4, 5]
).astype(int)

rfm['M_Score'] = pd.qcut(
    rfm['Monetary'],
    5,
    labels=[1, 2, 3, 4, 5]
).astype(int)
```

**Scoring logic:**

* **Recency:** Customers who purchased more recently receive higher scores.
* **Frequency:** Customers who purchase more frequently receive higher scores.
* **Monetary:** Customers who spend more receive higher scores.

The resulting scores provide a consistent framework for evaluating customers and assigning them to relevant segments.
---

## 🎯 Business Value & Recommendations

The analysis provides a framework for translating customer data into practical business decisions.

Potential applications include:

* **🏆 Retain High-Value Customers:** Identify Champions and Loyal Customers and explore strategies to strengthen long-term relationships.
* **⚠️ Re-engage At-Risk Customers:** Use inactivity indicators to identify customers who may benefit from targeted engagement.
* **💎 Improve Customer Value:** Examine purchasing behavior across segments to identify opportunities for repeat purchases and increased spending.
* **📅 Understand Seasonality:** Use historical revenue patterns to support promotional planning and inventory decisions.
* **🌍 Evaluate Geographic Markets:** Compare customer value and revenue performance across countries.
* **📊 Enable Data-Driven Decisions:** Use interactive dashboards to monitor performance and communicate findings clearly.

These recommendations should be interpreted in conjunction with the validated analytical results and the limitations of the dataset.

---

## 🧠 Skills Demonstrated

* SQL querying and data transformation
* Data cleaning and quality validation
* Python and Pandas
* Exploratory Data Analysis (EDA)
* RFM analysis and customer segmentation
* Customer inactivity and churn analysis
* Data modeling for business intelligence
* Power BI dashboard development
* DAX measures and KPI reporting
* Business problem-solving and analytical storytelling

---

## ⚠️ Final Disclaimer

This is an independent educational analytics project based on public, anonymized retail transaction data. IKEA Gifting is a fictional business concept created for analytical storytelling. The findings do not represent the actual operations, financial performance, customers, or business decisions of IKEA.

---


# 📊 Retail Customer Analytics & RFM Segmentation

*An end-to-end data analytics project using SQL, Python, and Power BI.*

---
## 📌 Project Overview

This project explores customer analytics for an e-commerce retail business, focusing on customer value, purchasing behavior, revenue contribution, and customer retention.

The objective is to transform raw transactional data into actionable business insights through an end-to-end data analytics workflow. The project combines SQL for data cleaning and validation, Python for customer analytics and segmentation, and Power BI for interactive business intelligence reporting.

By applying Recency, Frequency, and Monetary (RFM) analysis, the project investigates customer purchasing patterns, identifies high-value customer segments, and highlights customers who may be at risk of becoming inactive.

The final objective is to support data-driven decision-making through analytical findings, customer segmentation, and interactive dashboards.

---

## 🎯 Business Problem

Retail businesses need to understand which customers contribute the most value and which customers may be at risk of disengaging.

Without structured customer analytics, businesses may struggle to prioritize retention efforts, identify purchasing trends, and develop effective customer engagement strategies.

This project uses transactional data to evaluate customer value, analyze purchasing behavior, investigate customer inactivity, and identify opportunities for improving customer retention.

## ❓ Business Questions

* 👥 Who are the most valuable customers, and how much revenue do they contribute?
* ⚠️ Which customers may be at risk of becoming inactive?
* 📅 How do customer value and purchasing patterns change over time?
* 🌍 How does customer value vary across geographic markets?
* 💰 Which customer segments contribute the greatest share of revenue?
* 🎯 What strategies could improve customer engagement and retention?
* 📊 How can interactive dashboards help communicate business performance?

---

## 🔍 Key Findings

The analysis investigates customer value, revenue concentration, inactivity, and seasonal purchasing patterns.

* 🏆 **Customer Value Concentration:** Champions account for approximately 22% of customers and contribute close to 68% of total revenue.
* ⚠️ **Customer Inactivity:** The observed churn rate is approximately 50.86%, using a 90-day inactivity threshold.
* 💎 **Customer Value Differences:** Average monetary value varies across customer segments, highlighting differences in purchasing behavior.
* 🎁 **Seasonal Revenue Patterns:** Revenue shows noticeable peaks during the fourth quarter, suggesting seasonal variation in purchasing activity.

These findings are based on the selected dataset and analytical definitions used in the project.

---

## 📂 Data Source

**Dataset:** Online Retail II
**Source:** UCI Machine Learning Repository
**Original Contributor:** Daqing Chen
**Period Covered:** December 2009 – December 2011
**Dataset Size:** Approximately 1,067,371 raw transaction records across two sheets
**License:** Creative Commons Attribution 4.0 International, as specified by the dataset source.

The dataset contains anonymized transactional records from a UK-based, non-store online retailer selling giftware and other products for various occasions.

It provides transaction-level information that can be used to investigate customer behavior, product sales, revenue patterns, and customer value.

🔗 **Dataset:** https://archive.ics.uci.edu/dataset/502/online+retail+ii

---

## 🛠️ Tools & Technologies

| Tool                  | Purpose                                                                             |
| --------------------- | ----------------------------------------------------------------------------------- |
| 🗄️ SQL Server / SSMS | Data import, cleaning, deduplication, validation, and exploratory querying          |
| 🐍 Python             | RFM calculations, customer scoring, segmentation, and inactivity analysis           |
| 🧮 Pandas             | Data manipulation and analytical transformations                                    |
| 📓 Jupyter Notebook   | Interactive Python development and analysis                                         |
| 📊 Power BI Desktop   | Interactive dashboards and business intelligence reporting                          |
| 📐 DAX                | Measures for customer counts, revenue, churn percentage, and average customer value |

---

## 💡 Core Concepts Demonstrated

### 1. 📈 RFM Analysis

RFM analysis evaluates customers using three dimensions:

* **Recency:** How recently a customer made a purchase.
* **Frequency:** How often a customer makes purchases.
* **Monetary Value:** How much a customer spends.

These metrics help compare customer purchasing behavior and understand relative customer value.

### 2. 👥 Customer Segmentation

Customers are grouped into meaningful categories based on their RFM scores.

The six segments analyzed are:

* 🏆 Champions
* 💎 Loyal Customers
* ⚠️ At Risk
* 🆕 New Customers
* 🔔 Needs Attention
* 💤 Lost Customers

This approach helps distinguish high-value customers from customers who may require additional engagement.

### 3. 🚨 Customer Inactivity and Churn

A 90-day inactivity threshold is used to flag customers who have not purchased within the selected period.

This provides an analytical indicator of potential customer disengagement and helps identify possible retention opportunities.

Inactivity is a proxy for potential churn and does not necessarily mean that a customer has permanently left.

### 4. 🧹 Data Cleaning and Quality Management

The data preparation process addresses real-world data quality challenges, including:

* Mixed date formats
* Invalid data type conversions
* Duplicate transactions
* Missing customer identifiers
* Data consistency and validation

SQL conversion functions, conditional logic, and window functions support data cleaning and quality checks.

### 5. 🏗️ Data Preparation for Business Intelligence

Transaction-level data and customer-level segmentation results are combined into an analysis-ready dataset to support consistent reporting across multiple dashboard pages.

### 6. 🎨 Interactive Dashboard Design

Power BI features such as slicers, bookmarks, interactive filters, and multi-page navigation enable users to explore customer segments, revenue trends, and business performance.

---

## 🔄 Project Workflow

### Step 1: 📋 Business Requirements

Defined the business problem, project scope, key business questions, analytical definitions, and success criteria before beginning the technical analysis.

### Step 2: 🗄️ SQL — Data Cleaning and Exploration

* Imported both raw dataset sheets into SQL Server.
* Inspected the source data and corrected data types.
* Investigated inconsistent date formats affecting a substantial portion of the dataset.
* Standardized dates using SQL conversion functions.
* Identified and removed 32,907 exact duplicate rows.
* Examined missing customer identifiers and invalid values.
* Validated row counts and data consistency throughout the cleaning process.

### Step 3: 🐍 Python — RFM Analysis and Customer Segmentation

* Loaded the cleaned transactional data into Pandas.
* Calculated Recency, Frequency, and Monetary value for each customer.
* Assigned scores from 1 to 5 for each RFM dimension.
* Classified 5,881 customers into six customer segments.
* Applied a 90-day inactivity threshold to flag potentially churned customers.
* Prepared customer-level analytical outputs for reporting.

### Step 4: 📊 Power BI — Dashboard Development

* Combined customer segmentation results with transaction-level data.
* Prepared a unified dataset for reporting.
* Developed a three-page interactive Power BI dashboard.
* Created measures for revenue, customer counts, churn percentage, and average customer value.
* Added filters, navigation, and interactive visualizations to support business analysis.

---

## 📊 Dashboard Structure

### 🏠 Page 1 — Home

Introduces the project and provides navigation to the main dashboard pages.

Includes a glossary explaining Recency, Frequency, Monetary Value, and Churn Percentage.

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
* Interactive filtering by date, country, segment, and churn status

### 🎯 Page 3 — RFM Analysis

Focuses on customer segmentation and relative customer value.

**Key Visualizations:**

* Customer count by segment
* Revenue contribution by segment
* Average RFM scores
* Average customer value by segment
* Customer inactivity trends over time

---

## 💻 Sample SQL: Handling Mixed Date Formats

The following example demonstrates how to standardize dates stored in different formats using SQL Server conversion functions.

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

**Explanation:**

* `TRY_CONVERT()` attempts to convert a value using the specified format.
* Style `120` supports the `yyyy-mm-dd hh:mi:ss` format.
* Style `105` supports the `dd-mm-yyyy` format.
* `COALESCE()` returns the first successful conversion.
* `TRY_CONVERT()` returns `NULL` if conversion fails.

This approach helps standardize inconsistent date values before further analysis. The query assumes that the source table and column names match the database schema.

---

## 🐍 Sample Python: RFM Scoring

The following example demonstrates quintile-based scoring for Recency, Frequency, and Monetary value.

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
* **Frequency:** Customers who purchase more frequently generally receive higher scores.
* **Monetary:** Customers who spend more generally receive higher scores.

The resulting scores provide a framework for comparing customer value and assigning customers to relevant segments.

---

## 🎯 Business Value and Recommendations

The analysis provides a framework for translating customer data into practical business decisions.

* 🏆 **Retain High-Value Customers:** Identify Champions and Loyal Customers and explore strategies to strengthen long-term relationships.
* ⚠️ **Re-engage At-Risk Customers:** Use inactivity indicators to identify customers who may benefit from targeted engagement.
* 💎 **Improve Customer Value:** Examine purchasing behavior across segments to identify opportunities for repeat purchases and increased spending.
* 📅 **Understand Seasonality:** Use historical revenue patterns to support promotional planning and inventory decisions.
* 🌍 **Evaluate Geographic Markets:** Compare customer value and revenue performance across countries.
* 📊 **Support Data-Driven Decisions:** Use interactive dashboards to monitor performance and communicate findings clearly.

Recommendations should be interpreted in conjunction with the analytical results and the limitations of the dataset.

---

## 🧠 Skills Demonstrated

* SQL querying and data transformation
* Data cleaning and quality validation
* Python and Pandas
* Exploratory Data Analysis (EDA)
* RFM analysis and customer segmentation
* Customer inactivity and churn analysis
* Data preparation for business intelligence
* Power BI dashboard development
* DAX measures and KPI reporting
* Business problem-solving and analytical storytelling

---

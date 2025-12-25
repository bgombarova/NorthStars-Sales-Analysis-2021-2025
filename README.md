# Ecommerce_Analytics_SQL_PowerBI_Excel
---

<table width="90%" align="center">
<tr><td>

### **Abstract / Executive Summary**

This project presents an end-to-end analytics study of a **US-based ecommerce company** operating in the consumer retail domain. The dataset contains multi-year transactional, customer, fulfillment, and behavioral records used to evaluate business performance across revenue trends, order volume, profitability, discount impact, returns, delivery performance, and customer engagement.

The company serves a nationwide customer base and processes sales activity across multiple product categories and channels. The dataset includes approximately:

- **50,00+ unique customers**
- **220,000+ historical transactions**
- **$281M+ in recorded sales revenue**
- **Multiple sales and fulfillment channels**
- **Delivery time, returns, discounting & behavioral attributes**

A structured data engineering and analytics workflow was applied using:

- **SQL Server** — data ingestion, staging, transformation, and analytical queries  
- **Excel** — tabular validation, KPI summaries, and heatmap analysis  
- **Tableau** — visual analytics and executive insight storytelling  

The research focuses on deriving actionable insights across:

- revenue and order performance trends  
- product profitability and category contribution  
- discount effectiveness and AOV impact  
- return behavior and financial loss exposure  
- delivery speed and logistics performance  
- customer behavior, frequency, and retention risk  

Insights from this study are intended to support business leaders and operational teams in strategic planning, commercial decision-making, and performance optimization across the ecommerce lifecycle.

</td></tr>
</table>

---


<table width="90%" align="center">
<tr><td>

### **Background and Problem Context**

The dataset represents operations from a **Ecommerce Retail Company** that sells consumer products across multiple categories and fulfillment channels. Over recent years, the company has experienced rapid digital growth, increasing competition from peer retailers, evolving customer purchasing behavior, and operational challenges related to delivery performance and returns.

The business operates at national scale, serving a large and diverse customer base characterized by:

- high transaction volumes  
- varying order frequency across customers  
- mixed profitability across product categories  
- seasonal fluctuations in demand  
- discount-driven purchasing behavior in certain segments  

Despite having substantial data across sales, customers, fulfillment, and behavioral interactions, business leaders face several analytics and decision-making challenges, including:

- limited visibility into **revenue and order performance trends over time**  
- difficulty identifying **profitable vs. low-margin product categories**  
- uncertainty around the **financial impact of returns and refunds**  
- lack of insight into **delivery delays and logistics bottlenecks**  
- limited understanding of **customer repeat purchase behavior and churn risk**  
- challenges in assessing **regional performance differences across states**  

To address these challenges, this project applies a structured, data-driven analysis to evaluate historical performance, quantify operational risk areas, and generate insights that support **strategic planning, pricing decisions, retention strategy, and operational optimization**.

</td></tr>
</table>

---
>



<table width="90%" align="center">
<tr><td>

### 🎯 **Objectives and Research Goals**

The primary objective of this project is to evaluate the historical performance of a US-based ecommerce business and generate data-driven insights that support strategic decision-making across revenue growth, profitability, customer retention, and operational efficiency.

The analysis is designed to answer key business questions across the following domains:

**1- Sales & Revenue Performance**
- How have revenue, order volume, and AOV changed over time?
- Which months, seasons, or years exhibit strong or weak performance trends?

**2- Customer Engagement & Retention**
- Which customers generate the highest lifetime revenue?
- What proportion of customers are repeat vs. one-time buyers?
- Are there signs of churn based on inactivity duration?

**3- Product & Category Profitability**
- Which product categories contribute the most revenue and gross profit?
- Which categories have lower margins or higher refund exposure?

**4- Discount & Pricing Impact**
- How do discounted orders compare to non-discounted orders?
- Does discounting increase order frequency or reduce profitability?

**5- Returns & Operational Risk**
- What is the overall return rate and financial loss due to returns?
- Do slower deliveries increase return likelihood?

**6- Logistics & Delivery Performance**
- Which delivery speed categories perform best?
- How delivery delays impact customer behavior and satisfaction?

**7- Geographic Market Insights**
- Which states generate the highest order volume and revenue?
- Which locations show higher return or delivery issue risk?

The research goal is to transform raw transactional data into actionable insights that help leadership strengthen:

- pricing and promotion strategy  
- retention and loyalty programs  
- fulfillment and delivery performance  
- revenue growth and profitability optimization  

</td></tr>
</table>

---


<table width="90%" align="center">
<tr><td>

###  **Dataset Description**

The dataset contains multi-year ecommerce transaction records and supporting dimensional attributes covering operations from **2021 to 2025**. The data was validated in Excel, staged in SQL Server through staging tables, transformed into production tables, and analyzed using SQL queries and Tableau visual dashboards.

The analytical model consists of the following core datasets:

**Customers (Dimension Table)**
- 5,000+ unique customers
- Geographic attributes including state and city
- Purchasing frequency and engagement characteristics

**Product & Category (Dimension Table)**
- 8+ product categories
- Category-level performance & profitability context

**Sales Transactions (Fact Table)**
- 220,000+ transaction records
- Order ID, order date, quantity and revenue
- Total amount & discount amount
- Gross profit
- Delivery time & delivery speed category
- Return flag & financial return loss
- Behavioral attributes such as session duration

**Geographic Coverage**
- Orders generated across **7+ US states**

**Time Coverage**
- Historical period: **2021 – 2025**
- Monthly and yearly aggregation supported

**Business Scale Summary**
- 220,000+ sales records
- 5,000+ customers
- **$281M+ total recorded revenue**

The structured schema enables analysis across:

- sales and revenue performance over time  
- purchasing behavior and repeat frequency  
- product and category profitability  
- discount and pricing effectiveness  
- delivery performance and logistics speed  
- return-risk and operational loss exposure  

This curated dataset supports both **SQL-based analytical workflows** and **Tableau interactive dashboards** for executive-level decision-making.

</td></tr>
</table>

---

<table width="90%" align="center">
<tr><td>

### **Data Architecture and ETL Workflow**

This project follows a structured data-engineering workflow to ensure accuracy, reliability, and analytical readiness of the ecommerce dataset. The pipeline was designed using a **staging-to-production warehouse pattern**, with data validation checkpoints and referential-integrity controls.

The end-to-end ETL workflow consists of the following stages:

---

#### **Step 1 — Source Data Preparation**

The original dataset was provided as a consolidated **Sales Master Excel file**.  
From this file, three domain-specific extract files were created to support dimensional modeling:

- `dim_customer.csv`
- `dim_product.csv`
- `fact_sales.csv`

Each CSV file contained only relevant attributes for its target table, ensuring clean separation of:

- customer attributes
- product category attributes
- transactional sales facts

---

#### **Step 2 — Data Staging Layer (Raw Imports)**

A dedicated SQL schema (`stg`) was created to store raw imported files.

Staging tables were created with `VARCHAR(MAX)` data types to allow safe ingestion of:

- malformed values
- inconsistent text formats
- unexpected special characters

The following staging tables were implemented:

- `stg.stg_dim_customer`
- `stg.stg_dim_product`
- `stg.stg_fact_sales`

Bulk load operations were performed using `BULK INSERT`, with error handling and logging through an `etl_error_log` table.

This ensured:

- repeatable loading
- transparent failure tracking
- UTF-8 file support

---

#### **Step 3 — Data Quality & Validation Checks**

Before transformation, multiple validation blocks were executed, including:

- missing key detection (Order_ID, Customer_ID, Product_Category)
- duplicate key identification
- gender and loyalty tier distribution review
- blank or null field checks
- date parsing and invalid date detection
- numeric field casting validation
- negative and zero-value anomaly checks
- revenue reconciliation totals

Business-rule validation was also applied, including:

- unit price × quantity − discount vs recorded total
- checking rounding tolerances
- confirming financial consistency across records

This stage served as the **data reliability checkpoint** before promotion to production tables.

---

#### **Step 4 — Production Data Model (Cleaned Tables)**

After validation, data was transformed, standardized, and loaded into structured production tables:

- `dbo.customers` (Customer Dimension)
- `dbo.product_category` (Product Dimension)
- `dbo.sales` (Sales Fact Table)

Transformations included:

- text trimming & normalization
- `TRY_CAST` conversion to numeric and date types
- blank → NULL conversions
- boolean field normalization
- automatic date hierarchy derivation (Year, Month, Quarter, etc.)

Only **cleaned and validated rows** were inserted.

---

#### **Step 5 — Referential Integrity & Warehouse Constraints**

Foreign key relationships were enforced to maintain integrity:

- `sales.Customer_ID` → `customers.Customer_ID`
- `sales.Product_Category` → `product_category.Product_Category`

This ensures:

- no orphaned transaction records
- consistent lookup relationships
- trusted reporting outputs

The final schema follows a **star-schema analytical design**, optimized for:

- SQL analytical queries
- business insight reporting
- Tableau visualization

---

#### **Step 6 — Analytics & Reporting Layer**

The cleaned production tables were connected to:

- **Tableau** → for interactive dashboards and insights
- (optionally) Tableau → for visual exploration and validation

All SQL-based analysis queries were executed on the **production fact & dimension tables**, not on staging data — ensuring high-quality analytical outputs.

---

 This workflow delivers a robust, auditable, and enterprise-style ETL process designed for **data accuracy, performance reliability, and scalable analytics.**

</td></tr>
</table>

---

<table width="90%" align="center">
<tr><td>

###  **Tools and Technologies**

This project was implemented using a modern analytics technology stack combining data processing, validation, transformation, and visualization tools. Each platform was selected to support a structured and reliable end-to-end workflow.

**Microsoft SQL Server (SSMS)**
- Primary environment for data ingestion, staging, validation, and transformation  
- Implementation of ETL workflow, production tables, constraints, and analytical SQL queries  
- Enabled reliable star-schema modeling and referential-integrity enforcement

**SQL (T-SQL)**
- Used to design staging tables, cast and clean raw fields, and validate data quality  
- Applied business logic transformations across customer, product, and sales datasets  
- Powered analytical queries used for insight generation and reporting

**Microsoft Excel**
- Used during preprocessing and file structuring  
- Source for base “Sales Master” dataset and CSV extraction files  
- Assisted with result validation, summary exports, and supporting tables

**Tableau**
- Primary visualization and reporting layer  
- Used to build executive-level dashboards for:
  - revenue trends  
  - category profitability  
  - customer segmentation  
  - returns & delivery insights  

**GitHub**
- Used as the central repository for:
  - SQL scripts
  - dataset documentation
  - analytical queries
  - project write-up and artifacts

Together, these tools formed an integrated workflow that supported:

- secure and auditable data processing  
- repeatable ETL execution  
- accurate analytical outputs  
- clear and actionable insights for decision-makers  

</td></tr>
</table>

---


<table width="90%" align="center">
<tr><td>

### Methodology & Analytical Approach

This project follows a structured, end-to-end analytics workflow covering dataset preparation, ETL validation, warehouse modeling, analytical querying, and BI-driven storytelling. The methodology ensures that all insights are generated from **clean, validated, and trustworthy data**.

---

####  Phase 1 — Data Preparation & Source Structuring

The project began with a single **Sales Master File** (Excel source).  
To support scalable analytics, the dataset was logically decomposed into:

- **dim_customer.csv** — customer demographics & loyalty info  
- **dim_product.csv** — product category reference table  
- **fact_sales.csv** — transactional sales fact table  

This separation enabled a **star-schema–ready structure** and improved referential integrity.

Each file was designed to include only relevant business attributes to support downstream modeling.

---

####  Phase 2 — Staging Layer & Raw Data Ingestion

A dedicated **staging schema (`stg`)** was created in SQL Server to safely load raw CSV files.

- All fields were first ingested as `VARCHAR(MAX)`  
- BULK INSERT was used with UTF-8 compatibility  
- Error handling and ETL logging were implemented

The staging layer allowed:

- controlled ingestion  
- repeatable re-runs  
- isolation of raw data from production tables  

This ensured that **no unvalidated data** entered the warehouse.

---

####  Phase 3 — Data Quality Validation & Cleansing

A comprehensive validation framework was applied across staging tables, including:

**Customer data checks**
- missing / blank customer keys  
- duplicate customer records  
- loyalty tier distribution review  
- gender & demographic consistency checks  

**Product data checks**
- missing / null product categories  
- duplicate or malformed values  
- distinct category verification  

**Sales transaction controls**
- missing Order_ID / Customer_ID keys  
- invalid or non-parseable dates  
- numeric field validation for price, quantity, totals  
- formula validation for revenue computations  
- identification of negative or zero amounts  

Additional controls ensured:

- financial consistency  
- clean keys and foreign relationships  
- safe handling of edge-case values  

Only validated and corrected records proceeded to DW load.

---

####  Phase 4 — Warehouse Loading & Star-Schema Modeling

Cleaned records were inserted into production tables:

- **customers (Dimension)**
- **product_category (Dimension)**
- **sales (Fact Table)**

Key business attributes included:

- revenue, cost, gross profit & margin  
- discount & markup impact  
- delivery speed & return behavior  
- customer activity & session metrics  
- enriched calendar intelligence fields  

Referential integrity was enforced via:

- **FK_sales_customer**
- **FK_sales_product_category**

This ensured accurate one-to-many relationships across the model.

---

####  Phase 5 — Analytical Querying & KPI Computation

T-SQL was used to compute:

- revenue & order trends
- product profitability & category margins
- retention & returning-customer metrics
- geographic & state-level performance
- discount impact on conversion & AOV
- delivery delays vs return risk
- churn & behavioral indicators

Queries were structured for:

- repeatability  
- performance efficiency  
- analytical transparency  

Intermediate outputs were validated in Excel where necessary.

---

####  Phase 6 — Visualization & Insight Storytelling

Power BI was connected directly to the SQL warehouse to ensure:

- live query execution  
- reliable single-source-of-truth metrics  

Dashboards were designed to highlight:

- business-focused narratives  
- operational risk indicators  
- profitability opportunities  
- retention & return exposure patterns  

Visuals emphasized:

- clarity
- decision relevance
- executive interpretability

---

Overall, this methodology ensured that insights were generated through a **disciplined, auditable, and enterprise-aligned analytics process**, rather than through simple reporting or ad-hoc querying.

</td></tr>
</table>

> <div style="border:1px solid #d9d9d9; border-radius:6px; padding:16px; background:#fafafa;">


> 📊 **Sales Performance Analysis — SQL Insights + BI Visuals**

This section summarizes overall ecommerce performance using SQL-driven metrics and Tableau / Power BI visual analytics.  
The analysis covers platform scale, revenue performance, product contribution, and monthly revenue trends.

---

### 🟡 Query 1 — Platform Overview (Customers, Products, Orders)

**Purpose** — Understand business scale and dataset footprint.

**Business Question**  
How many customers, product categories, and total sales transactions exist in the portfolio?

**SQL Logic Used**

```sql
SELECT 
  (SELECT COUNT(*) FROM dbo.customers) AS customers_count,
  (SELECT COUNT(*) FROM dbo.product_category) AS product_categories_count,
  (SELECT COUNT(*) FROM dbo.sales) AS sales_count;
```

**Visualization — Portfolio Summary KPIs**  
<p align="center">
  <img src="BI_Visuals/Platform%20KPI.png" width="92%">
</p>
---

### 🟡 Query 2 — Total Revenue, Orders & AOV

**Purpose** — Measure overall financial performance.

**Business Question**  
What is the total revenue generated, transaction volume, and average order spend?

```sql
SELECT 
  SUM(Total_Amount) AS Total_revenue,
  AVG(Total_Amount) AS Avg_order_value,
  COUNT(*) AS orders
FROM dbo.sales;
```

**Visualization — Executive KPI Dashboard**  
<p align="center">
  <img src="BI_Visuals/Revenue%20KPI.png" width="92%">
</p>

---

### 🟡 Query 3 — Revenue & AOV by Product Category

**Purpose** — Identify commercial contribution by product segment.

```sql
SELECT 
    p.Product_Category, 
    COUNT(*) AS orders,
    SUM(s.Total_Amount) AS revenue,
    AVG(s.Total_Amount) AS aov
FROM dbo.sales s
JOIN dbo.product_category p 
    ON s.Product_Category = p.Product_Category
GROUP BY p.Product_Category
ORDER BY revenue DESC;
```

**Visualization — Revenue & Orders by Category**  
👉 *(insert revenue + AOV category chart)*

---

### 🟡 Query 4 — Monthly Revenue Trend (Time Series)

**Purpose** — Track revenue cycles and seasonality trends.

```sql
SELECT 
    [Year], 
    [Month], 
    CONCAT([Year], '-', RIGHT('0'+CAST([Month] AS VARCHAR(2)),2)) AS year_month,
    SUM(Total_Amount) AS revenue
FROM dbo.sales
GROUP BY [Year], [Month]
ORDER BY [Year], [Month];
```

**Visualization — Monthly Revenue Trend**  
👉 *(insert time-series chart visual)*

---

### 🧠 Sales Performance — Key Insights (Evidence-Based)

-Total recorded revenue is approximately $281.5M.
Revenue peaks in 2023, followed by a gradual decline in 2024–2025, indicating a post-growth normalization period.

-Electronics is the largest revenue contributor (~$135M).
It also has the highest AOV ($5K+), meaning the category is driven by fewer but higher-value premium transactions.

-Sports, Fashion, and Books generate high order volume but lower AOV.
These categories act as volume drivers, contributing strongly to transaction count but moderately to revenue share.

-Clear seasonal demand cycles are visible across multiple years.
Revenue spikes occur during mid-year and year-end periods, reflecting strong response to retail campaigns and promotions.

-2025 indicates emerging demand slowdown signals.
Annual order volume declines from 56K (2023) → 46K (2024) → 33K (2025), suggesting reduced purchasing frequency and potential retention risk.

-AOV remains stable at ~$1.28K despite order decline.
This confirms performance impact is volume-driven, not caused by discount erosion or ticket-size reduction.

</div>



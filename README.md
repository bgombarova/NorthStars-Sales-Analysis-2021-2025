# Ecommerce Analytics Platform — SQL , ETL & BI Insights
---
<p>
  <img src="https://img.shields.io/badge/SQL-Data%20Engineering-025E8C?style=for-the-badge&logo=postgresql" />
  <img src="https://img.shields.io/badge/Microsoft%20SQL%20Server-ETL%20%7C%20DW-CC2927?style=for-the-badge&logo=microsoftsqlserver" />
  <img src="https://img.shields.io/badge/Power%20BI-Analytics%20%7C%20Dashboards-F2C811?style=for-the-badge&logo=powerbi" />
  <img src="https://img.shields.io/badge/Tableau-Data%20Visualization-E97627?style=for-the-badge&logo=tableau" />
  <img src="https://img.shields.io/badge/Excel-Data%20Cleaning%20%7C%20Modeling-217346?style=for-the-badge&logo=microsoftexcel" />
  <img src="https://img.shields.io/badge/GitHub-Version%20Control-181717?style=for-the-badge&logo=github" />
</p>

<table width="90%" align="center">
<tr><td>

### **Executive Summary**

This project presents an end-to-end analytics study of a **US-based ecommerce company** operating in the consumer retail domain. The dataset contains multi-year transactional, customer, fulfillment, and behavioral records used to evaluate business performance across revenue trends, order volume, profitability, discount impact, returns, delivery performance, and customer engagement.

The research focuses on deriving actionable insights across:

This project is designed around the core ecommerce questions that business stakeholders and leadership teams typically care about:

**Revenue Growth & Demand Trends** — How sales volume and revenue evolve over time, and where growth or slowdown signals emerge

**Category & Product Profitability** — Which product groups drive profit vs volume, and where margin leakage occurs

**Customer Value & Retention Health** — Which customers generate repeat revenue, where churn risk appears, and how purchasing behavior shifts over time

**Price Sensitivity & Discount Dependency** — How discounts influence conversion, order value, and long-term revenue quality

**Returns & Financial Risk Exposure** — Which segments experience higher return rates and associated loss impact

**Delivery Performance & Experience Risk** — Where slow delivery correlates with operational friction or customer risk pockets

**Market & Geographic Concentration** — Which cities and states contribute most to revenue and profitability

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

### **Objectives and Research Goals**

The primary objective of this project is to evaluate the historical performance of a US-based ecommerce business and generate data-driven insights that support strategic decision-making across revenue growth, profitability, customer retention, and operational efficiency.

The analysis focuses on four core decision areas:

**Sales & Revenue Performance** — understanding demand trends, order growth, and AOV movement over time

**Customer Value & Retention** — identifying high-value, repeat, and at-risk customer segments

**Product & Profitability Dynamics** — assessing which categories drive revenue vs. margin contribution

**Operational & Experience Risk** — analyzing discounts, returns, and delivery performance exposure

The research objective is not only to describe what happened in the data, but to surface patterns, risks, and opportunities that leadership teams can use to:

- strengthen pricing & promotion strategy

- improve retention and repeat-purchase behavior

- optimize fulfillment and delivery experience

- support sustainable revenue and profitability growth

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

</td></tr>
</table>

---

<table width="90%" align="center">
<tr><td>

### **Data Preparation & Analytical Dataset Workflow**

The dataset was prepared to support decision-focused ecommerce analysis and reporting.
The final analytical model was structured into three validated tables:

**Customers** — acquisition, activity, repeat-purchase behavior

**Product Categories** — merchandise performance grouping

**Sales Transactions** — revenue, order value, discounts, returns

During preparation, the data was:

- reviewed for gaps, duplicates, and structural inconsistencies

- reconciled against financial totals to avoid misleading insights

- standardized into analysis-ready fields (dates, categories, KPIs)

- Only records that passed validation were promoted into the analytical layer.

The result is a clean, reliable dataset designed to answer real business questions, including:

- which products and markets drive revenue concentration

- how customer retention and purchase frequency evolve over time

- where operational risk appears in delivery, returns, or discounts

This ensures that every insight in the project is evidence-based, decision-relevant, and defensible to stakeholders.

</td></tr>
</table>

---

<table width="90%" align="center">
<tr><td>

###  **Tools and Technologies**

This project was implemented using a modern analytics technology stack combining data processing, validation, transformation, and visualization tools. Each platform was selected to support a structured and reliable end-to-end workflow.

**Microsoft SQL Server (SQL)** — data modeling, validation, transformation, analytical querying

**Excel** — source structuring & quick exploratory checks

**Tableau** — executive-level dashboards & visual storytelling

</td></tr>
</table>

---
<table width="90%" align="center">
<tr><td>


> <div style="border:1px solid #d9d9d9; border-radius:6px; padding:16px; background:#fafafa;">


> ### **Sales Performance — Business Insights**

This section evaluates revenue trends, order volumes, and product contribution patterns to understand business growth dynamics and commercial performance drivers.

---

**Key Findings**

-**Total recorded revenue is approximately $281.5M.**
Revenue peaks in 2023, followed by a gradual decline in 2024–2025, indicating a post-growth normalization period.

-**Electronics is the largest revenue contributor (~$135M)**.
It also has the highest AOV ($5K+), meaning the category is driven by fewer but higher-value premium transactions.

-**Sports, Fashion, and Books generate high order volume but lower AOV.**
These categories act as volume drivers, contributing strongly to transaction count but moderately to revenue share.

-**Clear seasonal demand cycles are visible across multiple years.**
Revenue spikes occur during mid-year and year-end periods, reflecting strong response to retail campaigns and promotions.

-**2025 indicates emerging demand slowdown signals.**
Annual order volume declines from 56K (2023) → 46K (2024) → 33K (2025), suggesting reduced purchasing frequency and potential retention risk.

-**AOV remains stable (~$1.28K) despite falling volume.**
This indicate drop in performance is volume-driven, rahter than caused by discount pressure or ticket-size erosion.



---

**Sales Excutive KPI's**

<p align="center">
  <img src="BI_Visuals/Revenue%20KPI.png" width="92%">
</p>

<p align="center">
  <img src="BI_Visuals/KPI%20Trend%20Details.png" width="92%">
</p

---

 **Revenue by Product Category**

<p align="center">
  <img src="BI_Visuals/Revenue%20By%20Product%20Category.png" width="92%">
</p>

---

**Revenue Time-Series Trend (Multi-Year)**

<p align="center">
  <img src="BI_Visuals/Sales%20Time%20Series.png" width="92%">
</p
BI_Visuals/Sales%20Time%20Series.png

---

**Strategic Implications**

- Growth now depends more on repeat purchase retention than new acquisition

- Electronics revenue concentration increases commercial dependency risk

- Volume-driven categories should be leveraged to cross-sell high-value segments

- Marketing teams can extend revenue uplift by expanding seasonal campaigns

- Declining order volume in later years signals early churn & demand softening

---

**Recommended Business Actions**

- Launch high-value Electronics loyalty bundles to stabilize premium revenue

- Introduce cross-sell promotions in Sports & Fashion to lift AOV

- Design reactivation campaigns targeting inactive 2024–2025 customers

- Expand seasonal promotion windows into pre-event warm-up periods

- Track early churn indicators through repeat purchase frequency monitoring



</td></tr>
</table>
  
</div>

<div style="border:1px solid #d9d9d9; border-radius:6px; padding:16px; background:#fafafa;">

---

<table width="90%" align="center">
<tr><td>

>### **Customer Behavior & Retention — Key Insights**


This section analyzes how customers behave across lifetime value, repeat purchase frequency, recency, churn risk, and acquisition cohorts.  
The objective is to understand **customer retention strength, spending concentration, and lifecycle purchase behavior**.

---

**Key Findings** 

The platform is primarily sustained by **loyal repeat customers**

- **3,926 customers** fall in the **High-Frequency (20+ purchases)** segment

- These buyers form the **financial backbone of recurring revenue**

Mid-frequency customers represent the **largest growth-conversion opportunity**

- **1,067 customers** sit in the **6–20 purchase range**

- They demonstrate consistent activity but have not yet reached **loyalty tier status**

A small set of customers contributes disproportionately high lifetime value

- Top customers generate** $400K–$900K+** lifetime revenue each

- AOV ranges between **$4K–$25K,** indicating premium buyers

Recency patterns suggest core customers remain active

- Many top-value customers purchased within **1–20 days**

- However, a subset shows **90–120+ day inactivity gaps**, signaling churn exposure

New-customer acquisition has slowed over time

- Initial cohorts show strong onboarding in early **2021**

- Later months drop to **double-digit → single-digit inflow**

- Growth is increasingly driven by **retention rather than acquisition**

---
 
**Repeat Purchase Distribution — Frequency Buckets**


<p align="center"> <img src="BI_Visuals/Repeat%20Purchase%20Frequency%20Buckets.png" width="92%"> </p>

---

**Customer Acquisition Cohort Trend — First Purchase Month**

<p align="center"> <img src="BI_Visuals/Customer%20Acquisition%20Cohort%20Trend.png" width="92%"> </p>

---

**Business Implications**

- Revenue stability depends heavily on repeat-buyer retention

- The business is now retention-led rather than acquisition-led

- Medium-frequency customers represent the highest-leverage expansion tier

- Ultra-high-value customers require special treatment and churn monitoring

- Acquisition slowdown indicates:

-- possible channel under-investment, or

-- market saturation in existing segments

---

**Recommended Business Actions**

**Short-Term (Retention Focus)**

- Design loyalty-upgrade program for 6–20 order segment

- Prioritize VIP relationship management for top-value customers

- Trigger recency-based re-engagement campaigns for inactive high-value users

**Medium-Term (Growth Pipeline)**

- Reassess acquisition channel performance & spend allocation

- Test referral + win-back incentives

- Evaluate new-audience targeting & market segmentation

</td></tr>
</table>

</div> 

> <div style="border:1px solid #d9d9d9; border-radius:6px; padding:16px; background:#fafafa;">

---

<table width="90%" align="center">
<tr><td>

> ###   **Product Performance & Profitability Analysis**
<div style="border:1px solid #d9d9d9; border-radius:6px; padding:16px; background:#fafafa;">

This section analyzes product-level commercial performance, including profitability, discount dependency, and financial exposure from returns.

---

**Key Findings** 

**Beauty delivers the highest margin performance (36.24%)**
but also reports one of the **highest return rates (~13%+)**, suggesting premium pricing strength but higher post-purchase dissatisfaction risk.

**Sports is the strongest risk-adjusted performer**
**High margin (30.96%)** + **low returns (~3–4%)** — indicating stable demand and efficient fulfillment economics.

**Electronics drives the largest revenue (~$135M)**
but** 66%** of orders are discount-driven, meaning performance is primarily promotion-sensitive rather than organic demand.

**Books and Beauty carry disproportionate return losses (>13%**)
significantly above the portfolio baseline **(~3–4%)**, implying potential issues in:
product fit, expectation mismatch, or quality perception.

**Food category shows weakest profitability (4.38% margin)**
indicating high cost of goods, weak pricing power, or operational inefficiencies.

**Fashion, Toys & Sports act as volume engines**
high order throughput with stable and predictable return risk — supporting scale growth without major loss exposure.

**Portfolio demand is highly price-elastic**
with 66% of all transactions occurring under discounts, confirming revenue reliance on promotional levers.

---

 **Profit Margin % by Product Category**

<p align="center"> <img src="BI_Visuals/Profitability%20by%20Product%20Category.png" width="92%"> </p>

---

**Returns & Loss Impact — Category Level**

<p align="center"> <img src="BI_Visuals/Returns%20%26%20Loss%20Impact%20—%20Product%20Category%20Level%20Chart.png" width="92%"> </p>

---

**Business Implications**

- Margin strength is concentrated in a small set of premium categories (Beauty, Sports, Electronics)

- Loss risk is driven by high-return categories (Beauty, Books)

- Revenue growth is promotion-dependent rather than organically driven

- Lower-margin categories (Food) may be diluting overall profitability

- Sports emerges as a scalable “profitable growth” category

- Electronics requires promotion planning rather than price cuts

- Beauty requires post-purchase experience improvement rather than discounting

  ---

 **Recommended Business Actions**
 
- Scale **Sports, Fashion & Toys — strong margins (20–31%)** and **low return risk (~3–4%)**; prioritize inventory allocation and campaign funding here.

- Protect profits in **Electronics — 66%** of orders are discount-driven; reduce blanket discounts and shift to loyalty, bundles, and targeted promos.

- Fix quality + expectation gaps in Beauty & Books — returns >13% causing refund losses; run root-cause review, improve product info, size/usage guidance, and post-purchase support.

- Re-evaluate **Food category economics — weakest margin (4.38%)**; renegotiate supplier pricing or trim unprofitable SKUs.

- Monitor price elasticity vs. margin erosion — track discount-to-profit ratio monthly to prevent promo-driven revenue dependence.

- Allocate growth investment toward **high-margin, low-risk categories** while stabilizing return-sensitive product lines before scaling further.

</td></tr>
</table>

</div>

> <div style="border:1px solid #d9d9d9; border-radius:6px; padding:16px; background:#fafafa;">

> <div style="border:1px solid #d9d9d9; border-radius:6px; padding:16px; background:#fafafa;">

---

## **Channel & Engagement Performance**

This section analyzes how customers engage across  
**time-of-week demand, sales channels, device usage behavior, and browsing intent patterns.**

The objective is to understand:

- peak shopping windows  
- which channels drive revenue & orders  
- device-level engagement behavior  
- whether longer session activity correlates with higher spending  

---

### 🟡 Query 12 — Orders & Revenue by Day of Week

**Purpose** — Identify weekly demand cycles and operational load patterns.

**Business Question**  
On which days does order volume and spending peak across the week?

```sql
SELECT 
    DayOfWeek, 
    COUNT(*) AS orders, 
    SUM(Total_Amount) AS revenue
FROM dbo.sales
GROUP BY DayOfWeek
ORDER BY CASE DayOfWeek
    WHEN 'Monday' THEN 1 
    WHEN 'Tuesday' THEN 2 
    WHEN 'Wednesday' THEN 3
    WHEN 'Thursday' THEN 4 
    WHEN 'Friday' THEN 5 
    WHEN 'Saturday' THEN 6 
    WHEN 'Sunday' THEN 7
    ELSE 8 END;
```

**Visualization — Orders & Revenue by Weekday**

<p align="center">
  <img src="BI_Visuals/Orders%20%26%20Revenue%20by%20Day%20of%20Week.png" width="92%">
</p>

---

### 🟡 Query 13 — Sales Channel Performance

**Purpose** — Evaluate which channels contribute the most to revenue and order traffic.

**Business Question**  
Which sales channels generate the highest revenue, AOV, and order contribution?

```sql
SELECT 
    Sales_Channel, 
    COUNT(*) AS orders, 
    SUM(Total_Amount) AS revenue, 
    AVG(Total_Amount) AS aov
FROM dbo.sales
GROUP BY Sales_Channel
ORDER BY revenue DESC;
```

**Visualization — Channel Contribution (Orders, Revenue, AOV)**

<p align="center">
  <img src="BI_Visuals/Sales%20Channel%20Performance.png" width="92%">
</p>

---

### 🟡 Query 14 — Device Type vs Engagement Quality

**Purpose** — Understand behavioral engagement differences across device platforms.

**Business Question**  
Do desktop, tablet, or mobile users show higher browsing depth or purchase intent?

```sql
SELECT 
    Device_Type,
    COUNT(*) AS orders,
    AVG(Session_Duration_Minutes) AS avg_session_mins,
    AVG(Pages_Viewed) AS avg_pages
FROM dbo.sales
GROUP BY Device_Type
ORDER BY orders DESC;
```

**Visualization — Device Usage & Engagement Metrics**

<p align="center">
  <img src="BI_Visuals/Device%20Type%20vs%20Engagement%20Quality.png" width="92%">
</p>


---

### 🟡 Query 15 — Session Duration vs Order Value (Intent Signal)

**Purpose** — Analyze whether deeper browsing translates to higher spending.

**Business Question**  
Is there a positive relationship between session duration and order value?

```sql
SELECT
    AVG(Session_Duration_Minutes) AS avg_session_mins,
    AVG(Total_Amount) AS avg_order_value
FROM dbo.sales
GROUP BY CAST(Session_Duration_Minutes / 5 AS INT)  -- engagement buckets
ORDER BY CAST(Session_Duration_Minutes / 5 AS INT);
```

**Visualization — Session Duration vs AOV Trend**

<p align="center">
  <img src="BI_Visuals/Session%20Duration%20vs%20Order%20Value%20scatter%20plot.png" width="92%">
</p>

---

## ** Channel & Engagement — Key Insights**

-Online & Mobile App channels dominate revenue contribution
Online contributes **$123.7M (highest revenue)** followed by Mobile App at **$100.6M** — confirming that digital channels are the primary commercial drivers, while Retail Store and B2B remain secondary channels.

-Strong multichannel demand but value concentration in digital
Retail Store & B2B generate meaningful order volumes, however revenue contribution remains significantly lower — indicating lower-value or transactional purchase behavior in these channels.

-Engagement is highest on Mobile devices despite similar session length
Mobile users account for **114K+ orders** compared to Desktop (74K) and Tablet (30K), even though session time **averages ~14 mins** across devices — suggesting higher conversion efficiency on Mobile.

-Page-depth patterns indicate stronger browsing behavior on Mobile & Tablet
Mobile & Tablet users average 9 pages/session vs 8 pages on Desktop, implying greater exploration behavior and potential cross-sell opportunities on mobile platforms.

-Weekday demand remains stable with no significant drop-off risk
Orders remain consistently distributed across days — Monday to Saturday **average ~31K orders** each, indicating predictable baseline demand and minimal weekday volatility.

-Sunday shows slightly lower order volume but stable revenue
Sunday orders dip modestly relative to weekdays, but revenue impact remains neutral — suggesting stable AOV rather than basket erosion.

-Longer browsing sessions correlate with higher purchase value
Session buckets **30–35** minutes show the highest AOV **(~$1.5K+)**, confirming that higher engagement duration is linked with stronger purchase intent rather than casual browsing.

-Extremely short & extremely long sessions indicate weak purchase intent
Very **short sessions (~0–5 mins)** and **very long sessions (~40+ mins)** reflect lower AOV, likely representing bounce traffic and abandoned browsing rather than high-value activity.
</div>

---

> ### **Delivery & CX Risk Analytics**
<div style="border:1px solid #d9d9d9; border-radius:6px; padding:16px; background:#fafafa;">

This section evaluates how delivery speed and logistics performance impact
customer experience, returns behavior, and satisfaction outcomes.

- The objective is to identify:
- delivery-driven financial risk,
- customer dissatisfaction thresholds, 
- fulfillment improvement opportunities.

---


### 🟡 Query 16 — Delivery Speed vs Returns (Logistics Risk)

**Purpose** — Assess whether slower delivery speeds are associated with higher return likelihood.

**Business Question**
Do delayed shipments increase product return probability?

```sql

SELECT 
    Delivery_Speed_Category,
    COUNT(*) AS orders,
    SUM(CASE WHEN Return_Flag = 1 THEN 1 ELSE 0 END) AS returns,
    CAST(
        100.0 * SUM(CASE WHEN Return_Flag = 1 THEN 1 ELSE 0 END) / COUNT(*)
        AS DECIMAL(6,2)
    ) AS return_rate_pct
FROM dbo.sales
GROUP BY Delivery_Speed_Category
ORDER BY return_rate_pct DESC;
```


Visualization — Returns vs Delivery Speed

<p align="center"> <img src="BI_Visuals/Delivery%20Speed%20vs%20Returns%20(Logistics%20Risk).png" width="92%"> </p>

---

### 🟡 Query 17 — Delivery Fulfillment Speed Buckets (Operational Exposure)

**Purpose** — To evaluate how order volume is distributed across delivery speed ranges, identify slow-fulfillment exposure, and highlight operational risk in orders taking more than 10 days to deliver.

**Business Question**
How many orders fall into each delivery time bucket, and what proportion of total orders are being fulfilled within acceptable delivery windows versus slow or delayed delivery windows?


```sql

WITH delivery_buckets AS (
    SELECT 
        CASE 
            WHEN Delivery_Time_Days BETWEEN 0 AND 3 THEN '0–3 Days'
            WHEN Delivery_Time_Days BETWEEN 4 AND 7 THEN '4–7 Days'
            WHEN Delivery_Time_Days BETWEEN 8 AND 10 THEN '8–10 Days'
            WHEN Delivery_Time_Days BETWEEN 11 AND 15 THEN '11–15 Days'
            WHEN Delivery_Time_Days BETWEEN 16 AND 20 THEN '16–20 Days'
            ELSE '20+ Days'
        END AS delivery_bucket,
        Customer_Rating,
        Delivery_Time_Days
    FROM dbo.sales
)
SELECT 
    delivery_bucket,
    COUNT(*) AS orders,
    AVG(Customer_Rating) AS avg_rating,
    AVG(Delivery_Time_Days) AS avg_delivery_days
FROM delivery_buckets
GROUP BY delivery_bucket
ORDER BY 
    CASE 
        WHEN delivery_bucket = '0–3 Days' THEN 1
        WHEN delivery_bucket = '4–7 Days' THEN 2
        WHEN delivery_bucket = '8–10 Days' THEN 3
        WHEN delivery_bucket = '11–15 Days' THEN 4
        WHEN delivery_bucket = '16–20 Days' THEN 5
        ELSE 6
    END;

```

Visualization — Delivery Time vs Orders Volume

<p align="center"> <img src="BI_Visuals/Delivery%20Fulfillment%20Speed%20Buckets%20(Operational%20Exposure).png" width="92%"> </p>

---

### **Delivery & CX — Key Insights**

**Order volume is concentrated in the 4–7 day delivery window**
**81,871 orders (≈40% of total volume)** fall in this bucket, indicating this is the primary logistics SLA used across the network.

**Ultra-fast (0–3 days) delivery accounts for 66,123 orders (~32%)**
This suggests a strong dependency on express fulfillment capacity, which likely drives higher logistics cost exposure.

**Deliveries exceeding 10 days form a visible long-tail risk segment**
34,122 (8–10 days) + 25,668 (11–15 days) + 8,252 (16–20 days) + 3,964 (20+ days)
→ **collectively 72,000+ delayed orders (~35% of total)**
representing potential experience degradation & retention risk.

**Slow deliveries show materially higher return probability**
Return rate = 6.82% for Slow vs ≈2% for Fast & Medium
confirming that delivery latency is a key CX failure driver, not product quality.

**Ratings remain flat across delivery buckets (avg = 3.0)**
This implies customers do not immediately reflect delivery pain in ratings,
reinforcing that returns & churn signals are stronger risk indicators than ratings.

**Most operational exposure sits between 8–15 days**
59,790 orders in these buckets indicate a systemic mid-tier logistics bottleneck
→ likely tied to regional routing or inventory transfer lag.

**20+ day orders represent a critical escalation zone**
3,964 cases constitute a CX incident-level segment requiring
customer recovery workflows (refund credit / proactive outreach).



</div>

---

### **Geographic Performance Insights**
<div style="border:1px solid #d9d9d9; border-radius:6px; padding:16px; background:#fafafa;">

 This section evaluates regional business performance using geography-level sales and profitability analytics.

 The objective is to understand state-level demand concentration, revenue contribution, and profit efficiency across operating regions.

---

### 🟡 Query 18 — Orders & Revenue Contribution by City & State

**Purpose** — Identify high-revenue markets and regional demand concentration.

**Business Question**
Which cities and states generate the highest order volume and revenue contribution across the portfolio?

```sql

SELECT 
    c.City,
    c.State,
    COUNT(*) AS orders,
    SUM(s.Total_Amount) AS revenue
FROM dbo.sales s
JOIN dbo.customers c 
    ON s.Customer_ID = c.Customer_ID
GROUP BY c.City, c.State
ORDER BY revenue DESC;
```

Visualization — Geographic Revenue Distribution (State & City Level)

<p align="center"> <img src="BI_Visuals/Orders%20%26%20Revenue%20Contribution%20by%20City%20%26%20State%20Detailed%20Visual.png" width="92%"> </p> 

<p align="center"> <img src="BI_Visuals/Revenue%20Contribution%20by%20City.png" width="92%"> </p> 


---

### 🟡 Query 19 — Profit Margin Performance by State

**Purpose** — Assess geographic profitability and operating efficiency variation.

**Business Question**
Which states are highly profitable vs cost-intensive, based on gross profit margin contribution?

```sql

SELECT 
    c.State,
    SUM(s.Gross_Profit) AS gross_profit,
    SUM(s.Total_Amount) AS revenue,
    CAST(
        100.0 * SUM(s.Gross_Profit) / SUM(s.Total_Amount)
        AS DECIMAL(6,2)
    ) AS profit_margin_pct
FROM dbo.sales s
JOIN dbo.customers c 
    ON s.Customer_ID = c.Customer_ID
GROUP BY c.State
ORDER BY profit_margin_pct DESC;
```

Visualization — State-Level Profitability Ranking

<p align="center"> <img src="BI_Visuals/Profit%20Margin%20Performance%20by%20State.png" width="92%"> </p>

---

### **Geographic Performance — Key Insights**

**Revenue leadership is highly concentrated in a few metro hubs.**
New York City alone contributes **$72.86M** in revenue across **56.9K** orders, making it the single largest commercial market.
Chicago **($38.14M)** and Los Angeles **($35.02M)** follow as secondary revenue centers, forming a Tier-1 urban performance cluster.

**California appears as a dual-engine revenue driver at the city level.**
Los Angeles ($35.0M) and San Francisco ($21.15M) together generate $56M+ revenue, reinforcing California’s position as a strategic premium consumer market.

**Atlanta and Boston exhibit strong mid-market performance.**
Despite lower order volumes vs Tier-1 cities, both deliver $21M–$30M revenue, indicating healthy demand density outside major population hubs.

**Texas markets show balanced commercial strength rather than spiky concentration.**
Dallas **($19.6M)** and Austin **($17.29M)** jointly contribute **$36.9M** revenue, suggesting distributed economic activity rather than single-city dominance.

**West-coast secondary markets demonstrate healthy profitability positioning.**
Seattle generates **$13.84M** revenue across 10.9K orders, aligning with higher-value but moderate-volume urban spending patterns.

**State-level profitability leaders indicate operational & pricing advantages.**
Massachusetts **(25.05%), Illinois (25.03%), and Texas (24.82%)** report the highest gross margin performance, suggesting
— lower discount reliance,
— stronger product mix, and
— healthier cost-to-revenue leverage.

**Lower-margin states still maintain strong revenue bases.**
California (24.71%) and New York (24.75%) remain highly profitable despite volume intensity, meaning margin pressure is controlled and structurally resilient

</div>


---


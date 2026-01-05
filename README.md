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

Despite having substantial data across sales, customers, fulfillment, and behavioral interactions, **company management face several analytics and decision-making challenges, including**:

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

### **Dataset Overview**

This analysis is based on a multi-year ecommerce transaction dataset covering 2021–2025, containing customer activity, product sales, delivery performance, discounts, and returns across multiple US states.

The dataset represents a mid-to-large scale retail business and supports trend, profitability, retention, and operational risk analysis.

**Data Scope & Business Coverage**

- 5,000+ customers

- 220,000+ sales transactions

- $281M+ recorded revenue

- Activity generated across multiple US states & metro markets

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

>### **Customer Behavior & Retention — Business Insights**


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

> ###   **Product Performance - Business Insights**
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

<table width="90%" align="center">
<tr><td>

> ### **Delivery & Customer Experience - Business Insights**
<div style="border:1px solid #d9d9d9; border-radius:6px; padding:16px; background:#fafafa;">

This section evaluates how delivery speed and logistics performance impact
customer experience, returns behavior, and satisfaction outcomes.

- The objective is to identify:
- delivery-driven financial risk,
- customer dissatisfaction thresholds, 
- fulfillment improvement opportunities.

---

 **Key Findings**

- **4–7 day delivery is the dominant fulfillment window**
81,871 orders (~40% of total) sit in this SLA — indicating it is the operational baseline for most shipments.

- **0–3 day “Express Delivery” carries ~32% of order volume**
66,123 orders rely on fast-track fulfillment — implying higher logistics cost dependency.

- **8–15 day deliveries form the largest CX risk band**
**34,122 (8–10 days)** + **25,668 (11–15 days)** →** 59,790** delayed orders **(~29%)**.

- **20+ day deliveries are small in volume but high-risk**
3,964 orders fall into critical delay territory — likely escalation / refund candidates.

- **Slow delivery significantly increases return probability**
Return rate = **6.82% (Slow)** vs ≈**2% (Fast/Medium)** →
delivery latency is a stronger risk driver than product issues.

- **Mid-tier shipping appears to be a systemic bottleneck**
8–15 day segment concentration suggests
inventory routing or regional hub lag issues.

---

**Return Rate % by Delivery Speed Category**

<p align="center"> <img src="BI_Visuals/Delivery%20Speed%20vs%20Returns%20(Logistics%20Risk).png" width="92%"> </p>

---

**Delivery Volume Distribution Across Time Ranges**

<p align="center"> <img src="BI_Visuals/Delivery%20Fulfillment%20Speed%20Buckets%20(Operational%20Exposure).png" width="92%"> </p>

---

**Business Implications**

- Delays beyond 8 days directly increase refund & churn risk

- Express delivery volume indicates cost-intensive dependency

- CX degradation is quietly accumulating in mid-tier shipping lanes

---

**Recommended Actions**

**1) Prioritize shipping optimization for 8–15 day deliveries**

- reroute inventory through faster hubs

- review regional carrier performance

- improve inter-warehouse transfer timing

**2) Flag 20+ day orders for proactive recovery workflows**

- auto-refund credit / apology voucher

- CX outreach triggers

**3) Protect margins by reducing reliance on express shipping**

- shift eligible volume to 4–7 day SLA where possible

**4) Introduce delivery-time transparency in checkout**

- manage expectations

- reduce returns driven by delay frustration

**5) Build a delivery-delay risk alert KPI**

- monitor orders crossing 8-day threshold in near-real-time


</td></tr>
</table>

</div>

---

<table width="90%" align="center">
<tr><td>

> ### **Geographic Performance - Business Insights**
<div style="border:1px solid #d9d9d9; border-radius:6px; padding:16px; background:#fafafa;">

 This section evaluates regional business performance using geography-level sales and profitability analytics.

 The objective is to understand state-level demand concentration, revenue contribution, and profit efficiency across operating regions.

---

- **Revenue leadership is highly concentrated in a few metro hubs.**
New York City alone contributes **$72.86M** in revenue across **56.9K** orders, making it the single largest commercial market.
Chicago **($38.14M)** and Los Angeles **($35.02M)** follow as secondary revenue centers, forming a Tier-1 urban performance cluster.

- **California appears as a dual-engine revenue driver at the city level.**
Los Angeles ($35.0M) and San Francisco ($21.15M) together generate $56M+ revenue, reinforcing California’s position as a strategic premium consumer market.

- **Atlanta and Boston exhibit strong mid-market performance.**
Despite lower order volumes vs Tier-1 cities, both deliver $21M–$30M revenue, indicating healthy demand density outside major population hubs.

- **Texas markets show balanced commercial strength rather than spiky concentration.**
Dallas **($19.6M)** and Austin **($17.29M)** jointly contribute **$36.9M** revenue, suggesting distributed economic activity rather than single-city dominance.

- **West-coast secondary markets demonstrate healthy profitability positioning.**
Seattle generates **$13.84M** revenue across 10.9K orders, aligning with higher-value but moderate-volume urban spending patterns.

- **State-level profitability leaders indicate operational & pricing advantages.**
Massachusetts **(25.05%), Illinois (25.03%), and Texas (24.82%)** report the highest gross margin performance, suggesting
— lower discount reliance,
— stronger product mix, and
— healthier cost-to-revenue leverage.

- **Lower-margin states still maintain strong revenue bases.**
California (24.71%) and New York (24.75%) remain highly profitable despite volume intensity, meaning margin pressure is controlled and structurally resilient

---

**Revenue Contribution by City**

<p align="center"> <img src="BI_Visuals/Revenue%20Contribution%20by%20City.png" width="92%"> </p> 

---

**Profit Margin Performance by State**

<p align="center"> <img src="BI_Visuals/Profit%20Margin%20Performance%20by%20State.png" width="92%"> </p>

---

**Business Implications**

- Revenue risk is **geographically concentrated** — underperformance in 2–3 cities would materially impact portfolio results.

- California and New York represent premium but cost-sensitive growth territories — requiring margin-aware scaling.

- Texas growth is **broad and stable**, making it a strong candidate for operational expansion.

- High-margin states signal **pricing power + healthier customer economics** and should guide future go-to-market focus.

- Mid-tier markets (Atlanta / Boston / Seattle) show untapped profitability upside relative to volume.

---

**Recommended Actions**

**1) Double-down growth programs in Tier-1 revenue hubs**

- New York, Chicago, Los Angeles:
 targeted retention + premium assortment expansion

**2) Scale marketing + fulfillment investments in high-margin states**

- Massachusetts, Illinois, Texas: 
 improve contribution without discount dependency

**3) Run expansion pilots in strong mid-tier markets**

- Atlanta, Boston, Seattle :
 test regional assortment + logistics optimization

**4) Monitor discount elasticity in California & New York**

- Protect margins while scaling volume growth

**5) Develop a geographic risk-diversification plan**

- Reduce over-dependence on top 3 cities

  </td></tr>
</table>

</div>


---


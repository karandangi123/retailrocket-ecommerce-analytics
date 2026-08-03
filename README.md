# RetailRocket Executive Analytics Case Study

> **(Customer Journey, Performance & Retention Analytics)**  
> **Author:** Karan Dangi | **Domain:** E-commerce Customer Journey, Merchandising & Retention Analytics  
> **Dataset:** RetailRocket E-Commerce Event Log (2.75M Events, 1.40M Visitors, 235K Products)

---

## Table of Contents
- [Executive Overview](#executive-overview)
- [Project Objective](#project-objective)
- [Key Business Performance Metrics](#key-business-performance-metrics)
- [Skills Demonstrated](#skills-demonstrated)
- [Technologies & Tools](#technologies--tools)
- [Strategic Business Impact Ranking](#strategic-business-impact-ranking)
- [Repository & File Architecture](#repository--file-architecture)
- [Business Analytics Workflow](#business-analytics-workflow)
- [Key Business Outcomes](#key-business-outcomes)
- [Executive Deliverables](#executive-deliverables)
- [Author & Contact](#author--contact)

---

## Executive Overview

This project demonstrates how raw clickstream data can be transformed into executive-ready business recommendations through customer journey analytics, conversion funnel analysis, RFM segmentation, cohort retention, merchandising analytics, and market basket analysis.

By auditing **2,755,641 clean behavioral events** across **1,407,580 unique visitors**, the analysis diagnoses top-of-funnel drop-offs, post-add cart abandonment friction, category merchandising opportunities, customer retention decay, and cross-selling potential.

```
   1.41M Total Visitors ──► 99.76% Product Views ──► 2.68% Add-to-Cart ──► 0.83% Purchase Conversion
                                                           │                      │
                                                 97.32% Funnel Drop-off   71.96% Cart Abandonment
```

---

## Project Objective

**Objective:** Identify the largest commercial bottlenecks across the customer journey and recommend data-driven initiatives to improve conversion, retention, and performance.

📄 **Detailed Executive Report:** [**Ecommerce Customer Behavior & Business Performance Analysis.pdf**](./Ecommerce%20Customer%20Behavior%20%26%20Business%20Performance%20Analysis.pdf)

---

## Key Business Performance Metrics

The table below provides the primary empirical benchmarks computed directly from the event log:

| Business Metric | Value | Empirical Benchmark / Interpretation |
|---|:---:|---|
| **Total Unique Visitors** | `1,407,580` | Total traffic volume across observation window (May–Sep 2015) |
| **Total Clean Events** | `2,755,641` | 2,664,312 views \| 69,332 add-to-carts \| 21,997 transactions |
| **Overall Purchase Conversion** | **`0.83%`** | 11,719 completed buyers out of 1.41M visitors |
| **Top-of-Funnel Loss (View → Cart)** | **`97.32%`** | 1,366,506 product viewers left without adding items to cart |
| **Cart Abandonment Rate** | **`71.96%`** | 27,146 cart creators abandoned before checkout |
| **Cart-to-Purchase Conversion** | **`31.07%`** | Visitors reaching cart convert 37.4× higher than browsers |
| **Repeat Purchase Rate** | **`21.98%`** | 2,582 repeat buyers (78.02% single-time buyers) |
| **Exact Same-Item Reorder Buyers** | `650` | Represents 5.55% of buyers (and 25.17% of repeat buyers) |
| **Single-Item Order Share** | **`81.45%`** | 18,324 single-product transactions (Average basket size: 1.27 items) |
| **Peak Hourly Conversion Multiplier**| **`3.4×`** | 1.16% conversion at 8 PM UTC vs 0.34% at 8 AM UTC |
| **Max Market Basket Lift** | **`166.48`** | Product 213834 ↔ 445351 (Parent Category 561) |

---

## Skills Demonstrated

• Customer Journey Analytics  
• Funnel Analysis  
• Product Analytics  
• Merchandising Analytics  
• Customer Segmentation (RFM)  
• Cohort Retention Analysis  
• Market Basket Analysis  
• SQL Window Functions  
• Business Storytelling  
• Executive Reporting  

---

## Technologies & Tools

• Python  
• SQL (SQLite)  
• Pandas  
• NumPy  
• Matplotlib  
• Seaborn  
• Mlxtend (Apriori)  
• Jupyter Notebook  

---

## Strategic Business Impact Ranking

Prioritizes commercial friction points by strategic urgency and recommended focus:

| Priority Rank | Opportunity / Friction Point | Strategic Focus | Recommended Initiative |
|---|---|---|---|
| <span style="color:#e11d48; font-weight:bold;">Rank 1 (P1)</span> | **Cart Abandonment Recovery** | Post-add friction mitigation | Test exit-intent popups, simplified checkout, and email recovery |
| <span style="color:#e11d48; font-weight:bold;">Rank 1 (P1)</span> | **View → Cart Loss Mitigation** | Top-of-funnel conversion | Audit high-traffic, low-converting product pages (e.g. Cat 491) |
| <span style="color:#2563eb; font-weight:bold;">Rank 2 (P2)</span> | **Lapsed Customer Retention** | Post-purchase retention | Launch automated win-back campaigns & controlled A/B experiments |
| <span style="color:#2563eb; font-weight:bold;">Rank 2 (P2)</span> | **Cross-Selling & Basket Expansion** | Basket size growth | Deploy "Frequently Bought Together" bundles (Parent Cat 561) |
| <span style="color:#d97706; font-weight:bold;">Rank 3 (P3)</span> | **Hidden-Gem Merchandising** | Catalog visibility | Promote high-converting, low-traffic categories on search & homepage |

---

## Repository & File Architecture

```
retailrocket/
├── Ecommerce Customer Behavior & Business Performance Analysis.pdf  # Main Deliverable: Executive PDF Report
├── README.md                                                        # Project Documentation & Executive Summary
│
├── Analysis Notebooks (Python & SQL)
│   ├── 01_Data+Product_Analytics.ipynb                              # Category Opportunity Matrix & Merchandising
│   ├── 02_Visitor_Behavior_Analytics.ipynb                         # Customer Journey, Funnel & Browsing Depth
│   ├── 03_RFM_Analysis.ipynb                                        # SQL NTILE(5) RFM Segmentation
│   ├── 04_Cohort_Analysis.ipynb                                     # Acquisition Cohorts & Retention Decay
│   └── 05_Market_Basket_Analysis.ipynb                              # Apriori Association Rule Mining (Lift)
│
├── Datasets & Database
│   ├── events.csv                                                   # Raw Behavioral Event Logs (2.75M rows)
│   ├── category_tree.csv                                            # Category Hierarchy Metadata
│   ├── item_properties_part1.csv                                    # Item Properties Dataset (Part 1)
│   ├── item_properties_part2.csv                                    # Item Properties Dataset (Part 2)
│   └── ecommerce.db                                                 # SQLite Database storing structured tables
│
└── Visualizations & High-Res PNG Charts (15 Charts)
    ├── Visitor Purchase Funnel.png
    ├── Visitor Participation by Funnel Stage.png
    ├── Visitor Drop-off Between Funnel Stages.png
    ├── Visitor Journey Comparison.png
    ├── Category Opportunity Matrix.png
    ├── Top Abandoned Categories.png
    ├── Customer Segmentation (RFM).png
    ├── Visitor Segments.png
    ├── Monthly Cohort Retention (%).png
    ├── Average Customer Retention Curve.png
    ├── Hourly Conversion.png
    ├── User Activity by Hour.png
    ├── Transactions by Hour.png
    ├── Transactions by Weekday.png
    └── Events by Weekday.png
```

---

## Business Analytics Workflow

1. **Data Preprocessing & Hygiene**: Audited 2.75M raw event records, deduplicated event logs, and handled schema missing values.
2. **Funnel & Behavioral Analytics**: Mapped stage transitions across View, Add-to-Cart, and Purchase stages for browsers vs repeat buyers.
3. **Merchandising & Quadrant Segmentation**: Grouped 422 categories using median traffic and conversion thresholds into Star, Hidden Gem, Optimize, and Underperforming.
4. **RFM Segmentation via SQL Windowing**: Applied SQLite `NTILE(5)` window functions to segment buyers across Recency, Frequency, and Monetary proxies.
5. **Cohort Retention Modeling**: Constructed monthly acquisition cohorts (May–Sep 2015) to evaluate retention decay over a 4.5-month window.
6. **Market Basket Mining (Apriori Algorithm)**: Evaluated multi-item orders (`min_support = 0.001`, `min_confidence = 0.30`) to uncover high-lift product affinity rules.

> **SQL Implementation Note:**  
> SQL was used extensively for customer segmentation, cohort generation, visitor aggregation, window functions (`NTILE`), and behavioral analytics through SQLite.

---

## Key Business Outcomes

This analysis identifies five high-impact commercial opportunities:

• **Recover abandoned carts**  
• **Improve View → Cart conversion**  
• **Increase basket size**  
• **Reduce customer churn**  
• **Improve merchandising visibility**  

---

## Executive Deliverables

| Deliverable | Description | Link |
|---|---|---|
| **Executive PDF Report** | Comprehensive Executive Business Presentation | [**View PDF Report**](./Ecommerce%20Customer%20Behavior%20%26%20Business%20Performance%20Analysis.pdf) |
| **SQLite Database** | Structured event tables & queries | `ecommerce.db` |
| **Analysis Notebooks** | 5 Python + SQL Jupyter Notebooks | [`Notebooks/`](./Notebooks) |
| **Executive Visualizations** | 15 High-Resolution Charts | [`Charts/`](./Charts) |

---

## Author & Contact

**Karan Dangi**  
- **LinkedIn:** [www.linkedin.com/in/karan-dangi-4a672925b](https://www.linkedin.com/in/karan-dangi-4a672925b)  
- **Email:** [karandangi1867@gmail.com](mailto:karandangi1867@gmail.com)  
- **Dataset:** [RetailRocket E-Commerce Dataset on Kaggle](https://www.kaggle.com/datasets/retailrocket/ecommerce-dataset)  

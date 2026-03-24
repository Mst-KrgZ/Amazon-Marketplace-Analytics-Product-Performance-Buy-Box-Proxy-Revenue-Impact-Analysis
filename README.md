# Amazon Marketplace Analytics: Product Performance, Buy Box Proxy & Revenue Impact Analysis

A multi-page Power BI dashboard built to analyze Amazon marketplace sales performance from multiple business angles, including category trends, product performance, cancellation behavior, Buy Box proxy signals, private label comparison, A/B test setup, and effect size-based impact estimation.

This project goes beyond descriptive reporting and aims to support decision-making by combining financial KPIs, operational signals, product-level diagnostics, and scenario-based business impact analysis.

---

## Project Overview

This project analyzes Amazon sales and operational performance through an interactive Power BI dashboard designed for portfolio-level business intelligence and decision-support use.

The dashboard explores questions such as:

- Which product categories drive the largest share of revenue and profit?
- Which SKUs and products contribute most to revenue, profit, or loss?
- Where do cancellations and delays concentrate?
- How can Buy Box performance be approximated using operational and pricing-related signals?
- Do private label, promotion, or service-level differences show measurable impact?
- What is the estimated business upside from improving operational and commercial performance?

The result is a structured analytical framework that combines revenue, profitability, fulfillment, cancellations, product scoring, and effect size interpretation in one reporting environment.

---

## Business Objective

The main objective of this project was to transform sales and operational marketplace data into a dashboard that helps answer both performance and action-oriented business questions.

### Key business questions

- How is revenue distributed across categories and products?
- Which products generate strong results, and which ones create hidden losses?
- How do cancellations, delays, and shipping preferences affect performance?
- Which categories and products appear stronger or weaker from a Buy Box perspective?
- How does private label revenue compare with overall category revenue?
- What is the estimated upside if operational or competitive signals improve?

### Why it matters

Marketplace data often contains valuable signals across pricing, fulfillment, cancellations, and product mix, but these signals are difficult to connect without a structured BI layer. This dashboard was built to turn those signals into interpretable business views for category management, portfolio evaluation, and improvement prioritization.

---

## Scope of Analysis

### 1. Category Analysis
- Revenue contribution by product category
- Cumulative revenue concentration
- SKU distribution by category
- Shipped vs never shipped SKU comparison
- Price band analysis by category
- Monthly category performance
- Weekend behavior by category
- Shipping preference by category
- Cancellation breakdown by category

### 2. Product Analysis
- Quantity, revenue, and profit by product
- Product-level loss analysis
- Monthly net revenue trends by product
- Regional performance by country, state, and city
- SKU-level revenue ranking
- Product action flags and issue diagnosis
- Fulfillment channel profitability
- Cancelled orders by product

### 3. Buy Box Analysis
- Buy Box Proxy Score framework
- Category-level Buy Box comparison
- SKU quantity vs Buy Box status
- Monthly Buy Box trend analysis
- Buy Box category buckets (Low / Medium / High)
- Delay, cancellation, pricing, and fulfillment-related score components

### 4. Private Label Analysis
- Private label revenue vs total revenue
- Product-level private label comparison
- Revenue concentration within labeled products
- Unit price and Buy Box relationship for labeled products

### 5. A/B Test
- Promotion-based comparison
- Service-level comparison
- Private label comparison
- Simple experimental grouping structure
- Mean comparison setup for business interpretation

### 6. Effect Size Analysis
- Composite effect size proxy
- Estimated revenue gain scenarios
- Revenue recovery potential
- Category impact comparison
- Cancellation effect size analysis
- Unit profit margin vs effect size interpretation

---

## Dashboard Structure

The report is organized as a multi-page analytical dashboard with a clear progression from overview to deep-dive diagnostics.

### Home
Introduces the dashboard structure and provides navigation to the main analysis modules.

**Decision support:** Helps users move quickly from overview to focused business questions.

### Category / Category 2 / Category 3
Explores category-level performance through revenue concentration, SKU structure, price bands, monthly trends, shipping preferences, weekend effects, and cancellation patterns.

**Decision support:** Supports assortment strategy, category prioritization, pricing band review, and operational risk identification.

### Product / Product 2 / Product 3
Moves from category-level patterns to product- and SKU-level diagnostics, including top performers, loss-making products, geographic distribution, fulfillment channel analysis, and action flags.

**Decision support:** Helps identify top contributors, underperforming SKUs, margin risks, and operational follow-up areas.

### Buy Box / Buy Box 2
Introduces a Buy Box proxy framework using composite scoring and supporting dimensions such as delay, cancellation, FBA share, pricing stability, and business-order context.

**Decision support:** Supports prioritization of products or categories that may need competitiveness, fulfillment, or pricing improvements.

### Private Label / Private Label 2
Compares total revenue with labeled revenue and evaluates private label product behavior through revenue, quantity, price, and Buy Box-related views.

**Decision support:** Supports private label performance review and strategic comparison against the broader portfolio.

### AB Test
Presents grouped comparison views for promotional, service-level, and private label scenarios.

**Decision support:** Helps frame controlled comparisons and directional impact interpretation.

### Effect Size / Effect Size 2
Estimates business impact through composite scoring, category-level effect size interpretation, revenue gain scenarios, and cancellation recovery analysis.

**Decision support:** Helps translate analytical patterns into estimated business opportunity.

---

## Tech Stack

![Power BI](https://img.shields.io/badge/Power%20BI-Dashboard-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![Power Query](https://img.shields.io/badge/Power%20Query-Data%20Preparation-217346?style=for-the-badge&logo=microsoftexcel&logoColor=white)
![DAX](https://img.shields.io/badge/DAX-Calculated%20Metrics-0F6CBD?style=for-the-badge)
![Data Modeling](https://img.shields.io/badge/Data%20Modeling-Semantic%20Layer-1F4E79?style=for-the-badge)
![Excel](https://img.shields.io/badge/Excel-Data%20Source-217346?style=for-the-badge&logo=microsoftexcel&logoColor=white)

### Core tools and techniques
- **Power BI** for report design, dashboarding, and interaction
- **Power Query** for cleaning, shaping, and preparing data
- **DAX** for KPI design, scoring logic, and analytical measures
- **Data Modeling** for semantic structure and reusable analysis
- **Excel / flat-file source data** for underlying dataset handling

---

## Data Model / Architecture

The semantic model is centered around a primary analytical table containing transaction and marketplace-level fields such as:

- product category
- product name
- SKU
- purchase date
- shipping country / state / city
- ship service level
- fulfillment channel
- price band
- business-order related flags

Supporting this core table, the model includes analytical helper tables and measure tables for focused calculation logic, such as:

- **Date table** for time intelligence and monthly trend analysis
- **Buy Box measure tables** for score construction
- **Effect size measure tables** for impact estimation
- **Profit and cancellation helper logic**
- **A/B grouping tables**
- **Breakdown and score component tables**

### Modeling approach
The dashboard combines:
- a central fact-like analytical structure
- reusable measures for KPIs
- helper tables for scoring and scenario analysis
- page-specific business views built on the same semantic model

### Scoring logic
A key part of the architecture is the use of composite analytical scoring, especially in the Buy Box and Effect Size sections. Rather than relying on one isolated metric, the dashboard blends multiple operational and commercial signals to create more decision-oriented views.

---

## Data Privacy & Anonymization

The dataset used in this project has been intentionally anonymized and partially transformed to protect sensitive business information.

Key adjustments include:
- Masking of product identifiers and selected category labels
- Modification of certain numerical values while preserving analytical structure
- Generalization of geographic and operational fields where appropriate

These transformations ensure that:
- The analytical logic remains realistic
- The relationships between variables are preserved
- No sensitive or proprietary business information is exposed

The focus of this repository is on the analytical approach, data modeling, dashboard design, and decision-support framework rather than the original raw dataset.

---

## Key Metrics / KPIs

### Financial KPIs
- **Net Revenue** — total realized revenue after the selected filters
- **Net Profit** — total profit contribution generated by the selected scope
- **Cancelled Revenue** — revenue associated with cancelled transactions
- **Cancelled Orders** — count of cancelled order events
- **AOV (Average Order Value)** — average revenue per order
- **Profit Margin** — profitability ratio used to assess efficiency

### Buy Box / Operational KPIs
- **Buy Box Proxy Score** — a composite metric designed to approximate competitive positioning
- **Delay Score** — score reflecting delivery or shipping delay behavior
- **Cancellation Score** — score reflecting cancellation-related performance
- **FBA Share** — share related to fulfillment structure and its contribution to competitiveness
- **Price Score Stability** — pricing consistency / competitiveness signal
- **B2B Score** — business-order related contribution signal

### Effect Size / Impact KPIs
- **Composite Effect Size Proxy** — aggregated impact-oriented score
- **Estimated Revenue Gain** — scenario-based estimated upside under selected assumptions
- **Revenue Recovery Potential** — estimated recoverable revenue linked to operational or cancellation-related improvement
- **Effect Size Cancellation Score** — directional impact measure associated with cancellation behavior

---

## Key Features

- **Multi-page interactive dashboard** with structured navigation
- **Category- and SKU-level performance analysis**
- **Revenue, profit, cancellation, and delay diagnostics**
- **Buy Box proxy scoring framework**
- **Private label comparison views**
- **A/B test and effect size-based business interpretation**
- **Action flags and "what to fix" logic for product-level follow-up**
- **Scenario-oriented business impact estimation**

---

## Key Insights

- Revenue is highly concentrated in a small number of product categories, indicating that portfolio performance is not evenly distributed.
- Category analysis suggests that a few leading categories generate the majority of revenue, while long-tail categories contribute much less.
- SKU distribution analysis highlights a difference between total listed products and truly active shipped products, which is relevant for assortment efficiency.
- Product-level views reveal that not all high-volume products are equally profitable; some products generate visible losses and require operational or commercial review.
- Cancellation and shipping pattern analysis helps identify where operational friction is concentrated.
- Buy Box proxy analysis shows that products can be segmented into low, medium, and high competitiveness zones rather than treated as one uniform portfolio.
- The Buy Box section indicates that delay, cancellation, fulfillment structure, and pricing stability are all important signals when assessing competitive strength.
- Private label revenue appears much smaller than total category revenue in the current view, suggesting room for strategic growth or clearer positioning.
- A/B comparison views show small directional differences rather than large practical shifts, which is valuable for realistic business interpretation.
- Effect size and impact estimation help bridge the gap between descriptive analytics and business action by turning patterns into estimated opportunity.

---

## Installation / Usage

### Open locally
1. Download or clone this repository.
2. Open the `.pbix` file in **Power BI Desktop**.
3. Refresh the data if needed.
4. Navigate through the report pages from the Home screen.

### Recommended usage flow
1. Start with **Category Analysis** to understand revenue concentration and assortment structure.
2. Move to **Product Analysis** to identify top-performing, loss-making, and regionally relevant products.
3. Continue to **Buy Box Analysis** to review proxy competitiveness.
4. Review **Private Label**, **AB Test**, and **Effect Size** sections for strategic and scenario-oriented interpretation.
5. Use slicers and filters such as:
   - country
   - state
   - city
   - fulfillment channel
   - business order flags
   - category / product selections

### Interaction tips
- Use slicers to narrow the analytical scope
- Use page navigation buttons to move through the dashboard
- Reset filters with the reset button where available
- Compare category-level and product-level views together for deeper interpretation

---

## Challenges & Learnings

### Challenges
- Designing consistent KPI formatting across counts, currency values, percentages, and score-based metrics
- Building a composite Buy Box proxy score without oversimplifying the business logic
- Structuring the dashboard from category-level overview to product-level diagnostics without losing clarity
- Balancing dashboard density with readability and storytelling
- Translating operational patterns into interpretable business impact estimates
- Aligning descriptive analysis with decision-support logic

### Learnings
- A strong BI project is not only about visuals but also about semantic clarity and business framing
- Composite metrics can be powerful when the components are transparent and interpretable
- Product-level actionability adds significant value beyond standard summary reporting
- Effect size and scenario-based views can make dashboards more strategic and portfolio-oriented
- Dashboard design improves when each page answers a specific decision question

---

## Future Improvements

- Add drillthrough pages for SKU- and category-level investigation
- Standardize all page language and formatting to a single report language
- Improve map visual selection and long-term compatibility
- Add tooltips with business explanations for score components
- Expand A/B testing with more statistically robust comparison logic
- Add scenario controls for revenue, cancellation, and Buy Box improvement simulations
- Integrate external benchmarks or competitor-related signals where possible
- Add export-ready executive summary pages

---

## Conclusion

This project demonstrates how marketplace sales data can be transformed into a portfolio-level decision-support dashboard using Power BI, Power Query, DAX, and analytical scoring logic.

Instead of only reporting what happened, the dashboard was designed to help interpret where value is concentrated, where performance risks exist, and where operational or commercial improvements may create measurable upside.

From category concentration and SKU diagnostics to Buy Box proxy scoring and effect size-based opportunity estimation, the project reflects both technical BI capability and business-oriented analytical thinking.

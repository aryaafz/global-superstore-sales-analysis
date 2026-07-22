# 📊 Retail Sales & Profitability Analysis & Interactive Power BI Dashboard


## 📌 Project Overview

This project analyzes 4 years (2011–2014) of transactional data from Global Superstore, a multinational retail company operating across 7 markets and 147 countries, to uncover sales performance, profitability drivers, customer behavior, and regional trends.

The project follows a complete data analytics workflow: data cleaning, feature engineering, exploratory data analysis (EDA) in Python, and an interactive Power BI dashboard — ending with dollar-quantified, decision-ready business recommendations rather than purely descriptive charts.


---

## 🎯 Business Problems

Despite four years of transactional data, Global Superstore's leadership lacked a clear, quantified answer to:

Which specific product lines are dragging down overall profitability, and by how much?
Is the company's discounting strategy protecting or eroding margin?
Are there specific regions, states, or countries generating losses that require intervention?
Which customer segments and products should be prioritized for future investment?
Does shipping/logistics performance materially affect profitability?


---

## 🎯 Project Objectives

- Quantify sales and profit performance trends from 2011–2014 to establish a baseline.
- Identify which product categories/sub-categories are the strongest and weakest profit contributors, in dollar terms.
- Determine whether discount policy is a significant driver of unprofitability.
- Pinpoint underperforming regions, states, and countries requiring targeted intervention.
- Assess whether shipping mode/duration has a measurable impact on profit.
- Translate findings into specific, dollar-quantified recommendations.
- Build an interactive Power BI dashboard for ongoing business decision-making.

---

# 🗂 Dataset

Dataset: Global Superstore
Records: 51,290 rows across 25,035 unique orders
Period: 2011 – 2014
Scope: 7 markets, 147 countries, 3 categories, 17 sub-categories, 795 unique customers


Main features include: Order Date, Ship Date, Sales, Profit, Discount, Quantity, Category, Sub-Category, Customer, Segment, Market, Region, Country.


---

# 🧹 Data Cleaning

The following data quality checks were performed:

- ✅ Checked missing values
- ✅ Checked duplicate records
- ✅ Converted data types
- ✅ Validated date columns
- ✅ Checked negative values
- ✅ Checked data consistency
- ✅ Verified outliers
- ✅ Created clean dataset for analysis

---

# ⚙ Feature Engineering

Additional features were created to support analysis:

- Year
- Month Name
- Month Number
- Quarter
- Shipping Days

---

# 📊 Exploratory Data Analysis

EDA was conducted to answer the business questions through multiple analyses.

### Sales & Profit Performance

- Monthly Sales Trend / Monthly Profit Trend
- Sales vs Profit Trend

### Product Analysis

- Sales & Profit by Category / Sub-Category
- Profit Margin by Category / Sub-Category
- High Sales–Low Profit Analysis (Sales vs Profit scatter by sub-category)

### Customer Analysis

- Sales & Profit by Segment
- Top 10 Customers by Sales / by Profit

### Regional Analysis

- Sales & Profit by Market / Region / Country
-Top 10 States by Sales

### Discount Analysis

- Discount Distribution
- Discount vs Profit (scatter)
- Average Profit by Discount Level
- Correlation Analysis (discount, profit, profit margin, shipping days)

---

# 💡 Key Business Insights

### 📈 Overall Performance

- The company processed $12.64M in sales and $1.47M in profit over 2011–2014, an overall margin of 11.62%.
- Both sales and profit trended upward from 2011 to 2014, peaking in Q4 2014 — but profit growth was more volatile than sales growth, indicating margin, not just volume, needs active management.

### 🖥 Product Performance

- Technology is the strongest category on both sales ($4.74M) and profit ($663.8K, 14.0% margin).
- Furniture generates the second-highest sales ($4.11M) but by far the lowest margin (6.98%, $286.8K profit) — nearly matching Technology in sales while delivering less than half the profit.
- Tables is the only sub-category operating at a loss: -$64,083 on $757K in sales (-8.47% margin), driven by the highest average discount of all 17 sub-categories (29.1%).
- Copiers deliver the best unit economics among high-volume products (17.1% margin, $258.6K profit); Paper posts the highest margin overall (24.2%) despite modest sales — an underexploited opportunity.

### 👥 Customer Analysis

- Consumer is the largest and most profitable segment; Home Office is the smallest.
- Customer value doesn't always track with sales: one of the top 10 customers by sales volume was Home Office actually unprofitable (-$410), and only 4 of the top 10 customers by sales also rank in the top 10 by profit.

### 🌍 Regional Analysis

- APAC leads all markets in both sales ($3.59M) and profit ($437.6K); Central is the strongest region ($2.82M sales, $311.4K profit).
- Southeast Asia ranks 5th by sales but converts to only a ~2% profit margin — far below the 11.6% company average.
- Indonesia shows the same pattern at the country level: solid sales (~$405K, 9th highest) but only a 3.9% margin, versus 21%+ margins in comparable markets like China and India.
- Among the top 10 states by sales, Texas (-$25.7K, -15.1% margin) and National Capital (-$13.1K, -8.6% margin) are the only two operating at a loss — a localized issue rather than a market-wide one.

### 💸 Discount Analysis

- Discount correlates negatively with profit (r = -0.32) and strongly with profit margin (r = -0.85) — the strongest negative driver of profitability identified in this analysis.
- Average profit turns negative once discounts exceed ~20%, and losses deepen sharply beyond 40%.
- Shipping days show negligible correlation with profit (r = 0.0015) — logistics speed is not a meaningful profitability lever.

---

# 📈 Business Recommendations

### Product Strategy

- Cap discounts on Tables at ≤16% (in line with Chairs, which remains profitable at a similar discount level) and review its underlying cost/pricing structure. Restoring margin to the company average could recover ~$88K in annual profit from this line alone.
- Implement discount governance requiring managerial approval for discounts above 15%, prioritized for the Furniture category as a whole (6.98% margin vs ~14% for Technology/Office Supplies).
- Prioritize marketing and inventory investment toward Copiers, Phones, and Paper, which combine strong sales with healthy margins.

### Discount Strategy

- Set a maximum discount threshold around 20%, since average profit turns negative beyond this point.
- Replace blanket discounting with targeted, product-specific promotions, particularly outside Furniture.

### Regional Strategy

- Continue investing in APAC and Central, the strongest-performing market and region.
- Conduct a targeted pricing/discount audit in Texas, National Capital, Southeast Asia, and Indonesia — these are point-specific margin problems, not evidence of broader regional or market failure.

### Customer Strategy

- Strengthen loyalty programs for top profit-contributing customers (not just top-sales customers, since the two lists diverge significantly).
- Continue prioritizing the Consumer segment while exploring scalable growth in Corporate.

### Logistic

- Shipping mode/speed shows no meaningful effect on profit margin — logistics investment should be directed at cost efficiency and customer experience rather than treated as a profitability lever.

---

# 📊 Power BI Dashboard

The interactive dashboard consists of three pages, each with slicers (Year, Market, Region, Country, State) for cross-filtering.

## 1️⃣ Overview

- KPI cards: Total Sales, Total Profit, Profit Margin, Total Orders, Total Customers
- Monthly Sales Trend / Monthly Profit Trend
- Sales & Profit Contribution by Category, with Profit Margin by Category available on hover — surfacing Furniture's low-margin issue that isn't visible from absolute profit alone


<img width="4150" height="3525" alt="Global Superstore_page-0001" src="https://github.com/user-attachments/assets/692fed21-d1d6-46b2-83a6-97af3729fa90" />


---

## 2️⃣ Product & Customer Performance

- Top Sub-Categories by Sales / by Profit, with Tables automatically flagged in red as the only loss-making line
- Sales vs Profit by Sub-Category (scatter) — visually isolates Tables in the loss quadrant
- Top 10 Customers by Sales
- Sales Distribution by Customer Segment


<img width="4150" height="3525" alt="Global Superstore_page-0002" src="https://github.com/user-attachments/assets/b89b2d22-4b0a-4596-a1de-8ef60696e181" />


---

## 3️⃣ Regional & Discount Analysis

- Sales by Market, Top Regions by Sales
- Global Sales/Profit Distribution map, with margin-based legend to surface underperforming countries like Indonesia
- Impact of Discount on Profit by discount bucket — buckets above ~20% automatically flagged in red


<img width="4150" height="3275" alt="Global Superstore_page-0003" src="https://github.com/user-attachments/assets/7c64f87d-6f3b-4371-83cb-45eb902c9ef2" />


---

# 🛠 Tools & Technologies

- Python 
- Jupyter Notebook
- Power BI 

---


# 🚀 Project Highlights

✔ End-to-end Data Analytics Project

✔ Data Cleaning & Validation

✔ Feature Engineering

✔ Exploratory Data Analysis (EDA)

✔ Business Insights & Recommendations

✔ Interactive Power BI Dashboard

---

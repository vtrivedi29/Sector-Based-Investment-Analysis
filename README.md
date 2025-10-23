# Financial Sector-Based Analysis

## Overview
This repository implements a **top-down investment strategy** designed to identify undervalued securities operating in high-growth industries.  
Our approach blends **sector-level analysis**, **fundamental screening**, and **quantitative evaluation** to systematically uncover opportunities that can deliver strong returns and price appreciation over time.

---

## Strategy Framework

### 1. Industry Overview
Using the **Financial Modeling Prep (FMP) API**, we analyze **year-over-year (YoY) changes in sector sizes** to identify the fastest-growing industries.  
The assumption: **sector growth trickles down to firms**, improving their earnings and valuations over time.  
By comparing sector-level data side by side, we identify which industries are currently exhibiting the strongest growth momentum.

### 2. Identifying Top 5 Firms
From the top-performing sector, we use **S&P 500 tickers** (sourced via public datasets) to filter for **large-cap firms** and then screen for **low P/E ratios** using **yfinance**.  
Our philosophy emphasizes **undervalued companies**—those with low price-to-earnings multiples that can offer **outsized appreciation** as earnings recover or expand.

### 3. Evaluating Financial Metrics
Each selected firm is analyzed across multiple key metrics:
- **P/E ratio (30%)** – market valuation of each $ of earnings.  
- **EPS growth** – ability to leverage industry growth.  
- **Gross margin** – fundamental profitability check.  
- **Net income, revenue, and price (10% each)** – supporting performance indicators.  

The code produces **weighted scores** to rank firms and generates **visuals** (via `matplotlib`) for:
- Revenue over time  
- EPS growth trends  
- Stock prices over the past 20 years  

These visuals allow for both **quantitative analysis and qualitative interpretation**.

---

## Implementation Details

### Technologies Used
- **Python 3.x**
- **APIs:** Financial Modeling Prep (FMP), yfinance
- **Libraries:** pandas, matplotlib, numpy, requests

---

## Results & Insights
The framework outputs:
1. **Top 5 firms** in the fastest-growing sector.  
2. **Weighted ranking** based on core financial metrics.  
3. **Visual charts** for long-term trend analysis.
4. **Best investment** based on our analysis.

While the process produces quantitative scores, it also provides **room for investor judgment**—allowing qualitative insights from visuals and context to influence the final investment decision.

---

## Strengths & Limitations

### Strengths
- **Efficient:** Enables quick identification of promising securities.  
- **Dynamic:** Data updates daily via APIs.  
- **Replicable:** Fully automatable and reusable for future periods.  

### Limitations
- **Subjectivity in weightings:** Different investors may prefer different metric emphasis.  
- **Data quality:** Metrics pulled from APIs like yfinance may slightly differ from restated filings.  
- **Assumptions:** Strategy assumes sector growth translates to firm-level performance.


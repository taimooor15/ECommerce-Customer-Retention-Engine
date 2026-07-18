# Multi-Channel Customer Retention & Churn Optimization Engine

## 📊 Business Problem & Context
In the e-commerce and retail sectors, acquiring a new customer can cost up to **5x more** than retaining an existing one. Without deep visibility into customer lifecycles, marketing departments waste budget on generic campaigns rather than targeting high-value users showing signs of attrition.

This project delivers an end-to-end data analytics pipeline that transforms raw transactional sales data into programmatic business strategies by identifying exact cohort drop-off velocities and segmenting customer bases accurately.

---

## 🛠️ Tech Stack & Architecture
- **Python 3.x** - Core data processing engine.
- **Pandas & NumPy** - Algorithmic data cleaning, outlier mitigation, and vector calculations.
- **Matplotlib & Seaborn** - Cohort matrix rendering and statistical distributions.
- **Data Source:** UCI Machine Learning Repository / Kaggle Online Retail Dataset (Real-world transaction logs from a UK-based registered non-store retail business).

---

## 🚀 Analytical Execution Breakdown

### 1. Data Quality Assurance & Cleaning
Raw enterprise data is filled with missing tracking points. The pipeline explicitly handles:
- Stripping out missing structural identifiers (`CustomerID`) where behavioral mapping is impossible.
- Programmatically removing cancelled transactions (invoices prefixed with 'C') and extreme financial anomalies (negative quantities or zero unit prices).
- Explicitly parsing unified datetime objects to align structural transaction histories.

### 2. Time-Based Cohort Retention Matrix
Customers are grouped into monthly cohorts based on the date of their very first transaction. A rolling user matrix tracks return behavior across subsequent active months to pinpoint the exact moment churn accelerates.

### 3. RFM Behavioral Segmentation Engine
Using statistical quantiles, every distinct customer profile is mathematically evaluated across three distinct parameters:
- **Recency (R):** Days elapsed since the customer's last invoice date.
- **Frequency (F):** The total number of unique successful transactions completed.
- **Monetary (M):** Total lifetime gross expenditure driven by the individual profile.

---

## 💡 Key Business Insights Revealed

- **The Month 1 Drop-off Cliff:** Across over 75% of historical user cohorts, customer retention drops below **25%** by the end of their first active month. 
  - *Strategic Recommendation:* A generic marketing newsletter at Day 30 is too late. The business must deploy an automated behavioral email trigger between Day 14 and Day 21 offering secondary incentives to flatten this curve.
- **High-Value Concentration:** The calculated `Champions / VIP` segment constitutes less than **10%** of total unique customer profiles, yet accounts for nearly **40%** of cumulative company revenue.
  - *Strategic Recommendation:* Implement a dedicated loyalty program or priority support system to ring-fence this demographic against competitor poaching.

---

## 📦 How to Run Locally

1. Clone this repository to your machine:
   ```bash
   git clone [https://github.com/taimooor15/ECommerce-Customer-Retention-Engine.git](https://github.com/taimooor15/ECommerce-Customer-Retention-Engine.git)


## Install the necessary analysis environments:
pip install -r requirements.txt

Download the raw sales data, place it in the /data/ folder as online_retail.csv, and execute the notebooks/churn_analysis.ipynb file inside VS Code.

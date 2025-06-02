# peak_volatility_category_analysis_nov2019

This project analyzes customer purchase behavior to uncover **daily volatility patterns** and **category-level risks** in e-commerce transactions. Using real user activity data from November 2019, we compute rolling metrics and visualize key risk signals, including **order fluctuation**, **average order value**, and **top-performing product categories during high-volatility periods**.

---

## Project Overview

- **Dataset:** [Kaggle - E-Commerce Behavior Data](https://www.kaggle.com/datasets/mkechinov/ecommerce-behavior-data-from-multi-category-store)
- **Timeframe:** November 2019
- **Focus Areas:**
  - Daily order trends and purchase volatility
  - Revenue and average order value (AOV) metrics
  - Identification of peak volatility days
  - Analysis of most affected product categories

---

## 📁 File Structure
├── 2019-Nov.csv # Raw dataset (November 2019)
├── daily_risk_metrics.csv # Aggregated daily metrics
├── peak_volatility_category_analysis.ipynb # Main analysis notebook
├── Risk_Exposure_Analysis.ipynb # Daily volatility & trend analysis
├── /visuals # Optional: output charts
└── README.md # Project documentation


---

## 📈 Key Visualizations

### 1. Daily Total Orders & Volatility  
A dual-axis line chart showing:
- 📘 **Daily Total Orders**  
- 🟠 **7-day Rolling Volatility** of order counts  

Helps identify fluctuations and unusual customer behavior patterns.

### 2. Top 10 Product Categories During Peak Volatility  
A horizontal bar chart showing:
- Most frequently ordered product categories between **Nov 16–18**
- Useful for identifying categories most sensitive to behavior surges

---

## 🧮 Methodology

- **Data Preprocessing**
  - Convert timestamps to daily granularity
  - Filter only `'purchase'` events
- **Daily Metrics Computation**
  - Total Orders = unique `user_session` per day
  - Total Users = unique `user_id` per day
  - Total Revenue = sum of `price`
  - AOV = mean of `price`
- **Volatility Metric**
  - `Order Volatility = Rolling 7-day Std. Dev. of Total Orders`
- **Peak Period Analysis**
  - Selected top 3 volatility days: `Nov 16–18`
  - Aggregated purchases by `category_code`

---

## 🛠️ Tools & Technologies

- **Language:** Python 3
- **Libraries:**
  - `pandas` – data wrangling and aggregation
  - `matplotlib` – data visualization
- **Environment:** Jupyter Notebook

---

## 📌 Key Insights

- Behavioral volatility can signal operational risk or opportunity.
- Rolling order standard deviation highlights peak shopping periods.
- Electronics and clothing categories were most affected during spikes.
- Order trends and volatility analysis can inform inventory planning and marketing focus.


---

## About Me

Hi! I'm a data analytics graduate student passionate about using data to drive strategic insights.  
This project was created as part of my data portfolio to demonstrate applied skills in:

- Risk metrics
- Behavioral analysis
- Data storytelling



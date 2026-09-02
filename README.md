# 🚀 AI-Powered Demand & Inventory Intelligence Platform

An end-to-end Machine Learning platform for **retail demand forecasting, customer risk scoring, inventory planning, and business intelligence**.

The project analyzes historical retail transaction data, identifies sales patterns, forecasts future revenue, segments customers using RFM analysis, and generates actionable business recommendations.

---

## 📌 Project Overview

Retail businesses need to accurately predict future demand while maintaining the right inventory levels and retaining valuable customers.

This project combines **Exploratory Data Analysis, Feature Engineering, Machine Learning Forecasting, Customer Risk Scoring, and Business Analytics** into a single intelligence platform.

### 🎯 Key Objectives

* Forecast future retail demand and revenue
* Identify important sales and demand patterns
* Reduce inventory overstock and stockout risks
* Identify high-value and at-risk customers
* Support customer retention strategies
* Compare multiple forecasting algorithms
* Generate business recommendations from data

---

## 🏗️ Project Architecture

```text
Raw Retail Data
       ↓
Data Loading
       ↓
Data Cleaning
       ↓
Exploratory Data Analysis
       ↓
Feature Engineering
       ↓
Demand Forecasting
       ↓
Model Evaluation
       ↓
Customer RFM Analysis
       ↓
Customer Risk Scoring
       ↓
Business Insights
       ↓
Inventory & Customer Recommendations
       ↓
Dashboard / Deployment
```

---

## 📊 Dataset

The project uses historical retail transaction data containing information such as:

| Column      | Description                  |
| ----------- | ---------------------------- |
| Invoice     | Invoice / transaction number |
| StockCode   | Product identifier           |
| Description | Product description          |
| Quantity    | Number of units purchased    |
| InvoiceDate | Transaction date and time    |
| Price       | Unit price                   |
| Customer ID | Customer identifier          |
| Country     | Customer country             |

### Derived Variable

```text
Revenue = Quantity × Price
```

The dataset contains transactions from **2009–2011** and is used to analyze customer behavior, product performance, revenue trends, and demand patterns.

---

# 🔄 Project Workflow

## 1️⃣ Data Cleaning

The raw dataset was processed to improve data quality.

### Cleaning steps

* Combined multiple yearly datasets
* Removed duplicate transactions
* Converted date columns
* Converted numerical columns
* Removed cancelled invoices
* Removed invalid quantities
* Removed invalid prices
* Created Revenue
* Handled missing Customer IDs
* Created time-based features

---

## 2️⃣ Exploratory Data Analysis

EDA was performed to understand the underlying business patterns.

### Analysis includes

* Monthly revenue trends
* Monthly quantity trends
* Top countries by revenue
* Top products by revenue
* Top products by quantity
* Top customers by revenue
* Revenue distribution
* Quantity distribution
* Revenue by day of week
* Correlation analysis
* Quarterly revenue analysis

---

## 3️⃣ Feature Engineering

Time-series and business features were created for Machine Learning.

### Features include

* Year
* Month
* Quarter
* Month Index
* Revenue Lag 1
* Revenue Lag 2
* Revenue Lag 3
* Revenue Lag 6
* Rolling Revenue Mean
* Quantity Lag Features
* Orders Lag
* Customer Lag
* Product Lag
* Revenue Growth
* Average Order Value
* Month Sin
* Month Cos

Lag and rolling features are constructed using previous observations to reduce the risk of data leakage.

---

# 🤖 Machine Learning Forecasting

Multiple forecasting approaches were evaluated.

### Models

* Random Forest
* XGBoost
* LightGBM
* ARIMA
* SARIMA
* Prophet

The models were evaluated using time-based validation rather than random train/test splitting.

### Evaluation Metrics

| Metric | Purpose                                    |
| ------ | ------------------------------------------ |
| MAE    | Measures average absolute prediction error |
| RMSE   | Penalizes larger prediction errors         |
| MAPE   | Measures percentage forecasting error      |

The best-performing model is selected based on the evaluation results.

---

# 👥 Customer Risk Scoring

Customer behavior is analyzed using **RFM Analysis**.

### RFM Components

**Recency**
How recently the customer made a purchase.

**Frequency**
How often the customer purchased.

**Monetary**
How much revenue the customer generated.

### Customer Segments

* 🏆 Champions
* 💎 Loyal Customers
* 🌱 New / Promising
* ⚠️ At Risk
* 🔴 Lost Customers
* ⭐ Potential Loyalists

---

# 🚨 Customer Risk Classification

Customers are assigned a risk score based on:

* Recency
* Frequency
* Monetary value

### Risk Levels

```text
Low Risk
Medium Risk
High Risk
```

High-value customers with increasing recency and declining engagement can be prioritized for retention campaigns.

---

# 📈 Model Evaluation & Visualization

The project contains multiple visualizations for evaluating model performance and business behavior.

### 10 Key Visualizations

1. Actual vs Predicted Revenue
2. MAPE Comparison
3. RMSE Comparison
4. MAE Comparison
5. Forecast Error Distribution
6. Top 10 Feature Importance
7. Historical Revenue + Future Forecast
8. Next 3 Months Forecast Comparison
9. Revenue by Customer Segment
10. Average Order Value by Country

---

# 💡 Business Insights

The platform helps answer questions such as:

* Which products generate the most revenue?
* Which customers contribute the most revenue?
* Which customers are at risk of leaving?
* What is the expected future revenue?
* Which features are most important for forecasting?
* Which countries have higher average order values?
* How should inventory be planned?
* Which customers should receive retention campaigns?

---

# 📦 Inventory Recommendations

The forecasting system can support inventory decisions by:

### High predicted demand

Increase inventory availability to reduce potential stockouts.

### Low predicted demand

Avoid excessive purchasing and reduce inventory holding costs.

### Seasonal demand

Prepare inventory before periods of expected demand increases.

### Product prioritization

Focus inventory planning on high-revenue and high-demand products.

---

# 🎯 Customer Retention Recommendations

### High-Risk Customers

Launch targeted win-back campaigns.

### High-Value At-Risk Customers

Provide personalized offers, loyalty benefits, or priority engagement.

### Loyal Customers

Use loyalty programs and cross-selling opportunities.

### New Customers

Use onboarding campaigns and personalized recommendations.

---

# 🛠️ Technology Stack

### Programming

* Python
* Pandas
* NumPy

### Data Visualization

* Matplotlib
* Seaborn

### Machine Learning

* Scikit-learn
* XGBoost
* LightGBM

### Time Series Forecasting

* ARIMA
* SARIMA
* Prophet

### Development

* Google Colab
* Jupyter Notebook
* Git
* GitHub

### Dashboard

* Streamlit

---

# 📂 Project Structure

```text
AI-Powered-Demand-Inventory-Intelligence-Platform/
│
├── data/
│   └── Dataset.xlsx
│
├── notebooks/
│   ├── 01_Data_Cleaning.ipynb
│   ├── 02_EDA.ipynb
│   ├── 03_Feature_Engineering.ipynb
│   ├── 04_Forecasting.ipynb
│   ├── 05_Customer_Risk_Scoring.ipynb
│   └── 06_Model_Evaluation.ipynb
│
├── outputs/
│   ├── feature_engineered_sales_data.csv
│   ├── final_model_evaluation.csv
│   ├── best_model_predictions.csv
│   ├── feature_importance.csv
│   ├── future_revenue_forecasts.csv
│   ├── customer_risk_scores.csv
│   ├── high_risk_customers.csv
│   └── high_value_at_risk_customers.csv
│
├── app/
│   └── app.py
│
├── requirements.txt
│
└── README.md
```

---

# ▶️ How to Run

## 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/AI-Powered-Demand-Inventory-Intelligence-Platform.git
```

## 2. Navigate to the project

```bash
cd AI-Powered-Demand-Inventory-Intelligence-Platform
```

## 3. Install dependencies

```bash
pip install -r requirements.txt
```

## 4. Run the notebooks

Open the notebooks using:

```bash
jupyter notebook
```

Or upload the notebooks to **Google Colab**.

---

# 📊 Expected Outputs

The project produces:

* Cleaned retail transaction data
* EDA visualizations
* Engineered time-series features
* Forecasting model results
* Model comparison table
* Feature importance analysis
* Future revenue forecasts
* Customer RFM scores
* Customer risk levels
* High-value at-risk customer list
* Business recommendations

---

# 🚀 Future Improvements

* Real-time inventory monitoring
* SKU-level demand forecasting
* Automated stockout alerts
* Deep Learning forecasting using LSTM
* Real-time Streamlit dashboard
* Automated model retraining
* Cloud deployment
* Recommendation engine
* Automated email alerts for high-risk customers

---

# 👨‍💻 Author

**Tamil Arasan**

Machine Learning | Data Science | Python | Business Analytics

---

## ⭐ Project Highlights

> **From historical retail transactions to AI-powered demand forecasting and customer intelligence.**

This project demonstrates an end-to-end approach to solving real-world retail problems using **Data Science, Machine Learning, Time-Series Forecasting, Customer Analytics, and Business Intelligence**.

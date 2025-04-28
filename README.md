# Sales-Forecasting-Challenge

## Project Overview
This notebook predicts the next 7 days of daily revenue for a UK-based online gift retailer using historical sales data from December 1, 2010 through December 9, 2011. We load and clean transaction‐level records, aggregate to daily revenue, explore trends and seasonality, and fit a Prophet model to generate short-term forecasts with uncertainty bounds.

## Dataset
- **Source:** Kaggle – E-Commerce Data  
- **Period:** 2010-12-01 to 2011-12-09  
- **Fields:**  
  - `InvoiceNo`: Unique transaction line ID  
  - `StockCode`: Product code  
  - `Description`: Product name  
  - `Quantity`: Units sold (negative = return)  
  - `InvoiceDate`: Timestamp  
  - `UnitPrice`: Price per unit  
  - `CustomerID`: Customer identifier (nullable)  
  - `Country`: Customer’s country  

## Prerequisites
- Python 3.8+  
- pandas  
- matplotlib  
- prophet  

Install dependencies with:
```bash
pip install pandas matplotlib prophet

**Notebook Structure**
Data Preprocessing

Load CSV, parse dates

Drop rows missing Quantity or UnitPrice

Compute Revenue = Quantity × UnitPrice

Drop rows with missing CustomerID (guest checkouts)

Exploratory Data Analysis

Aggregate to daily totals

Plot historical revenue trend

Identify weekly and yearly seasonality patterns

Forecasting with Prophet

Rename to ds (date) and y (revenue)

Instantiate and fit Prophet with weekly & yearly seasonality

Generate 7-day future dataframe

Predict and plot:

Full forecast + 95% confidence intervals

Decomposed components (trend, weekly, yearly)

Results & Interpretation

Point forecasts and confidence bounds for next 7 days

Seasonal insights (weekday vs weekend, holiday effects)

Business recommendations for inventory, staffing, and promotions

Usage
Open the notebook daily_sales_forecast.ipynb.

Update the file path to your CSV data.

Run all cells in order.

Examine the forecast table and plots to make data‐driven decisions.

Investment Risk & Volatility Monitor

A dynamic financial risk monitoring dashboard built using Python and Tableau to analyze stock performance, measure portfolio risk, and simulate market shock scenarios.
Project Objective

To build an interactive portfolio risk monitoring system that:
1.Calculates stock Log Returns
2.Measures Volatility
3.Computes Value at Risk (VaR 95%)
4.Analyzes Stock Correlation
5.Performs Monte Carlo Simulation
6.Allows dynamic What-If Market Shock Analysis
7.Displays Executive-Level KPIs.

Tech Stack:
Python
Pandas
NumPy
yFinance
Tableau
Dynamic Parameters
Calculated Fields
Interactive Dashboards
CSV Files for Data Exchange

Key Features
1️⃣ Log Return Calculation:
Daily log returns calculated using:
l𝑜𝑔𝑅𝑒t𝑢𝑟𝑛=𝑙𝑛(𝑃𝑡/𝑃𝑡−1)LogReturn=ln(Pt/Pt−1)

2️⃣ Dynamic What-If Analysis:
A Tableau parameter allows users to simulate:
"What if the Tech sector drops by 10%?"
This dynamically recalculates:
Adjusted Returns
Portfolio Volatility
Value at Risk
Portfolio Distribution

3️⃣ Correlation Heatmap:
Visual representation of correlation between stocks:
Columns → Stock 1
Rows → Stock 2
Color → Correlation
Marks → Square
Used to identify diversification opportunities.

4️⃣ Monte Carlo Simulation
Simulates multiple possible future portfolio values based on historical return distribution.
Histogram created using:
PortfolioValue (Bins)
Count
Marks → Bar

5️⃣ Executive Summary Dashboard
Designed for decision-makers.
Displays:
📉 Current VaR (95%)
📊 Portfolio Volatility
📉 Maximum Drawdown
💰 Current Portfolio Value
Clean KPI-style layout for quick interpretation.

🔄 Data Automation
Market data can be refreshed using Python script:
import yfinance as yf
import pandas as pd
stocks = ["AAPL","MSFT","GOOGL","NVDA","META"]
data = yf.download(stocks, start="2020-01-01")
data.to_csv("log_returns.csv")

Dashboard updates after refreshing data source in Tableau.

✅ Financial Accuracy Validation
All risk metrics were verified using NumPy:
VaR → np.percentile(returns, 5)
Volatility → np.std(returns) * np.sqrt(252)
Correlation → returns.corr()
Ensuring alignment with industry-standard financial calculations.
 Business Impact
This system helps:
Portfolio Managers monitor risk exposure
Analysts simulate stress scenarios
Executives view high-level KPIs instantly
Investors understand diversification risk



👤 Author

Jayasudha MVS
Aspiring Data Analyst | Financial Analytics Enthusiast


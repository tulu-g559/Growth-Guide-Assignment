# 💹 AlgoTrading_GG

A Python-based **mini algo-trading prototype** that connects to real-time stock APIs, implements technical trading strategies, uses machine learning for signal prediction, and automates trade logging and analytics in Google Sheets.

> 🚀 Built as part of an internship assessment assignment.  
> 📈 Focused on trading logic, automation, ML modeling, and deployment-readiness.

---

## 📌 Features

- ✅ **Stock Data Ingestion** from Yahoo Finance API
- ✅ **Technical Indicators**: RSI, MACD, 20-DMA, 50-DMA
- ✅ **Trading Strategy Logic**: RSI < 30 + 20DMA crossover
- ✅ **Machine Learning Predictions**:
    - Logistic Regression
    - Random Forest
    - XGBoost
- ✅ **Best model per ticker auto-selected** with accuracy tracking
- ✅ **P&L Simulation** based on signal outcome
- ✅ **Google Sheets Automation**:
  - Trade logs
  - P&L summaries
  - Win ratios
  - Model summary
- ✅ **Telegram Alerts** for signals and pipeline status
- ✅ **Fully Modular & Documented Codebase**

---

## 📊 Strategy Logic

BUY Signal triggered when:
- RSI < 30 (Oversold condition)
- 20DMA crosses above 50DMA (Bullish crossover)


Each ticker undergoes training with:
*   LogisticRegression
*   RandomForestClassifier
*   XGBoostClassifier
    

Features used:
*   RSI, MACD, MACD Signal, Volume, 20DMA, 50DMA

> The model with **highest test accuracy** is selected and saved.

📤 Google Sheets Integration
----------------------------

Your output is auto-uploaded to:

*   🟢 Individual stock worksheets
*   🟡 `PNL_Summary`: Exit strategy-based returns
*   🔵 `SUMMARY`: ML Accuracy, total signals, win %
*   🟣 `Win_Ratios`: Simplified win-loss stats
    

📦 Output Examples
------------------

| Ticker        | ML Model     | Accuracy | Win Ratio | Total Signals |
| ------------- | ------------ | -------- | --------- | ------------- |
| ADANIENT.NS   | Logistic     | 46.67%   | 62.50%    | 43            |
| BAJFINANCE.NS | Logistic     | 60.00%   | 72.72%    | 59            |
| COALINDIA.NS  | RandomForest | 53.33%   | 66.66%    | 48            |


| App Interface Screenshot | Telegram Alert Screenshot |
|--------------------------|---------------------------|
| <img src="https://github.com/user-attachments/assets/336c304d-ca9b-4914-ba1c-b6fa9ef70765" height="350" width="160"/> | <img src="https://github.com/user-attachments/assets/016f7b21-615e-438e-a2dc-2d7d07d6e43d" height="350" width="160"/> |


🛠️ Technologies Used
---------------------

*   Python (v3.10+)
*   yfinance (API)
*   pandas, numpy
*   scikit-learn, xgboost
*   gspread + Google Auth
*   Google Colab + Drive
*   Telegram Bot API
    

📂 File Structure
-----------------
```
📁 Growth Guide Assignment/
├── AlgoTrading_GG.ipynb               # Main prototype notebook
├── README.md                          # Project overview
├── 📤 Google Sheet: AlgoTrading       # Auto-updated live data
└── 📧 Telegram alerts
```

📬 How to Run
-------------
    1.  Clone or open the notebook in Google Colab
    2.  Authenticate with Google for Sheets & Drive
    3.  Set tickers + date range (default: last 6 months)
    4.  Run run_algo_trading_pipeline()
    5.  View results in:
        *   Google Sheet (AlgoTrading)
        *   Telegram (if enabled)
        

✅ Evaluation Mapping
--------------------

| Criterion                    | Met? | Details                              |
| ---------------------------- | ---- | ------------------------------------ |
| API/Data Handling            | ✅    | yfinance, robust fetch, NaN handling |
| Strategy Logic               | ✅    | Multi-condition RSI + MA crossover   |
| ML/Analytics                 | ✅    | 3 models, dynamic selection, saved   |
| Sheets Automation            | ✅    | Auto-uploads with formatting         |
| Code Quality & Documentation | ✅    | Modular, logged, Markdown-documented |

#

👤 Author
---------

## **Arnab Ghosh**

3rd Year Undergraduate | AIML & Hackathon Enthusiast
* [LinkedIn](https://www.linkedin.com/in/tulug559) 
* [GitHub](https://github.com/tulu-g559)

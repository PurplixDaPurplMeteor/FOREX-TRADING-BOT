# 📈 FOREX TRADING (Machine Learning Based Trading System)

## Overview

This project is a **machine learning–based Forex trading system** designed to analyze historical market data, train predictive models, backtest trading strategies, and predict the **next candle market direction (UP / DOWN)**.

The system focuses mainly on **EURUSD** and supports **multiple timeframes** such as **5M, 10M, 15M, 20M, and 30M**, using historical data from **MetaTrader 5, Dukascopy, and Yahoo Finance**.

This project is intended for **educational, experimental, and research purposes**, showing how machine learning can be applied to Forex trading and strategy evaluation.

---

## Key Features

- Machine learning–based price direction prediction
- Multi-timeframe model support (5M → 30M)
- Model loading and inference
- Historical backtesting engine
- MT5, Dukascopy, and Yahoo Finance data support
- Automated preprocessing and feature engineering
- Trade logging and performance evaluation

---

## Project Structure

FOREX TRADING/
│
├── ALL_MODELS/
│ ├── EURUSD_lgbm_bundle.pkl
│ ├── EURUSD_lgbm_T_5M.pkl
│ ├── EURUSD_lgbm_T_10M.pkl
│ ├── EURUSD_lgbm_T_15M.pkl
│ ├── EURUSD_lgbm_T_20M.pkl
│ ├── EURUSD_lgbm_T_30M.pkl
│
├── CSV_FILES/
│ ├── BACKTEST_DATA.csv
│ ├── dukascopy_EURUSD_5M.csv
│ ├── EURUSD_Exchange_Rate_Dataset.csv
│ ├── MT5_5M_BT_EURUSD_Dataset.csv
│ ├── MT5_5M_EURUSD_Exchange_Rate_Dataset.csv
│ ├── MT5_5M_XAUUSD_Exchange_Rate_Dataset.csv
│ ├── MT5_10M_EURUSD_Exchange_Rate_Dataset.csv
│ ├── MT5_EURUSD_Exchange_Rate_Dataset.csv
│ ├── Trade_log.csv
│
├── PY_FILES/
│ ├── ALL_BACKTEST.py
│ ├── ALL_PRED_NXT.py
│ ├── ALL_PROCESS.py
│ ├── Dukascopy_Data.py
│ ├── func.py
│ ├── Get_dataMT5.py
│ ├── Get_dataYF.py
│ ├── Load_model.py
│ ├── PRED_NEXT.py
│ ├── Preprocessing.py
│ ├── test.py
│
└── requirements.txt


---

## Folder Explanation

### ALL_MODELS

This folder contains **pre-trained machine learning models** saved as `.pkl` files.

Each model is trained for a **specific timeframe**:

- `EURUSD_lgbm_T_5M.pkl` → 5-minute timeframe  
- `EURUSD_lgbm_T_10M.pkl` → 10-minute timeframe  
- `EURUSD_lgbm_T_15M.pkl` → 15-minute timeframe  
- `EURUSD_lgbm_T_20M.pkl` → 20-minute timeframe  
- `EURUSD_lgbm_T_30M.pkl` → 30-minute timeframe  

`EURUSD_lgbm_bundle.pkl` usually contains:
- The trained model
- Feature column names
- Other metadata required for prediction

Each model is optimized for its timeframe and loaded dynamically during prediction or backtesting.

---

### CSV_FILES

This folder stores **all datasets and logs** used by the system.

Important files include:

- `BACKTEST_DATA.csv`  
  Cleaned dataset used specifically for strategy backtesting.

- `dukascopy_EURUSD_5M.csv`  
  Historical EURUSD data downloaded from Dukascopy.

- `MT5_*_Exchange_Rate_Dataset.csv`  
  Market data collected directly from MetaTrader 5.

- `Trade_log.csv`  
  Automatically generated trade history containing executed trades, outcomes, and performance metrics.

These datasets are used for:
- Training models
- Backtesting strategies
- Evaluating model performance
- Debugging and analysis

---

### PY_FILES

This folder contains **all Python scripts** responsible for data processing, prediction, and evaluation.

Key scripts:

- `ALL_PROCESS.py`  
  Handles full data processing pipeline including cleaning, indicator calculation, and feature preparation.

- `Preprocessing.py`  
  Focuses on transforming raw OHLCV data into machine-learning-ready format.

- `Load_model.py`  
  Loads trained models from the `ALL_MODELS` directory.

- `ALL_PRED_NXT.py`  
  Runs next-candle predictions across multiple timeframes.

- `PRED_NEXT.py`  
  Executes a single next-candle prediction for real-time or testing usage.

- `ALL_BACKTEST.py`  
  Performs historical backtesting, evaluates trade outcomes, and logs results.

- `Get_dataMT5.py`  
  Fetches historical or live market data from MetaTrader 5.

- `Get_dataYF.py`  
  Fetches market data using Yahoo Finance API.

- `Dukascopy_Data.py`  
  Downloads and formats Forex data from Dukascopy.

- `func.py`  
  Contains helper and utility functions shared across the project.

---

### requirements.txt

This file lists all required Python libraries needed to run the project.
  numpy
  pandas
  scikit-learn
  lightgbm
  catboost
  joblib
  MetaTrader5
  ta


Installation Guide
Step 1: Clone the Repository

Plain Text

git clone https://github.com/yourusername/forex-trading.git
cd FOREX-TRADING

Step 2: Install Dependencies

Plain Text

pip install -r requirements.txt

How to Use the Project
🔹 Run Data Processing

Plain Text

python PY_FILES/ALL_PROCESS.py


This prepares raw CSV data for training or prediction.

🔹 Run Backtesting

Plain Text

python PY_FILES/ALL_BACKTEST.py


This will:
Simulate trades on historical data
Calculate win rate
Log trades into Trade_log.csv

🔹 Predict Next Candle Direction
python PY_FILES/ALL_PRED_NXT.py
or
python PY_FILES/PRED_NEXT.py




The model outputs:
- Predicted direction (UP / DOWN)
- Probability confidence scores

---

## YouTube Tutorials

Detailed explanations of this project, including **code walkthroughs, strategy logic, and machine learning concepts**, are available on my YouTube channel:

📺 **Ezee Kits**  
🔗 https://www.youtube.com/@Ezee_Kits

Content includes:
- Python programming
- Machine learning
- Forex trading automation
- Data analysis
- Engineering concepts

---

## Disclaimer ⚠️

This project is for **educational and research purposes only**.  
Forex trading involves substantial risk, and no trading system can guarantee profits.

The author is **not responsible for any financial losses** incurred from using this software.

---

## Author

**Ezee Kits**  
Electrical & Electronics Engineer  
Python Developer | Machine Learning Enthusiast  

YouTube: https://www.youtube.com/@Ezee_Kits


# 📈 Stock-Market-prediction

A Python-based toolkit for fetching historical stock prices, exploring time-series patterns, and forecasting future values using classical statistical models like ARIMA and SARIMA.  
Ideal for data scientists, students, and developers interested in learning and applying time-series forecasting techniques.


## 📚 Table of Contents

- [Features](#features)  
- [Demo](#demo)  
- [Getting Started](#getting-started)  
- [Prerequisites](#prerequisites)  
- [Installation](#installation)  
- [Usage](#usage)  
  - [Fetch & Prepare Data](#fetch--prepare-data)  
  - [Exploratory Analysis](#exploratory-analysis)  
  - [Train & Evaluate Models](#train--evaluate-models)  
  - [Make Predictions](#make-predictions)  
- [Project Structure](#project-structure)  
- [Results & Metrics](#results--metrics)  
- [Customization](#customization)  
- [Contributing](#contributing)  
- [License](#license)  
- [Contact](#contact)

---

## ✅ Features

- 📅 Download historical stock data using `yfinance`
- 📊 Perform rolling mean & standard deviation analysis
- 🔍 Decompose time series into trend, seasonality, and residuals
- 🧠 Fit ARIMA & SARIMA models for forecasting
- 📈 Visualize actual vs predicted values
- 📄 Export forecasts to CSV for further analysis


## 🚀 Getting Started

### 🧰 Prerequisites

- Python 3.7+
- Git
- (Optional but recommended) [conda](https://docs.conda.io/) for environment management

### ⚖️ Installation

```bash
# Clone the repository
git clone https://github.com/abhi6112/Stock-Market-prediction.git
cd Stock-Market-prediction

# Create a virtual environment
python3 -m venv venv

# Activate environment
# macOS/Linux
source venv/bin/activate
# Windows
venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

## 🛠️ Usage

### 📄 Fetch & Prepare Data

```bash
python scripts/fetch_data.py --ticker AAPL --start 2015-01-01 --end 2024-06-01
```
> Produces: `data/AAPL.csv` (includes Open, High, Low, Close, Adj Close, Volume)



### 📊 Exploratory Analysis

Open the notebook:
```
notebooks/eda.ipynb


Includes:
- Plotting Rolling Mean & Std Dev
- ADF Test for Stationarity
- Seasonal Decomposition of Time Series



### 🧪 Train & Evaluate Models

```bash
python scripts/train_model.py \
  --model arima \
  --order 5 1 2 \
  --output models/arima.pkl


Generates:
- Trained model `.pkl` file
- `reports/arima_metrics.json` with metrics like MSE, RMSE, MAE



### 🔮 Make Predictions

```bash
python scripts/predict.py \
  --model models/arima.pkl \
  --periods 30 \
  --output forecasts_30d.csv


Then view the forecast:

```bash
python scripts/plot_forecast.py \
  --historical data.csv \
  --forecast forecasts_30d.csv


## 📂 Project Structure


Stock-Market-prediction/
├── data/
├── scripts/
│   ├── fetch_data.py
│   ├── train_model.py
│   ├── predict.py
│   └── plot_forecast.py
├── notebooks/
│   └── eda.ipynb
├── models/
├── reports/
├── forecasts/
├── requirements.txt
└── README.md
```

---

## 📊 Results & Metrics

- 📉 Evaluation metrics: MSE, RMSE, MAE
- 📊 Visual comparison of actual vs predicted prices
- 🔁 Cross-validation for model performance



## ⚙️ Customization

- Switch between ARIMA and SARIMA using CLI flags
- Modify rolling window sizes and forecast periods
- Extend to multivariate models (future feature)



## 🤝 Contributing

Contributions, issues, and feature requests are welcome!  
Feel free to fork the repo and submit a pull request.



## 📝 License

This project is licensed under the MIT License. See `LICENSE` file for details.



## 📬 Contact

**Abhishek S.** – [GitHub](https://github.com/abhi6112)




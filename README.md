# 📈 Algorithmic Trading Strategy Development & Portfolio Optimization

This project implements **momentum-based trading strategies** enhanced with **Stop-Loss (SL)** and **Take-Profit (TP)** refinements. Using 10 NASDAQ stocks (2015–2025), it compares multiple strategies, performs post-COVID recovery analysis, and optimizes portfolio allocation using Sharpe ratio blending.

---

## 🚀 Features
✔ Momentum-based signal generation using:
- 30-day return
- Moving Average Crossover (MA20 > MA50)
- RSI > 55

✔ Strategies implemented:
- **Buy & Hold**
- **Momentum Only**
- **SL/TP + Hold Days**
- **SL/TP Final (Dynamic Exit)**

✔ Key Analysis:
- Risk-adjusted metrics: **Sharpe Ratio**, **Max Drawdown**
- Post-COVID price recovery timelines
- Sharpe-based **portfolio blending optimization**

---

## 📂 **Project Structure**

- `README.md` – Project documentation and usage instructions  
- `requirements.txt` – Python dependencies for reproducibility  
- `.gitignore` – Ignore unnecessary files like CSVs, logs, and checkpoints  


- `notebooks/` – Jupyter notebooks for implementation  
  - `Task3_Adv_Analytics.ipynb` – Main notebook implementing data processing, feature engineering, strategy simulation, and portfolio optimization  


- `data/` – Raw input data (stock price history)  
  - `Apple.csv` – Price data for Apple (2015–2025)  
  - `Amazon.csv` – Price data for Amazon  
  - `Microsoft.csv` – Price data for Microsoft  
  - `Google.csv` – Price data for Google  
  - `Meta.csv` – Price data for Meta  
  - `Netflix.csv` – Price data for Netflix  
  - `Tesla.csv` – Price data for Tesla  
  - `Costco.csv` – Price data for Costco  
  - `Starbucks.csv` – Price data for Starbucks  
  - `Amgen.csv` – Price data for Amgen  


- `results/` – Simulation outputs and visualizations  
  - `Cumulative Returns.png` – Comparison of cumulative returns across strategies  
  - `Portfolio Comparison.png` – Strategy-level performance visualization  
  - `Grid Search.png` – Parameter tuning visualization for SL/TP thresholds  
  - `Final.png` – Sharpe-weighted blended portfolio result  
---

---

## 📊 Sample Results

### ✅ Cumulative Returns (₹1 base)
| Ticker | Buy & Hold | Momentum | SL/TP Final |
|--------|-----------|----------|-------------|
| AAPL   | 8.02      | 65.33    | 12.74       |
| TSLA   | 30.95     | 1523.65  | 54.66       |
| NFLX   | 14.79     | 418.21   | 17.22       |

### ✅ Portfolio Sharpe Ratio
| Strategy      | Sharpe | Max Drawdown |
|--------------|--------|-------------|
| Buy & Hold   | 1.14   | -0.38       |
| Momentum     | 3.91   | -0.09       |
| SL/TP Final  | 2.51   | -0.09       |

---

## ▶ How to Run
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/Algorithmic-Trading-Strategy.git
   cd Algorithmic-Trading-Strategy
   
2. Install dependencies:
 ```bash
pip install -r requirements.txt
  ```
3. Open the notebook:
```bash
jupyter notebook notebooks/Task3_Adv_Analytics.ipynb
```
---

## 🤝 Connect
For questions, collaborations, or opportunities related to AI in finance and risk modeling, feel free to connect through dhakshashganesan@gmail.com or GitHub.




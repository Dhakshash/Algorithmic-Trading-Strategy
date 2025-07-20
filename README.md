# 📈 Algorithmic Trading Strategy Development & Portfolio Optimization

This project implements **momentum-based trading strategies** enhanced with **Stop-Loss (SL)** and **Take-Profit (TP)** refinements. Using 10 NASDAQ stocks (2015–2025), it compares multiple strategies, performs post-COVID recovery analysis, and optimizes portfolio allocation using Sharpe ratio blending.

---
## 🔄 Workflow

This project implements a complete pipeline for designing, evaluating, and optimizing momentum-based algorithmic trading strategies across ten diversified NASDAQ stocks over a ten-year period (2015–2025). The workflow integrates advanced signal generation, robust risk management, and portfolio optimization to achieve strong risk-adjusted returns.


### **1. Data Preparation**
Historical daily price data for ten NASDAQ stocks (AAPL, MSFT, GOOGL, AMZN, NFLX, META, TSLA, SBUX, AMGN, COST) was collected and cleaned to ensure consistency across the 2015–2025 period. Missing values were handled, dates were standardized, and datasets were aligned for uniform time-series analysis. Feature engineering included:
- **Lagged returns (1–5 days)** for short-term momentum.
- **Exponential Moving Averages (EMA-12, EMA-26)** for trend smoothing.
- **MACD (Moving Average Convergence Divergence)** to detect momentum shifts.
- **RSI (Relative Strength Index)** for overbought/oversold conditions.

These indicators form the foundation for momentum signal generation, enabling strategies to adapt to varying market trends.


### **2. Strategy Design**
A **Hybrid Momentum Strategy** was designed by combining multiple technical indicators to reduce overfitting and improve adaptability. Signals were generated based on three conditions:
1. **30-day return** exceeds a predefined threshold.
2. **Moving Average Crossover**: MA20 > MA50.
3. **RSI > 55** indicating bullish momentum.
A buy signal was triggered if any two conditions were satisfied, creating a rule-based yet flexible trading framework. This approach ensures robustness across bull, bear, and sideways markets.


### **3. Stop-Loss & Take-Profit Mechanisms**
To manage downside risk and lock in gains, advanced SL/TP rules were integrated:
- **Momentum Only**: Trades executed purely on signal entry/exit.
- **SL/TP + Fixed Hold**: Combines stop-loss and take-profit thresholds with a fixed holding period.
- **SL/TP Final (Dynamic Exit)**: Exits immediately upon hitting SL or TP, removing the rigidity of time-based exits.
Dynamic SL/TP significantly reduces large drawdowns in volatile markets, offering superior risk control compared to static holding strategies.


### **4. Performance Evaluation**
Each strategy was evaluated using metrics that capture both profitability and stability:
- **Cumulative Returns** for growth comparison.
- **Sharpe Ratio** to assess risk-adjusted performance.
- **Maximum Drawdown (MaxDD)** for downside risk analysis.
These measures prevent overemphasis on raw returns and ensure strategies provide consistent, risk-adjusted gains suitable for portfolio allocation.


### **5. COVID Recovery Analysis**
To stress-test resilience, strategies were analyzed during the COVID-19 market shock (Feb 2020 crash). Recovery timelines were computed by measuring the days required for each stock to regain pre-crash price levels. Results highlighted stocks like AMZN and NFLX recovering within three weeks, while others like GOOGL and SBUX took several months. This analysis validates strategy performance under real-world crisis conditions.


### **6. Portfolio Optimization**
Equal-weighted portfolios were constructed for each strategy, followed by **Sharpe-weighted blending** of Momentum and SL/TP Final to balance high returns with low volatility. A grid search approach optimized the weight distribution, ensuring maximum Sharpe ratio while maintaining minimal drawdown (-0.09). This blending approach enhances portfolio resilience and is aligned with modern risk management principles.


### **7. Visualization**
Comprehensive visual analysis was implemented to illustrate:
- **Cumulative returns across strategies and stocks**.
- **Sharpe ratio vs. drawdown comparison tables**.
- **Grid search heatmaps for SL/TP optimization**.
- **COVID recovery timelines**.
These visualizations provide intuitive insights for decision-making and make strategy comparisons transparent.


**Summary:**  
The workflow integrates robust signal generation, advanced risk management through dynamic SL/TP, and portfolio optimization using Sharpe-based blending. This ensures the strategies deliver superior risk-adjusted returns while remaining resilient under extreme market conditions.

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




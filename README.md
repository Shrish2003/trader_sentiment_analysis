# Trader Performance vs Market Sentiment  
**Data Science / Analytics Intern – Round 0 Assignment (Primetrade.ai)**

---

## 📌 Objective
The objective of this project is to analyze how **market sentiment (Fear, Greed, Neutral)** relates to **trader behavior and performance** on the Hyperliquid trading platform.  
The goal is to uncover **patterns and insights** that can inform **smarter, risk-aware trading strategies**.

---

## 📂 Datasets Used
1. **Bitcoin Fear & Greed Index**
   - Columns include: date, classification (Fear, Extreme Fear, Neutral, Greed, Extreme Greed)
   - Used to represent overall market sentiment on a daily basis

2. **Hyperliquid Historical Trader Data**
   - Contains trader-level execution details such as:
     - Account
     - Trade size
     - Side (Buy/Sell)
     - Closed PnL
     - Timestamp
     - Leverage and position-related information

---

## 🧪 Methodology

### 1. Data Preparation
- Loaded both datasets using Pandas
- Converted timestamps into **daily granularity**
- Explicitly handled datetime format inconsistencies
- Normalized sentiment into three regimes:
  - **Fear** (Fear + Extreme Fear)
  - **Greed** (Greed + Extreme Greed)
  - **Neutral**
- Aligned trader execution data with daily market sentiment

### 2. Feature Engineering
Created key analytical metrics:
- **Daily PnL per trader**
- **Win rate** (percentage of profitable trades)
- **Trade frequency per day**
- **Behavioral changes across sentiment regimes**

### 3. Analysis
- Compared performance metrics across sentiment regimes
- Studied behavioral changes such as trading activity and win rates
- Visualized results using boxplots and bar charts

---

## 📊 Output Charts & Tables

All outputs are generated **inside the Jupyter Notebook (`analysis.ipynb`)**.

### Key Visualizations:
- **Daily Trader PnL by Market Sentiment (Boxplot)**
- **Average Trades per Day by Sentiment (Bar Chart)**
- **Average Win Rate by Sentiment (Bar Chart)**

These charts provide clear evidence of how trader performance and behavior differ under Fear, Greed, and Neutral market conditions.

---

## 🔍 Key Insights

1. **Fear regimes exhibit the highest PnL volatility**
   - Large dispersion in outcomes
   - Indicates increased downside risk and unstable performance

2. **Greed regimes show higher trading activity and upside potential**
   - Traders are more active
   - Presence of positive PnL outliers, but risk remains high

3. **Neutral regimes are the most stable**
   - Narrower PnL distribution
   - Fewer extreme outcomes
   - Acts as a baseline trading environment

4. **Trader behavior changes with sentiment**
   - Trade frequency increases during Greed
   - Fear periods show erratic participation and higher uncertainty

---

## 🎯 Strategy Recommendations

1. **Risk Management during Fear**
   - Reduce leverage and position size
   - Especially important for high-frequency or aggressive traders

2. **Controlled Aggression during Greed**
   - Allow increased trade frequency only for traders with historically high win rates
   - Prevent excessive risk-taking during euphoric market conditions

These strategies help balance **risk and reward** based on prevailing market sentiment.

---

## ⚙️ Setup Instructions

### 1. Clone the Repository
```bash
git clone https://github.com/yourusername/trader-sentiment-analysis.git
cd trader-sentiment-analysis
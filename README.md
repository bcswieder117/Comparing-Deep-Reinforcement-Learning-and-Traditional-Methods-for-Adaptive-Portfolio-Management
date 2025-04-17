# Comparing Deep Reinforcement Learning and Traditional Methods for Adaptive Portfolio Management

This project explores and compares the effectiveness of Deep Reinforcement Learning (DRL) agents and traditional Machine Learning (ML) models in stock trading strategy development. The analysis evaluates model performance across multiple market regimes using real-world data and metrics aligned with financial portfolio optimization.

---

##  Project Objective

To compare traditional ML methods like Gradient Boosting Machines (GBM) and Deep Neural Networks (DNN) with DRL agents (DQN, PPO, A2C) for adaptive trading. The goal is to assess:
- Predictive accuracy of ML models
- Strategy robustness and adaptability of DRL agents
- Performance consistency across dynamic regimes (bull, bear, volatile)

---

##  Key Results

### Traditional ML Models

| Model | MSE     | R²      |
|-------|---------|---------|
| GBM   | 5.60    | 0.998   |
| DNN   | 485.60  | 0.819   |

GBM achieved the highest prediction accuracy with the lowest mean squared error.

![Model Predictions vs Actual](DNN%20XGBoost%20Algorithm%20Comparision%20Result.png)

---

### DRL Agent Performance (Overall)

| Agent | Total Reward |
|-------|--------------|
| DQN   | 13.85        |
| PPO   | 65.85        |
| A2C   | 151.67       |

![Cumulative Rewards](Cumulative%20Rewards%20Over%20Time.png)

---

### DRL Agent Performance by Market Regime

#### Bull Market
A2C and PPO outperformed DQN significantly.

![Bull Market](Cumulative%20Rewards_Bull%20Market.png)

#### Bear Market
DQN preserved capital effectively; A2C struggled with volatility.

![Bear Market](Cumulative%20Rewards_Bear%20Market.png)

#### Volatile Market
A2C adapted best to changing conditions and maintained upward growth.

![Volatile Market](Cumulative%20Rewards_Volatile%20Market.png)

---

##  Methodology

- **ML models**: Trained using historical stock data (OHLCV) from 2018–2023.
- **DRL environment**: Custom OpenAI Gym-compatible environment simulating portfolio actions (buy/sell/hold).
- **Market segmentation**: Data separated into bullish, bearish, and sideways/volatile markets using 30-day moving averages and % thresholds.
- **Metrics**:
  - ML: Mean Squared Error (MSE), R²
  - DRL: Total reward, Sharpe Ratio, Sortino Ratio, Maximum Drawdown

---

##  Repository Contents

- `CSC 6230 Code.zip` - Full implementation of traditional models and DRL agents
- `*.png` - Visualizations of performance and predictions
- `Project Proposal_Swieder.pdf` - Initial proposal outlining the goals and structure
- `Problem Statement_Swieder.pdf` - Research problem and planned methods

---

##  Future Work

- Incorporate transaction costs and slippage into the DRL environment.
- Evaluate models with higher-frequency (minute/hourly) trading data.
- Extend to multi-asset portfolio optimization and risk-sensitive reward shaping.

---

##  License and Authorship

This project was created and executed solely by Blaine Swieder for CSC 6230: Machine Learning. No external codebases or datasets were used beyond freely accessible public historical market data.



##  License

This work is released for academic/research use only. No financial advice is provided.

---


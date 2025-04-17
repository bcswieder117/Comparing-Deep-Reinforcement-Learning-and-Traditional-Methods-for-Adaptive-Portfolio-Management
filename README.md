#  Comparing Deep Reinforcement Learning and Traditional Methods for Adaptive Portfolio Management

This repository contains the full implementation of a graduate-level research project conducted at Tennessee Technological University. The objective is to evaluate and compare traditional machine learning models and deep reinforcement learning (DRL) agents for adaptive stock trading under varying market regimes.

##  Overview

The study benchmarks:

- **Traditional Models**:
  - Gradient Boosting Machines (GBM)
  - Deep Neural Networks (DNN)

- **Deep Reinforcement Learning Agents**:
  - Deep Q-Network (DQN)
  - Proximal Policy Optimization (PPO)
  - Advantage Actor-Critic (A2C)

Models are tested across real-world stock data (2018–2023) and market conditions (bullish, bearish, sideways) using a custom OpenAI Gym trading environment.

##  Key Findings

- **GBM** had the best prediction accuracy (MSE ≈ 5.60, R² ≈ 0.998).
- **A2C** showed the most robust trading performance with highest cumulative rewards and best Sharpe/Sortino ratios.
- DRL agents outperformed traditional models in adaptability but were more sensitive to training conditions and randomness.

##  Repository Structure

- cleaned_stock_data.csv – Preprocessed stock data
- notebooks/
  - 01_traditional_models.ipynb – GBM and DNN evaluation
  - 02_drl_environment.ipynb – Custom Gym environment
  - 03_drl_agents.ipynb – DQN, PPO, A2C training
  - 04_market_regimes.ipynb – Market condition analysis
  - 05_results_summary.ipynb – Final graphs and comparisons

##  Technologies

- Python, NumPy, Pandas, scikit-learn, TensorFlow/Keras
- XGBoost
- OpenAI Gym, stable-baselines3
- Matplotlib, Seaborn

##  Future Work

- Incorporate transaction costs and slippage
- Experiment with high-frequency data
- Apply hybrid ensemble models for stability
- Implement dynamic position sizing and risk control

##  License

This work is released for academic/research use only. No financial advice is provided.

---


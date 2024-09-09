
# Stock Prices Prediction using Deep Reinforcement Learning

This project implements a **novel ensemble strategy** that combines five state-of-the-art deep reinforcement learning (DRL) algorithms: **Proximal Policy Optimization (PPO)**, **Advantage Actor Critic (A2C)**, **Deep Deterministic Policy Gradient (DDPG)**, **Twin Delayed Deep Deterministic Policy Gradient (TD3)**, and **Soft Actor-Critic (SAC)**. The goal is to predict stock prices and develop optimal trading strategies that maximize profit while managing risk.

## Overview

Stock price prediction is a challenging task due to the volatile nature of financial markets. This project leverages DRL algorithms to allow agents to learn trading strategies through trial and error by interacting with historical market data and optimizing their actions to maximize returns.

### Features:
- **Ensemble Strategy**: Integrates PPO, A2C, DDPG, TD3, and SAC into an ensemble of agents, combining their strengths for enhanced prediction and decision-making.
- **Continuous Action Space**: DDPG, TD3, and SAC handle continuous action spaces, while PPO and A2C manage discrete decisions.
- **Policy Optimization**: Focus on improving trading policies using policy gradient techniques.
- **Real-Time Trading Simulation**: Simulates trading on historical stock market data, learning optimal strategies to maximize profit.
- **Risk Management**: Agents learn to balance profitability with risk management.

## Deep Reinforcement Learning Algorithms

1. **Proximal Policy Optimization (PPO)**:
   - A policy gradient method that simplifies optimization while maintaining a balance between exploration and exploitation.
   - Ensures more stable convergence through clipped objective functions.

2. **Advantage Actor Critic (A2C)**:
   - An on-policy algorithm that computes the advantage function to reduce the variance in policy gradient estimation.
   - Uses a synchronous version of A3C, making it faster and more efficient for training in parallel.

3. **Deep Deterministic Policy Gradient (DDPG)**:
   - Handles continuous action spaces, making it suitable for real-world trading where actions (e.g., buying/selling stock quantities) are not discrete.
   - Uses an actor-critic framework, leveraging experience replay and target networks.

4. **Twin Delayed Deep Deterministic Policy Gradient (TD3)**:
   - A variant of DDPG designed to address its overestimation bias.
   - Uses twin Q-networks to provide more accurate value estimates and applies delayed policy updates to ensure stable training.

5. **Soft Actor-Critic (SAC)**:
   - An off-policy algorithm that maximizes entropy along with rewards to encourage exploration and prevent premature convergence.
   - Provides superior performance in environments requiring continuous action spaces by balancing exploration and exploitation.

## Installation

To set up the project locally, follow these steps:

```bash
# Clone the repository
git clone https://github.com/Abhicoder03/Stock-Prices-Prediction-using-Deep-Reinforcement-Learning.git

# Navigate to the project directory
cd Stock-Prices-Prediction-using-Deep-Reinforcement-Learning
```

## Usage

After installing the necessary dependencies, you can run the training script as follows:

```bash
python train.py --algorithm <ppo|a2c|ddpg|td3|sac> --stock_data <path_to_stock_data> --epochs <num_epochs>
```

### Arguments:
- `--algorithm`: Specify the DRL algorithm to use: `ppo`, `a2c`, `ddpg`, `td3`, or `sac`.
- `--stock_data`: Path to the historical stock data file.
- `--epochs`: Number of epochs for training the model.

## Datasets

You can use historical stock market data from various sources, such as:
- **Yahoo Finance**: Provides open-source stock market data.
- **Quandl**: Another data source for stock prices, indices, and commodities.

Make sure to format the data correctly (e.g., date, open, high, low, close, volume).

## Results

![image](https://github.com/user-attachments/assets/4f0e4f04-494d-4c6a-850b-dd0dcf59cc92)

**Figure: Stock Data Analysis comparing A2C (Advantage Actor-Critic), Mean Variance Strategy, and Stock Close Prices from July 2021 to January 2024. The A2C strategy shows significant growth towards the end, outperforming both the Mean Variance strategy and the actual stock closing prices.**


This graph represents **Stock Data Analysis** over a specific period from **July 2021 to January 2024**, comparing the performance of different strategies:

1. **A2C (Advantage Actor-Critic)**: 
   - Shown by the **blue line**, this curve represents the performance of the stock prediction model based on the A2C algorithm.
   - The A2C model generally tracks the stock price movements, but it starts diverging positively from the green line (Close Price) over time, showing a higher return, especially towards the latter part of the time period. Around **January 2024**, it shows a strong upward trend, indicating that the model's strategy has successfully increased in value.

2. **Mean Var**:
   - Represented by the **orange line**, this is likely a reference to a mean-variance optimization method or a baseline comparison strategy.
   - The performance is moderate and consistent, remaining relatively stable over time without much volatility. The growth rate is slower than A2C, but it remains above the actual stock close price for most of the period, indicating that this strategy maintains value better than the actual stock closing prices.

3. **Close**:
   - The **green line** represents the actual stock closing prices over time.
   - It fluctuates moderately throughout the timeframe, showing some dips and rises but relatively stable overall. It acts as the baseline for comparing the performance of both A2C and Mean Var strategies.


### Conclusion:
This chart demonstrates that the **A2C-based strategy** has been effective in generating higher returns compared to both the stock's actual close prices and the **Mean Var strategy**. The sharp rise in A2C's value at the end of the period indicates that the reinforcement learning-based model can potentially capitalize on market opportunities better than traditional strategies like Mean Var.

Similarly grapgh of other algorithms.

![image](https://github.com/user-attachments/assets/9db8a6c0-2614-4f9a-8996-a31573ad2f71)

**Figure: Stock Data Analysis comparing DDPG, Mean Variance Strategy, and Stock Close Prices from July 2021 to January 2024. The DDPG strategy shows significant growth towards the end, outperforming both the Mean Variance strategy and the actual stock closing prices.**

![image](https://github.com/user-attachments/assets/0197394b-f201-44ad-8810-71fbb5d07c1e)

**Figure: Stock Data Analysis comparing PPO, Mean Variance Strategy, and Stock Close Prices from July 2021 to January 2024. The PPO strategy shows significant growth towards the end, outperforming both the Mean Variance strategy and the actual stock closing prices.**

![image](https://github.com/user-attachments/assets/f268563d-605c-46a8-b02e-d7dc47686a0d)

**Figure: Stock Data Analysis comparing TD3, Mean Variance Strategy, and Stock Close Prices from July 2021 to January 2024. The TD3 strategy shows significant growth towards the end, outperforming both the Mean Variance strategy and the actual stock closing prices.**

![image](https://github.com/user-attachments/assets/1b876a2a-f894-4b50-8446-7eea1c9c57e7)

**Figure: Stock Data Analysis comparing SAC, Mean Variance Strategy, and Stock Close Prices from July 2021 to January 2024. The SAC strategy shows significant growth towards the end, outperforming both the Mean Variance strategy and the actual stock closing prices.**


## Contributing

If you want to contribute to this project, feel free to fork the repository, make changes, and create a pull request. All contributions are welcome!

---

## Made with :heart:

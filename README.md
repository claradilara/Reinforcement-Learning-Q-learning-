
# Reinforcement Learning: Taxi-v3 with Q-Learning

## Problem Description
This project solves the **Taxi-v3** environment using **Q-learning**, a classic
model-free reinforcement learning algorithm.

The agent must:
- Pick up a passenger at one location
- Navigate a grid world
- Drop the passenger off at the correct destination
while minimizing penalties and maximizing cumulative reward.

The environment is stochastic and penalizes illegal actions, making it a standard
benchmark for reinforcement learning algorithms.

---

## Environment
- Environment: OpenAI Gym `Taxi-v3`
- State space: 500 discrete states
- Action space: 6 discrete actions  
  (south, north, east, west, pickup, dropoff)

---

## Methodology

### Algorithm
- Q-learning (off-policy temporal-difference control)
- Tabular Q-value representation

### Training Strategy
- ε-greedy exploration
- Learning rate (α)
- Discount factor (γ)
- Episode-based training

Q-value update rule:
Q(s,a) ← Q(s,a) + α [ r + γ max Q(s′,a′) − Q(s,a) ]

---

## Evaluation
The agent is evaluated using:
- Average reward per episode
- Number of penalties
- Successful episode completion

Training metrics are monitored to verify learning convergence.

---

## Results
- The agent learns an effective navigation policy
- Illegal actions and penalties decrease significantly
- Average reward improves and stabilizes over time

This demonstrates successful learning in a discrete state–action environment.

---

## Project Structure
📦 taxi-q-learning/  
 ┣ notebooks/  
 ┃ ┗ Taxi_q_learning_notebook.ipynb  
 ┣ outputs/  
 ┃ ┗ training_metrics.png  
 ┣ requirements.txt  
 ┗ README.md  

---

## Tech Stack
- Python
- NumPy
- OpenAI Gym
- Matplotlib

---

## How to Run
1. Install dependencies:
pip install -r requirements.txt

2. Run the notebook:
jupyter notebook Taxi_q_learning_notebook.ipynb

---

## Key Takeaways
- Demonstrates understanding of reinforcement learning fundamentals
- Implements Q-learning from scratch
- Highlights exploration–exploitation trade-off
- Serves as a baseline for advanced RL methods (SARSA, DQN)

---

## Future Improvements
- Compare Q-learning with SARSA
- Implement Deep Q-Network (DQN)
- Hyperparameter optimization
- Reward shaping experiments

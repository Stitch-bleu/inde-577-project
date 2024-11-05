# Reinforcement Learning: FrozenLake Q-Learning

## Introduction

Reinforcement Learning (RL) is a type of machine learning where an agent learns to make decisions by interacting with an environment. Through trial and error, the agent receives rewards for beneficial actions and penalties for undesirable ones. The objective is to learn an optimal strategy, or policy, to maximize rewards over time.

In this example, we tackle the FrozenLake problem using a **Q-learning algorithm**. The FrozenLake environment consists of a 4x4 grid where the agent starts at one location and must reach a goal. The environment includes frozen tiles (safe) and holes (unsafe), and each move has a probability of slipping, adding complexity to the path-finding problem. The agent's goal is to find the safest and most efficient path to reach the goal while avoiding the holes.

## Theory and Methodology

### Reinforcement Learning and Markov Decision Processes (MDPs)

At the core of Reinforcement Learning is the **Markov Decision Process (MDP)** framework, which provides a mathematical model for decision-making. An MDP is defined by:

- **States (S)**: All possible situations the agent can encounter (e.g., each tile in FrozenLake).
- **Actions (A)**: All possible moves the agent can make from each state (e.g., left, right, up, down).
- **Transition probabilities (T)**: The likelihood of moving from one state to another given an action.
- **Rewards (R)**: Immediate feedback received after an action.
- **Discount factor (γ)**: Determines the importance of future rewards versus immediate rewards.

### Q-learning

**Q-learning** is a model-free Reinforcement Learning algorithm, meaning it doesn't require prior knowledge of the environment's transition probabilities. Instead, Q-learning approximates the optimal action-value function (Q) that defines the expected reward of taking an action in a given state and then following the optimal policy.

The Q-learning algorithm updates Q-values according to:

\[
Q(s, a) \leftarrow Q(s, a) + \alpha \times (R + \gamma \times \max Q(s', a') - Q(s, a))
\]

Where:
- \( Q(s, a) \): The current Q-value of state-action pair (s, a).
- \( \alpha \): The learning rate, controlling how much the Q-values are updated.
- \( \gamma \): The discount factor, determining the importance of future rewards.
- \( R \): The reward received after taking action \( a \) from state \( s \).
- \( s' \): The next state after taking action \( a \) from state \( s \).

### Exploration vs. Exploitation

The Q-learning algorithm uses an **ε-greedy policy** to balance exploration and exploitation:
- **Exploration**: With probability \( ε \), the agent chooses a random action to explore.
- **Exploitation**: With probability \( 1 - ε \), the agent chooses the action with the highest Q-value.

Over time, ε is decayed to encourage the agent to focus more on exploitation as it gains more knowledge about the environment.

## Hyperparameters

The following parameters are crucial for Q-learning in this environment:
- **num_episodes**: Number of training episodes to run.
- **max_steps_per_episode**: Maximum steps allowed per episode.
- **learning_rate** (α): Controls how quickly the algorithm updates the Q-values.
- **discount_rate** (γ): Determines the importance of future rewards.
- **epsilon**: Initial exploration rate.
- **max_epsilon**: Maximum exploration probability.
- **min_epsilon**: Minimum exploration probability.
- **epsilon_decay_rate**: Rate at which ε decreases after each episode.

## Implementation

1. **Setup**: 
   - Install and import necessary libraries (`gym` for environment setup and `numpy` for Q-table manipulation).
   - Initialize the FrozenLake environment and the Q-table.

2. **Q-Learning Training Loop**:
   - For each episode, initialize the environment and set the state.
   - Run a loop where the agent takes actions, observes rewards, and updates Q-values.
   - Adjust ε to reduce exploration over time.

3. **Visualization**:
   - Use `seaborn` and `matplotlib` to visualize the learned Q-values in a heatmap.

```python
import matplotlib.pyplot as plt
import seaborn as sns

plt.figure(figsize=(10, 6))
sns.heatmap(q_table, annot=True, fmt=".2f", cmap="coolwarm", cbar=True)
plt.title("Q-Values for Actions in Each State (FrozenLake)")
plt.xlabel("Actions")
plt.ylabel("States")
plt.show()

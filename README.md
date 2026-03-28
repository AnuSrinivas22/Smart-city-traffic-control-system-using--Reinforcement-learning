# Smart-city-traffic-control-system-using--Reinforcement-learning


# 🚦 Smart Traffic Control System using Reinforcement Learning

This project implements an AI-based smart traffic signal control system using Reinforcement Learning (RL). The system dynamically adjusts traffic signals to minimize congestion and waiting time at intersections.

---

## 📌 Project Overview

Traditional traffic lights operate on fixed timers, which are inefficient under dynamic traffic conditions. This project uses a Reinforcement Learning agent to learn optimal traffic light control strategies.

The agent interacts with a simulated environment and learns to reduce traffic congestion over time.

---

## 🧠 Key Concepts

- Reinforcement Learning (RL)
- Custom OpenAI Gym Environment
- Proximal Policy Optimization (PPO)
- Reward Optimization
- Simulation using Pygame

---

## ⚙️ Technologies Used

- Python
- Gymnasium (OpenAI Gym)
- Stable-Baselines3
- NumPy
- Pygame
- Matplotlib

---

## 🏙️ Environment Description

The traffic system is modeled as a 4-way intersection:

- Each direction has a queue of vehicles
- State: Number of vehicles in each lane → `[N, S, E, W]`
- Action Space:
  - `0` → Green for North-South
  - `1` → Green for East-West

---

## 🎯 Reward Function

The reward is designed to:

- Minimize total waiting time
- Maintain balance between lanes

```python
reward = -(waiting_penalty + 0.5 * balance_penalty)

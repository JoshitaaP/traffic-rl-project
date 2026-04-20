# Traffic Signal Control using Reinforcement Learning (DQN)

## Overview

This project implements an adaptive traffic signal control system using Deep Reinforcement Learning (DQN) and the SUMO traffic simulator.

The system dynamically adjusts traffic light phases based on real-time traffic conditions to reduce congestion, waiting time, and improve overall traffic flow.

---

## Problem Statement

Traditional traffic signals use fixed timing, which leads to:

* Unnecessary waiting at empty roads
* Traffic congestion at busy lanes
* Inefficient traffic flow

This project solves the problem by using an AI-based adaptive signal controller.

---

## Solution Approach

The system follows a Reinforcement Learning pipeline:

1. Extract traffic state (vehicle count per lane)
2. Use a DQN agent to choose signal action
3. Apply action in SUMO simulation
4. Receive reward based on traffic improvement
5. Update model using experience replay

---

## Tech Stack

* Python 
* SUMO (Simulation of Urban Mobility)
* TraCI API
* PyTorch 
* Matplotlib 

---

## Project Structure

```
traffic_rl_project/
│── notebooks/
│   └── traffic_rl.ipynb
│
│── sumo_files/
│   ├── simple.net.xml
│   ├── simple.rou.xml
│   └── simple.sumocfg
│
│── agent/
│── utils/
│── env/
│
│── README.md
│── .gitignore
```

---

## Key Features

*  Lane-wise traffic state representation
*  Deep Q-Network (DQN) implementation
*  Experience Replay Buffer
*  Target Network for stable learning
*  Epsilon-Greedy exploration
*  Improved reward function (traffic reduction based)
*  Training performance visualization

---

## Results

* Traffic congestion reduced over time
* Reward improved from negative values to near zero
* System successfully learned to clear traffic dynamically

---

## Sample Output

* Initial phase: High congestion
* Mid training: Gradual improvement
* Final phase: Minimal / zero traffic

---

##  How to Run

### 1. Install Dependencies

```bash
pip install torch matplotlib traci sumolib
```

### 2. Set SUMO_HOME

```bash
set SUMO_HOME=C:\Program Files (x86)\Eclipse\Sumo
```

### 3. Run the Project

```bash
python your_script.py
```

---

## Future Improvements

* Multi-intersection traffic control
* Continuous traffic generation
* Advanced RL (Double DQN, PPO)
* Real-world dataset integration

---

##  Conclusion

This project demonstrates how AI can optimize real-world systems like traffic control, making cities smarter and more efficient.

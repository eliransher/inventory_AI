# 🧠 Neural Network Approximations for Inventory Models

This repository implements and evaluates **three neural network architectures (NN1, NN2, NN3)** designed to approximate analytical and simulation-based results of a **stochastic inventory system** operating under an $(s,S)$ policy.  
Each network captures a different mapping between inventory system parameters and steady-state performance metrics.

---

## 📘 Project Overview

Traditional inventory models often rely on analytical approximations or simulation-based evaluations, which can be computationally expensive for general inter-arrival and lead-time distributions.  
This project explores the use of **deep learning** to approximate system performance efficiently and accurately.

The three networks serve distinct purposes:

| Model | Objective | Description |
|--------|------------|-------------|
| **NN1** | Estimate the steady-state probability vector $\mathbf{P}$ | Predicts the stationary inventory-level distribution based on input moments and policy parameters. |
| **NN2** | Predict cycle time and demand fulfillment probability | Learns the mapping from system features to expected cycle time $\mathbb{E}[C]$ and fulfillment probability $q$. |
| **NN3** | Approximate total expected cost $g(s, S)$ | Combines learned relationships from NN1 and NN2 to predict long-run average cost per time unit. |

---

## 🧩 The Inventory Model

The system assumes:
- Single-item, continuous-review $(s,S)$ inventory policy.  
- Random **inter-demand** times $D$ and **lead times** $L$ (not necessarily exponential).  
- No backorders; unmet demand results in lost sales.  

## Running the package
The file main under code contains all the trained NNs with examples and illustrations.



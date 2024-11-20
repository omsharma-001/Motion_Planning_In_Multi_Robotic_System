# Distributed Multi-Robot Motion Planning Using A* and Deep Reinforcement Learning (DRL)

## Overview

Collision-free motion planning in distributed multi-robot systems is a challenging problem, particularly in dynamic environments where multiple robots operate simultaneously. This research integrates traditional graph search algorithms like **A\*** with **Deep Reinforcement Learning (DRL)** to enable real-time, adaptive, and efficient robot coordination.

The proposed framework ensures:
- **Collision-free navigation**.
- **Minimized execution time and energy usage**.
- **Dynamic adaptability to real-time environmental changes**.

---

## Features

- **2D Grid Environment**: Robots navigate from source to destination on a two-dimensional grid.
- **A\***: Provides deterministic and fast pathfinding for smaller grids.
- **DRL**: Enables adaptive learning and decision-making for dynamic environments.
- **Comparative Analysis**: Highlights the strengths and weaknesses of both approaches.

---

## Results
### Tabulated Results

| Grid Size | A\* Execution Time (s) | A\* Avg. Cost | DRL Execution Time (s) | DRL Avg. Cost |
|-----------|-------------------------|---------------|-------------------------|----------------|
| 4x4       | 0.0059                  | 6             | 1.076                  | 6              |
| 8x8       | 0.1036                  | 14            | 2.002                  | 14             |
| 16x16     | 0.4807                  | 30            | 7.581                  | 30             |
| 32x32     | 3.0483                  | 62            | 11.284                 | 62             |
| 64x64     | 15.4763                 | 126           | 34.424                 | 126            |
| 128x128   | 84.7217                 | 254           | 73.499                 | 254            |
| 256x256   | 607.4264                | 510           | 1612.103               | 510            |

---

## DRL Hyperparameters

To achieve optimal performance, the following DRL hyperparameters were used:

| Grid Size | Gamma | Alpha | Epsilon Decay | Max Steps |
|-----------|-------|-------|---------------|-----------|
| 4x4       | 0.95  | 0.1   | 0.1           | 2000      |
| 8x8       | 0.95  | 0.1   | 0.1           | 2000      |
| 16x16     | 0.95  | 0.1   | 0.1           | 5000      |
| 32x32     | 0.9   | 0.2   | 0.995         | 5000      |
| 64x64     | 0.9   | 0.2   | 0.995         | 10000     |
| 128x128   | 0.9   | 0.2   | 0.995         | 20000     |
| 256x256   | 0.9   | 0.2   | 0.995         | 5000      |

---

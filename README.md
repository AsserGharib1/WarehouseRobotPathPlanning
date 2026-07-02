# Multi-Robot Warehouse Navigation — Classical Planning & Deep RL

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/AsserGharib1/WarehouseRobotPathPlanning/blob/main/warehouse_path_planning.ipynb)
[![View on nbviewer](https://img.shields.io/badge/view%20full%20notebook-nbviewer-F37626?logo=jupyter&logoColor=white)](https://nbviewer.org/github/AsserGharib1/WarehouseRobotPathPlanning/blob/main/warehouse_path_planning.ipynb)


Path planning for warehouse order-fulfillment robots on an occupancy-grid map: classical **A\*** and **Dijkstra** planners with dynamic-obstacle replanning, benchmarked against a **Deep Q-Network** multi-robot controller.

## Highlights

- **Occupancy-grid mapping**: environment explored and rasterized to a 0/1 grid (`explored_ogm.npy`, `manual_ogm.npy`), visualized with pygame.
- **A\* vs Dijkstra benchmark** across 20 test cases, including dynamic obstacles that force online replanning.
- **Five-robot DQN controller** trained with experience replay, target networks, and reward shaping; hyperparameters tuned with **PSO** — reducing collisions versus the classical baseline.
- Full experiment figures in `figures/` and a detailed write-up in `docs/report.pdf`.

## Grid maps

Manually defined warehouse map and explored occupancy-grid map used by the planners:

![Manual grid map](figures/manual_grid_map.png)

![Explored grid map](figures/explored_grid_map.png)

## Repository contents

- `warehouse_path_planning.ipynb` — mapping, planners, simulation, and experiments (outputs preserved).
- `explored_map.png`, `*.npy` — grid maps used by the notebook.
- `docs/report.pdf` — project report.

## Running

```bash
pip install -r requirements.txt
jupyter notebook warehouse_path_planning.ipynb
```

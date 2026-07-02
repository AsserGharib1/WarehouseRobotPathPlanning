# Multi-Robot Warehouse Navigation — Classical Planning & Deep RL

Path planning for warehouse order-fulfillment robots on an occupancy-grid map: classical **A\*** and **Dijkstra** planners with dynamic-obstacle replanning, benchmarked against a **Deep Q-Network** multi-robot controller.

## Highlights

- **Occupancy-grid mapping**: environment explored and rasterized to a 0/1 grid (`explored_ogm.npy`, `manual_ogm.npy`), visualized with pygame.
- **A\* vs Dijkstra benchmark** across 20 test cases, including dynamic obstacles that force online replanning.
- **Five-robot DQN controller** trained with experience replay, target networks, and reward shaping; hyperparameters tuned with **PSO** — reducing collisions versus the classical baseline.
- Full experiment figures in `figures/` and a detailed write-up in `docs/report.pdf`.

## Repository contents

- `warehouse_path_planning.ipynb` — mapping, planners, simulation, and experiments (outputs preserved).
- `explored_map.png`, `*.npy` — grid maps used by the notebook.
- `figures/` — benchmark and training figures.
- `docs/report.pdf` — project report.

## Running

```bash
pip install -r requirements.txt
jupyter notebook warehouse_path_planning.ipynb
```

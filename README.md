# Autonomous-Path-Planning-Simulator
Interactive 2D path planning simulator implementing the A* (A-Star) algorithm. Designed to validate global navigation logic for autonomous mobile robots, featuring dynamic obstacle interaction, heuristic optimization analysis, and real-time search visualization.
Autonomous Path Planning Simulator (自主路径规划仿真)

**核心定位：** Path Planning, Algorithm Implementation, Motion Planning, Heuristic Search.

#### 1. Repository Description (GitHub 简介)
> **中文：** 基于 A* 算法的 2D 路径规划仿真器。用于验证移动机器人的全局导航逻辑，支持动态障碍物交互与启发式函数性能分析。
> **English:** Interactive 2D path planning simulator implementing the A* (A-Star) algorithm. Designed for validating global navigation logic for mobile robots, featuring dynamic obstacle interaction and heuristic function analysis.

#### 2. README.md 内容

```markdown
# 🧭 Autonomous Navigation Pathfinding Simulator

## 📖 Introduction
路径规划 (Path Planning) 是实现 **Embodied AI (具身智能)** 和全自主系统的核心环节。

本项目构建了一个可视化的算法验证沙盒，重点复现并分析了 **A* (A-Star)** 算法在栅格地图 (Grid Map) 中的表现。项目旨在模拟 UGV (无人地面车辆) 在复杂障碍物环境下的决策过程，验证算法在“搜索效率”与“路径最优性”之间的权衡。

## ✨ Key Features
* **Interactive Simulation Environment**: 支持用户自定义构建复杂的拓扑地图（设置起点、终点、绘制任意障碍墙）。
* **Heuristic Search Visualization**: 直观展示算法的搜索边界 (Open Set) 与已遍历区域 (Closed Set)，帮助分析不同启发式函数 (Manhattan vs Euclidean) 对搜索效率的影响。
* **Optimal Path Generation**: 保证在静态环境中规划出数学上的最短路径，并具备回溯机制。
* **Scalable Architecture**: 代码结构模块化，便于扩展至 Dijkstra, BFS, 或更高级的 D* Lite / RRT 算法。

## 🛠️ Tech Stack
* **Language**: Python 3.8+
* **Visualization**: Pygame / Matplotlib
* **Data Structures**: Priority Queues (Min-Heap) for $O(log N)$ retrieval efficiency.

## 🧠 Core Logic
The planner minimizes the total cost function $f(n) = g(n) + h(n)$:
* **$g(n)$**: The actual cost from the start node to the current node.
* **$h(n)$**: The heuristic estimated cost from the current node to the goal.

This project specifically focuses on optimizing the **Heuristic Function** to reduce computational overhead suitable for embedded systems with limited processing power.

## 🚀 Usage
```bash
git clone [https://github.com/your-username/pathfinding-simulator.git](https://github.com/your-username/pathfinding-simulator.git)
pip install pygame
python src/main.py

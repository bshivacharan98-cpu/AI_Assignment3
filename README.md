
# ASSIGNMENT 3
This project is a small exploration of how different search algorithms behave in navigation problems. Instead of treating everything as theory, each part focuses on a practical scenario — from road networks to grid-based movement and finally to environments that change over time.

---

## 1. Route Optimization on a City Network

The first problem looks at how to compute efficient routes between cities.

A dataset of Indian cities and distances is used to form a weighted graph. Based on a chosen starting point, the algorithm calculates the minimum travel cost to other cities.

### What it does:

* Builds a graph from external data (CSV file)
* Computes shortest paths using Dijkstra’s approach
* Supports flexible user queries (single destination or full map)
* Handles input variations gracefully

This section demonstrates how pathfinding algorithms can be applied beyond grids, especially in transportation-style problems.

---

## 2. Grid-Based Navigation with Obstacles

The second scenario shifts to a 2D environment where a ground vehicle must move from one point to another.

The environment is represented as a grid, where some cells are blocked. The difficulty of navigation is adjusted by changing how many obstacles are present.

To solve this, the A* algorithm is used, combining cost and heuristic estimates to guide the search.

### Key elements:

* Custom start and goal positions
* Random obstacle generation with varying densities
* Performance metrics such as:

  * Distance traveled
  * Nodes explored
  * Time taken

### Observation:

Denser environments significantly increase the effort required to find a valid route, sometimes even making it impossible.

---

## 3. Navigation in a Changing Environment

The final part introduces uncertainty.

Here, the vehicle does not operate in a fixed world — new obstacles may appear while it is already moving. This means a path that was once valid may suddenly become unusable.

To handle this:

* The system continuously monitors the path
* If blocked, it recalculates a new route from the current position

This reflects more realistic navigation scenarios where conditions are not static.

---

# Comparison of Algorithms for Minimum-Cost Flow

**Project for the Algorithms and Data Structures course**, analyzing and comparing the performance of two different algorithms for solving the **minimum-cost flow problem** on a graph.

---

## Project Objective

The goal of this project is to implement and analyze two classical algorithmic approaches for the minimum-cost flow problem: the **Cycle Canceling Algorithm** and the **Successive Shortest Path Algorithm (SSPA)**.

Using Python implementations and tests on randomly generated graphs, the project aims to compare the performance and computational complexity of the two methods, determining which is more efficient based on graph characteristics (size and density).

---

## Minimum-Cost Flow Problem

The minimum-cost flow problem is a fundamental graph optimization problem.  
Given a directed graph where each edge has a **maximum capacity** and a **cost** per unit of flow, the objective is to find a flow from a source node to a target node that **minimizes the total cost**, while respecting edge capacity constraints and flow conservation at each node.

This problem has numerous applications in logistics, telecommunications, and network design.

---

## Algorithms Analyzed

The following algorithms were implemented and compared:

- **Cycle Canceling Algorithm:** An iterative algorithm that starts from a feasible flow and repeatedly searches for **negative cycles** in the residual graph. A negative cycle represents a closed path where the flow can be increased while decreasing the total cost. The algorithm terminates when no more negative cycles exist, guaranteeing an optimal solution.  

- **Successive Shortest Path Algorithm (SSPA):** This algorithm iteratively finds the shortest paths (in terms of cost) from the source to the target in the residual graph. At each iteration, the flow is increased along the minimum-cost path found. The process continues until no more paths exist from the source to the target.  

---

## Methodology and Technologies

The comparative analysis followed these steps:

1. **Random Graph Generation:** A Python function was created to generate directed random graphs with a variable number of nodes and edges, assigning random capacities and costs to simulate different test conditions.  
2. **Algorithm Implementation:** Both the Cycle Canceling Algorithm and SSPA were implemented in Python.  
3. **Visualization and Analysis:** Graphs and resulting flows were visualized for qualitative analysis. Performance was evaluated in terms of theoretical computational complexity and practical observations.  

**Technologies used:**

- **Language:** Python  
- **Libraries:**  
  - **NumPy:** For efficient handling of numerical data structures.  
  - **NetworkX:** For creating, manipulating, and analyzing complex graphs.  
  - **Matplotlib:** For visualizing graphs and results.  

---

## Conclusions

From the comparison, it emerged that while both algorithms converge to the optimal solution, their efficiency strongly depends on the graph characteristics:

- **SSPA** tends to perform better on small to medium-sized graphs.  
- **Cycle Canceling Algorithm** can be advantageous on large graphs with low edge density.  

In conclusion, there is no universally superior algorithm; the choice depends on the specific problem structure.

---

## Contatti

* Alessio Bifulco: `alessio.bifulco@studio.unibo.it`

# Overview

This project extends the transportation optimization framework to a four-plant, four-destination network, solved using Linear Programming with the lpSolve and lpSolveAPI packages. The objective is to minimize total production and transportation costs while satisfying all destination demands and plant capacity constraints. A dummy destination absorbs any surplus production capacity.

The analysis includes both the primal and dual formulations:

- The primal model allocates shipments from each plant to each destination to achieve the minimum total cost.

- The dual model interprets shadow prices (marginal values) associated with each demand and supply constraint, connecting the mathematical model to economic equilibrium theory.

An economic interpretation is also provided, linking the dual formulation to the Marginal Revenue (MR) = Marginal Cost (MC) condition — the universal rule of profit maximization in economics. Visualization of MR and MC curves is performed using ggplot2.

# Findings

The optimal transportation cost (objective function value) is 55,320, representing the minimum total production and shipping expenditure.

Optimal shipment plan:

- Plant 1: 40 units → Destination 2; 60 units → Dummy

- Plant 2: 75 units → Destination 1

- Plant 3: 15 units → Destination 2; 70 units → Destination 3

- Plant 4: 5 units → Destination 1; 35 units → Destination 2

All supply and demand constraints are satisfied exactly, confirming model feasibility and efficiency.

# Dual interpretation:

- The shadow prices (pj – ci ≥ TCij) reflect per-unit marginal costs and revenues.

- Economic equilibrium occurs when MR = MC, meaning the system reaches optimal allocation with no incentive to increase or decrease production.

- The generated MR–MC graph illustrates equilibrium at a quantity of roughly 160 units, validating the theoretical equivalence between cost minimization and profit maximization.

- The analysis demonstrates how mathematical optimization can directly model economic decision-making and production efficiency.

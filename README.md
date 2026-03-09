# Traffic Flow Simulation using the Intelligent Driver Model

This repository contains the simulation code, animations, and final
report for the project:

**Modelling and Simulation of Traffic Flow**\
*MTH3024 -- Modelling and Simulation*\
Queen's University Belfast

The project models motorway traffic using the **Intelligent Driver Model
(IDM)**, a microscopic car‑following model where each vehicle adjusts
its acceleration based on the distance and velocity of the vehicle
ahead.

The aim of the project is to investigate how individual driver behaviour
leads to large‑scale traffic phenomena such as:

-   Free flow traffic
-   Congestion
-   Stop‑and‑go shockwaves
-   The effect of merging traffic from slip roads
-   The impact of speed limits on overall traffic flow

The repository also includes animations of the simulations used to
validate and visualise the model.

------------------------------------------------------------------------

# Repository Structure

Traffic-Flow-Model

│\
├── Traffic_Project_Code.ipynb\
│ Main Jupyter notebook containing the full simulation code\
│\
├── BasicTraffic.mp4\
│ Animation of the base IDM ring‑road simulation\
│\
├── TrafficSimulationWithSlipRoad.mp4\
│ Animation of the slip‑road extension simulation\
│\
├── Group5_Traffic_Model.pdf\
│ Final report for the project\
│\
└── README.md\
Repository documentation

------------------------------------------------------------------------

# Intelligent Driver Model (IDM)

The Intelligent Driver Model describes the acceleration of each vehicle
as a function of:

-   desired velocity
-   current velocity
-   distance to the vehicle ahead
-   relative velocity between vehicles

The IDM acceleration law is

dv/dt = a \[1 − (v/v_max)\^δ − (s\*/s)\^2\]

where the desired headway is

s\* = s_min + max(0, vT + (vΔv)/(2√(ab)))

This allows vehicles to:

-   accelerate towards a desired speed
-   maintain safe following distances
-   brake smoothly when approaching slower traffic

Using this model we can simulate realistic traffic behaviour.

------------------------------------------------------------------------

# Simulation 1 --- Ring Road Traffic

The first simulation models vehicles travelling on a **circular
motorway**.

Using a ring road avoids boundary effects and allows the system to reach
a steady traffic state.

From the simulation we construct the three **fundamental diagrams of
traffic flow**:

-   Flow vs Density
-   Velocity vs Density
-   Flow vs Velocity

These diagrams reveal the existence of a **critical density** at which
traffic flow is maximised before congestion begins.

### Ring Road Animation
[![Ring Road Animation](preview_basic.gif)](./BasicTraffic.mp4)

------------------------------------------------------------------------

# Simulation 2 --- Slip Road Extension

The model was extended by adding a **slip road where vehicles can merge
onto the motorway**.

Key features of this extension include:

-   Vehicles spawn on the slip road with probability P_in
-   Vehicles travel along the slip road using the same IDM rules
-   Vehicles may only merge if a safe gap exists on the motorway
-   Vehicles exit the motorway with probability P_out

This allows investigation of how merging traffic influences motorway
performance.

Simulations were repeated **30 times** for each parameter value to
compute mean values and standard deviations of traffic flow.

### Slip Road Animation
[![Slip Road Animation](preview_sliproad.gif)](./TrafficSimulationWithSlipRoad.mp4)
------------------------------------------------------------------------

# Running the Simulation

The simulation code is contained in:

Traffic_Project_Code.ipynb

Install dependencies:

pip install numpy matplotlib

Run the notebook and execute the cells sequentially to reproduce the
simulations and generate the animations.

------------------------------------------------------------------------

# Project Report

The full methodology, analysis, and results are available in:

Group5_Traffic_Model.pdf

The report contains:

-   Mathematical formulation of the IDM
-   Simulation methodology
-   Fundamental traffic diagrams
-   Slip road extension experiments
-   Speed limit analysis
-   Conclusions and limitations of the model

------------------------------------------------------------------------

# Authors

Ben Hamilton\
Luke Jackson\
Alex O'Connor\
Adam Higgins

School of Mathematics and Physics\
Queen's University Belfast

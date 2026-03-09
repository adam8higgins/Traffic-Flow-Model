# Traffic Flow Model -- Intelligent Driver Model Simulation

This repository contains the **code, animations, and final report** for
our\
**MTH3024 Modelling and Simulation** project at **Queen's University
Belfast**.

The project models motorway traffic using the **Intelligent Driver Model
(IDM)**, a microscopic car‑following model where each vehicle adjusts
its acceleration based on the distance and relative velocity to the car
ahead.

The goal of the project is to explore how **simple driver behaviour
rules lead to large‑scale traffic phenomena**, such as:

-   Free‑flow traffic
-   Traffic congestion
-   Shockwaves and stop‑and‑go behaviour
-   The impact of slip roads on motorway flow

------------------------------------------------------------------------

# Repository Contents

  -------------------------------------------------------------------------------------------
  File                                    Description
  --------------------------------------- ---------------------------------------------------
  **Traffic_Project_Code.ipynb**          Main Jupyter notebook containing the full
                                          simulation code

  **BasicTraffic.mp4**                    Animation of the base ring‑road traffic model

  **TrafficSimulationWithSlipRoad.mp4**   Animation of the slip‑road extension

  **Group5_Traffic_Model.pdf**            Final project report

  **README.md**                           Repository documentation
  -------------------------------------------------------------------------------------------

------------------------------------------------------------------------

# Model Overview

The simulation is based on the **Intelligent Driver Model (IDM)**, a
widely used microscopic traffic model that describes vehicle
acceleration as

a = a_max \[ 1 - (v/v_max)\^δ - (s\*/s)\^2 \]

where vehicle acceleration depends on:

-   desired speed
-   safe following distance
-   distance to the vehicle ahead
-   relative velocity to the vehicle ahead

This produces realistic traffic behaviour including: - smooth
acceleration - safe braking - spontaneous traffic jams -
density‑dependent flow behaviour

------------------------------------------------------------------------

# Simulation 1 --- Ring Road Traffic

The first model simulates vehicles travelling on a **circular
motorway**.

Using periodic boundary conditions avoids edge effects and allows
investigation of the **fundamental diagrams of traffic flow**:

-   Flow vs Density
-   Speed vs Density
-   Speed vs Flow

These diagrams allow us to analyse the transition from **free flow
traffic to congested traffic**.

### Animation

```{=html}
<video src="BasicTraffic.mp4" controls width="700">
```
```{=html}
</video>
```

------------------------------------------------------------------------

# Simulation 2 --- Slip Road Extension

The model was extended by introducing a **slip road where vehicles can
enter the motorway**.

Key features include:

-   Vehicles spawn randomly on the slip road with probability **P_in**
-   Vehicles travel along the slip road using the same IDM rules
-   Vehicles merge only when a **safe gap exists on the motorway**
-   Vehicles exit the motorway with probability **P_out**

This extension allows investigation of how **merging behaviour
influences traffic flow and congestion**.

### Animation

```{=html}
<video src="TrafficSimulationWithSlipRoad.mp4" controls width="700">
```
```{=html}
</video>
```

------------------------------------------------------------------------

# Running the Simulation

The simulation code is contained in:

    Traffic_Project_Code.ipynb

### 1. Install dependencies

    pip install numpy matplotlib

### 2. Open the notebook

Run the notebook in:

-   Jupyter Notebook
-   JupyterLab
-   VS Code

### 3. Run the cells in order

Running the notebook will:

-   simulate traffic dynamics using the IDM
-   generate traffic data
-   produce the traffic animations

------------------------------------------------------------------------

# Project Report

The full methodology, analysis, and results are available in:

    Group5_Traffic_Model.pdf

The report contains:

-   Mathematical description of the IDM
-   Simulation methodology
-   Fundamental traffic diagrams
-   Slip road extension analysis
-   Discussion of traffic flow behaviour

------------------------------------------------------------------------

# Authors

**Group 5 -- MTH3024 Modelling and Simulation**\
Queen's University Belfast

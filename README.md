# 🚗 Traffic Flow Simulation -- Intelligent Driver Model

Simulation of motorway traffic using the **Intelligent Driver Model
(IDM)** developed as part of

**MTH3024 -- Modelling and Simulation**\
School of Mathematics and Physics\
**Queen's University Belfast**

This project models how **individual driver behaviour produces
large-scale traffic patterns**, including congestion, optimal density,
and flow breakdown.

------------------------------------------------------------------------

# 🎥 Simulation Videos

## Basic Ring Road Model

Vehicles follow the Intelligent Driver Model on a **circular motorway**.

BasicTraffic.mp4

------------------------------------------------------------------------

## Slip Road Extension

Vehicles can **enter and exit the motorway** via a slip road,
introducing merging behaviour.

traffic_simulation.mp4

------------------------------------------------------------------------

# 📊 Project Overview

Traffic flow is simulated using the **Intelligent Driver Model**, a
microscopic car-following model describing how drivers accelerate and
brake in response to surrounding vehicles.

The model demonstrates how microscopic behaviour leads to macroscopic
traffic patterns such as:

-   Free-flow traffic\
-   Congestion\
-   Shockwave formation\
-   Optimal traffic density

The simulation reproduces the **fundamental traffic diagrams** used in
traffic engineering:

-   Flow vs Density\
-   Velocity vs Density\
-   Flow vs Velocity

These diagrams are used to validate the simulation against known traffic
theory.

------------------------------------------------------------------------

# 🧠 Intelligent Driver Model

The IDM determines vehicle acceleration using:

dv/dt = a \[ 1 − (v / vmax)\^δ − (s\* / s)\^2 \]

where

s\* = s_min + max(0, vT + (v Δv) / (2√ab))

Variables:

  Symbol   Meaning
  -------- ----------------------
  v        vehicle speed
  vmax     desired speed
  s        headway distance
  s\*      desired headway
  a        maximum acceleration
  b        comfortable braking
  T        safe time gap

This allows vehicles to:

-   accelerate when the road is clear\
-   slow when approaching traffic\
-   maintain safe following distances.

------------------------------------------------------------------------

# 🔵 Simulation 1 -- Basic Ring Road

The base model simulates vehicles travelling on a **circular road**.

Features:

-   periodic boundary conditions\
-   constant number of vehicles\
-   identical driver behaviour\
-   no inflow or outflow

This produces equilibrium traffic flow and allows construction of the
**fundamental traffic diagrams**.

------------------------------------------------------------------------

# 🟢 Simulation 2 -- Slip Road Extension

The model is extended by introducing a **slip road** where vehicles may:

-   enter the motorway with probability `Pin`
-   exit with probability `Pout`
-   merge only when a safe gap exists

If a safe gap does not exist, vehicles **queue on the slip road** until
merging becomes possible.

This allows the simulation of **real motorway merging behaviour**.

------------------------------------------------------------------------

# 📈 Key Results

### Critical Density

Traffic flow increases with density until a **critical density** is
reached.

Beyond this point:

-   congestion forms\
-   average velocity drops\
-   total traffic flow decreases.

------------------------------------------------------------------------

### Slip Road Effects

Increasing the **length of the slip road**

-   increases the probability that vehicles successfully merge\
-   increases the density of the motorway\
-   reduces total traffic flow once the system exceeds the critical
    density.

------------------------------------------------------------------------

### Speed Limit Effects

Increasing the speed limit increases flow **up to around 70--80 mph**.

Beyond this point, increases in speed provide **minimal improvements in
traffic flow** because braking waves become more severe.

------------------------------------------------------------------------

# ⚙️ Running the Simulation

Install dependencies:

pip install numpy matplotlib

Run the basic model:

python basic_ring_model.py

Run the slip road model:

python slip_road_model.py

The scripts generate animation videos:

BasicTraffic.mp4\
traffic_simulation.mp4

------------------------------------------------------------------------

# 📂 Repository Structure

Traffic-Flow-Model │ ├── BasicTraffic.mp4 ├── traffic_simulation.mp4 ├──
basic_ring_model.py ├── slip_road_model.py └── README.md

------------------------------------------------------------------------

# 📚 References

Treiber, M. & Kesting, A.\
Traffic Flow Dynamics: Data, Models and Simulation\
Springer, 2013

Hoogendoorn, S.\
Traffic Flow Theory and Simulation

Chandler, R. E., Herman, R., & Montroll, E. W.\
Traffic Dynamics: Studies in Car Following

------------------------------------------------------------------------

# 👨‍💻 Authors

Adam Higgins\
Ben Hamilton\
Luke Jackson\
Alex O'Connor

School of Mathematics and Physics\
Queen's University Belfast

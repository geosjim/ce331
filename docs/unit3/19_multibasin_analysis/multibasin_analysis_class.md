# In-Class - Multi-basin Analysis

We will work these examples together in class. Examples A-C follow the same steps as homework problem 4.14: rainfall excess, convolution with a unit hydrograph for each subbasin, then lag routing and summation at the outlet.

Excel starter file: [Multi-basin Analysis Example Template_v2.xlsx](Multi-basin%20Analysis%20Example%20Template_v2.xlsx)

# Textbook Example 2-7 - Hydrograph Convolution

Two subareas meet at confluence point A. Use the 10-yr 6-hr design rainfall for Houston. Infiltration losses are 0.15 in. for the first hour and 0.1 in./hr thereafter. Note: 1 ac-in/hr ≈ 1 cfs.

10-yr design storm volumes (Houston, Fig. 1-15):

| t (hr) | i (in./hr) | Rainfall (in.) |
|:---:|:---:|:---:|
| 1 | 3.1 | 3.1 |
| 2 | 2.0 | 4.0 |
| 3 | 1.5 | 4.5 |
| 6 | 0.9 | 5.4 |

Unit hydrograph ordinates (cfs):

| Time (hr) | UH₁ | UH₂ |
|:---:|:---:|:---:|
| 0 | 0 | 0 |
| 1 | 100 | 160 |
| 2 | 300 | 480 |
| 3 | 450 | 720 |
| 4 | 350 | 560 |
| 5 | 250 | 400 |
| 6 | 150 | 240 |
| 7 | 100 | 160 |
| 8 | 50 | 80 |
| 9 | 0 | 0 |

Data file: [Example_2-7_Data.xlsx](Example_2-7_Data.xlsx)

# Example A - Rainfall Excess for a Three-Subbasin Watershed

For a 30-min design storm with three 10-min pulses, compute the rainfall excess $i_e$ for each subbasin and each interval. Subbasins A and B have higher initial losses than C, so their excess depths differ.

$$i_e = (i - f)\,\Delta t \quad \text{(depth per 10-min step)}$$

where $i$ is rainfall intensity, $f$ is loss rate, and $\Delta t$ = 10 min = 1/6 hr.

| Time | Intensity (cm/hr) | Loss A & B (cm/hr) | Loss C (cm/hr) |
|:---:|:---:|:---:|:---:|
| 0-10 min | 6 | 2 | 1 |
| 10-20 min | 8 | 1.5 | 0 |
| 20-30 min | 5 | 1.5 | 0 |

Find: the excess depth (cm) for each pulse, tabulated for A & B and for C.

# Example B - Convolution for Each Subbasin

Demonstrate the discrete convolution for each subbasin. The unit hydrograph gives the watershed response to 1 cm of excess rainfall in 10 min; each pulse in the design storm produces a scaled, shifted copy of the UH. Sum across the pulses to get the storm hydrograph.

$$Q(t_n) = \sum_i P_i\,U_{n-i+1}$$

Given unit hydrographs (m³/s per cm, 10-min):

| Time (min) | UH A | UH B | UH C |
|:---:|:---:|:---:|:---:|
| 0 | 0 | 0 | 0 |
| 10 | 12 | 3 | 10 |
| 20 | 28 | 9 | 30 |
| 30 | 22 | 17 | 45 |
| 40 | 16 | 24 | 32 |
| 50 | 11 | 26 | 20 |
| 60 | 7 | 20 | 9 |
| 70 | 3 | 13 | 4 |
| 80 | 1 | 8 | 0 |
| 90 | 0 | 5 | |
| 100 | | 0 | |

Drainage areas: A = 6.0 km², B = 7.5 km², C = 9.0 km². Use the excess depths $P_1$, $P_2$, $P_3$ from Example A (A and B share the same excess depths).

Find: the storm hydrograph for sub-basins A, B, and C, and the sum A + B.

# Example C - Add, Lag, and Sum at the Outlet

Once each subbasin hydrograph is computed, we combine them at the watershed outlet. Subbasins A and B meet at confluence 1 upstream of C, so their summed hydrograph must be routed (here, a simple lag of K = 30 min = 3 time steps) to confluence 2 where it joins C.

Procedure:

1. Add $Q_A(t) + Q_B(t)$.
2. Lag the sum by K = 30 min (shift 3 time steps).
3. Add the lagged (A+B) hydrograph to $Q_C(t)$.
4. Plot $(A+B)_{lagged}$, $Q_C$, and the total at the outlet.

Find: the outlet hydrograph from 0 to 150 min, and the peak flow and time to peak at the outlet.

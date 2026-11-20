# In-Class - Unit Hydrographs

We will work these examples together in class. Each one is the same type of problem as a homework problem, with different numbers.

Excel starter file: [Unit Hydrographs Example Template.xlsx](Unit%20Hydrographs%20Example%20Template.xlsx)

Textbook Examples 2-2 (convolution) and 2-3 (lagging) data: [Example2-2.xlsx](Example2-2.xlsx)

# Example A - Convolution

A small watershed has a 1-hr unit hydrograph with ordinates U = [0, 100, 250, 200, 100, 0] cfs at t = 0, 1, …, 5 hr.

During a storm event, the net (excess) rainfall hyetograph in 1-hr pulses is Pn = [0.4, 1.0, 0.6] inches. Baseflow is negligible.

Using the convolution equation

$$Q_n = \sum_i P_i\,U_{n-i+1} = P_1 U_n + P_2 U_{n-1} + P_3 U_{n-2}$$

compute the storm hydrograph at the watershed outlet. Lay out $P_1 U$, $P_2 U$, $P_3 U$ each shifted by one hour and sum across each row.

Find: the storm hydrograph $Q_n$ (cfs) and the peak flow $Q_p$ and its time $t_p$. Check that the table starts and ends with a row of zeros.

# Example B - Identify the UH, Then Lag to a 2-hr UH

Two candidate 1-hr hydrographs were measured on a 2000-ac watershed (baseflow ≈ 0). The direct runoff ordinates (cfs) are:

| t (hr) | H1 (cfs) | H2 (cfs) |
|:---:|:---:|:---:|
| 0 | 0 | 0 |
| 1 | 100 | 100 |
| 2 | 300 | 250 |
| 3 | 500 | 400 |
| 4 | 450 | 350 |
| 5 | 300 | 220 |
| 6 | 200 | 130 |
| 7 | 100 | 50 |
| 8 | 50 | 0 |

a. Compute the runoff depth (in.) for each candidate. The candidate that delivers exactly 1.0 inch of direct runoff is the 1-hr UH.<br>
b. Once you know the 1-hr UH, derive the 2-hr UH by lagging.

Find: which hydrograph is the 1-hr UH, and the 2-hr UH by lagging. Check that the new UH volume is 1.0 in.

# Example C - Two-Subarea Convolution

Two adjacent subareas A and B drain to a common confluence. The 1-hr UHs and a 4-hr storm hyetograph are:

| t (hr) | 1-hr UH-A (cfs) | 1-hr UH-B (cfs) |
|:---:|:---:|:---:|
| 0 | 0 | 0 |
| 1 | 50 | 25 |
| 2 | 200 | 100 |
| 3 | 350 | 175 |
| 4 | 250 | 125 |
| 5 | 100 | 50 |
| 6 | 0 | 0 |

- Rainfall i = [0.5, 1.2, 2.5, 0.8] in/hr in 1-hr pulses
- Infiltration f = 0.3 in/hr (constant)

a. Compute the net (excess) rainfall by subtracting the constant f from each i.<br>
b. Convolve Pn with UH-A to get $Q_A$ and with UH-B to get $Q_B$.<br>
c. Add ordinate-by-ordinate to get the combined hydrograph $Q_{total} = Q_A + Q_B$ at the confluence.

This sets up everything you need for homework problems 2.18-2.20.

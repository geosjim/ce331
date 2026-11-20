# In-Class - Infiltration

We will work these examples together in class. Each one is the same type of problem as a homework problem, with different numbers.

Excel starter file: [Infiltration Example Template.xlsx](Infiltration%20Example%20Template.xlsx)

Textbook Examples 2-10 (Horton) and 2-12 (Green-Ampt) spreadsheet: [Examples10and12.xlsx](Examples10and12.xlsx)

# Example A - Horton Infiltration Capacity at Given Times

A soil has the following Horton parameters:

- Initial infiltration capacity $f_0$ = 1.2 in/hr
- Final constant capacity $f_c$ = 0.4 in/hr
- Decay coefficient $k$ = 0.5 hr$^{-1}$

Use Horton's equation

$$f(t) = f_c + (f_0 - f_c)\,e^{-kt}$$

to compute $f$ at t = 10 min, 30 min, 1 hr, 2 hr, and 4 hr. Also compute the cumulative infiltration $F$ over 4 hours.

Find: $f(t)$ at each time and the cumulative infiltration $F$ over 4 hr.

# Example B - Horton Model on a Varying-Intensity Storm

A 4-hr storm over a 10-acre basin delivers:

| Hour | Intensity $i$ (in/hr) |
|:---:|:---:|
| 1 | 1.5 |
| 2 | 1.8 |
| 3 | 0.5 |
| 4 | 0.3 |

The soil has Horton parameters $f_0$ = 1.0 in/hr, $f_c$ = 0.2 in/hr, $k$ = 1.0 hr$^{-1}$. For each hour, compute the infiltration rate at the midpoint and the resulting overland flow (in/hr). Then compute the total runoff depth.

Find: $f$ at the midpoint of each hour, the overland flow rate for each hour (in/hr), and the total runoff depth (in).

# Example C - Green-Ampt Ponding Time and Infiltration Curve

A loamy sand soil receives a steady rain at $i$ = 2.5 cm/hr. Green-Ampt parameters: $K_s$ = 1.0 cm/hr, $\psi$ = -10 cm, $\theta_s$ = 0.50, $\theta_i$ = 0.10.

Find:

1. the moisture deficit $M_d$ and the cumulative infiltration $F_s$ at which ponding begins;
2. the corresponding ponding time $t_p$; and
3. the infiltration rate $f$ at F = 1, 2, 4, and 6 cm.

# Example D - Green-Ampt Infiltration Rate and Constant-Rain Depth

A soil has Green-Ampt parameters: $K_s$ = 0.8 cm/hr, $\psi$ = -15 cm, $M = \theta_s - \theta_i$ = 0.25.

a. Compute $f$ for F = 1, 2, 3, and 5 cm using $f = K_s\,(1 - M\psi/F)$.<br>
b. If rain falls at a constant rate of 0.3 cm/hr for 2 hr (less than $K_s$), what is the cumulative infiltration?<br>
c. After many hours of saturation, what does $f$ approach?

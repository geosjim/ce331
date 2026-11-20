# In-Class - Hydrologic Routing

These examples mirror homework problems 4.8, 4.9, and 4.15. Each uses the Muskingum method:

$$D = K - Kx + 0.5\Delta t$$

$$C_0 = \frac{-Kx + 0.5\Delta t}{D} \qquad C_1 = \frac{Kx + 0.5\Delta t}{D} \qquad C_2 = \frac{K - Kx - 0.5\Delta t}{D}$$

$$Q_2 = C_0 I_2 + C_1 I_1 + C_2 Q_1$$

Excel starter file: [Hydrologic Routing Example Template.xlsx](Hydrologic%20Routing%20Example%20Template.xlsx)

# Example A - Muskingum Coefficients

Before any row-by-row routing can start, you must compute the three Muskingum weighting coefficients from the reach parameters K (travel time) and x (weighting factor) and the routing time step Δt.

**Given:**

- K = 3 hr (reach travel time)
- x = 0.25 (weighting factor)
- Δt = 1 hr (routing time step)

**Find:**

- Coefficients C₀, C₁, C₂
- Verify C₀ + C₁ + C₂ = 1.00
- Write the routing equation Q₂ = C₀I₂ + C₁I₁ + C₂Q₁
- Check the stability condition 2Kx ≤ Δt ≤ K

# Example B - Row-by-Row Routing

Using the coefficients from Example A (K = 3 hr, x = 0.25, Δt = 1 hr), route the short inflow hydrograph below through the reach. Assume the reach is initially in steady state, so Q₁ = I₁ at t = 0.

| t (hr) | 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 |
|---|---|---|---|---|---|---|---|---|
| I (m³/s) | 10 | 30 | 60 | 80 | 55 | 30 | 15 | 10 |

**Find:**

- Q(t) for t = 0 to 7 hr
- The routed peak Qp and its time tp
- The lag of Qp relative to the inflow peak

# Example C - Linear Reservoir

A reservoir whose storage is proportional to its outflow, S = K·Q, is called a linear reservoir. Many hydrologic models use it as a routing element. Claim: a linear reservoir is the special case of the Muskingum method with x = 0.

**Given:**

- S = K·Q (linear reservoir)
- K = 2 hr, Δt = 1 hr
- Initial outflow Q₀ = 0
- The same inflow hydrograph as Example B (peak 80 m³/s)

**Find:**

1. Prove the claim by substituting x = 0 into S = K[xI + (1−x)Q].
2. Compute C₀, C₁, C₂.
3. Route the inflow row by row.
4. Compare the peak attenuation to Example B.

# Textbook Example 4-3

The inflow data for textbook Example 4-3 (Muskingum routing with K = 2 days, x = 0.2, Δt = 1 day) are in this file: [Example4-3.xlsx](Example4-3.xlsx)

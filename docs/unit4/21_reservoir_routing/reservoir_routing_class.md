# In-Class - Reservoir Routing

These examples mirror homework problems 4.12, 4.13, and 4.17. Reservoir routing continues over two class periods.

Excel starter file: [Reservoir Routing Example Template.xlsx](Reservoir%20Routing%20Example%20Template.xlsx)

# Example A - Linear Reservoir

A small detention basin has a linear storage-discharge relationship S = K·Q, with K = 2.0 hr (S in m³·s·hr⁻¹ when Q is in m³/s). Starting from an empty pond (S₀ = 0, Q₀ = 0), route the inflow hydrograph below using Δt = 1 hr. Use the average-flow continuity form, substitute S = KQ, and solve for Q<sub>n+1</sub>.

| t (hr) | 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 |
|---|---|---|---|---|---|---|---|---|---|
| I (m³/s) | 0 | 20 | 60 | 100 | 80 | 50 | 20 | 5 | 0 |

**Find:**

- Outflow hydrograph Q(t)
- Peak outflow and its time of occurrence
- Peak attenuation, Q<sub>peak</sub> / I<sub>peak</sub>

# Example B - Storage-Indication for a Non-Linear Reservoir

A reservoir has a non-linear storage-discharge relation S = K·Q^1.5 with K = 2.0 (S in m³·s·hr⁻¹ when Q is in m³/s). Route the same inflow as Example A through this reservoir using storage-indication with Δt = 1 hr. Initially S₀ = 0 and Q₀ = 0.

Procedure:

1. Tabulate Q from 0 to 120 m³/s and compute S = 2·Q^1.5.
2. Compute the routing variable (2S/Δt + Q) in consistent units.
3. Plot (2S/Δt + Q) vs Q. This is the storage-indication curve.
4. Apply (I<sub>n</sub> + I<sub>n+1</sub>) + (2S<sub>n</sub>/Δt − Q<sub>n</sub>) = (2S<sub>n+1</sub>/Δt + Q<sub>n+1</sub>).
5. Read Q<sub>n+1</sub> from the curve, then carry the identity (2S/Δt − Q) = (2S/Δt + Q) − 2Q forward.

Δt unit consistency: Δt = 1 hr = 3600 s. Convert (2S/Δt) into m³/s before plotting.

**Find:**

- Storage-indication table and curve
- Outflow hydrograph Q(t)
- Compare the peak Q with Example A's linear case

# Example C - Tabular S-Q Rating

A small reservoir's S-Q rating is given as a table (typical of survey plus outlet-hydraulics data). Route a triangular inflow hydrograph using storage-indication with Δt = 1 hr = 3600 s. Initially S₀ = 0 and Q₀ = 0.

| S (10⁶ ft³) | Q (cfs) |
|---|---|
| 0 | 0 |
| 10 | 200 |
| 30 | 600 |
| 50 | 1,000 |
| 70 | 1,400 |

| t (hr) | 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 |
|---|---|---|---|---|---|---|---|---|---|
| I (cfs) | 0 | 200 | 600 | 1000 | 1400 | 1000 | 500 | 100 | 0 |

Steps:

1. Compute (2S/Δt + Q) for each row of the rating (watch units: 1 hr = 3600 s).
2. Plot or interpolate Q from (2S/Δt + Q).
3. March through Eq. 4-13 step by step.

**Find:**

- Routing curve (2S/Δt + Q) vs Q
- Outflow hydrograph Q(t)
- Maximum storage during the event
- Peak attenuation, Q<sub>peak</sub> / I<sub>peak</sub>

# Additional Routing Examples

These workbooks are used for the continued reservoir routing discussion:

- [SpecialRouting.xlsx](SpecialRouting.xlsx)
- [Inventory Routing Derivation and Example.pdf](Inventory%20Routing%20Derivation%20and%20Example.pdf)

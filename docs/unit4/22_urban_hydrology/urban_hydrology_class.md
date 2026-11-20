# In-Class - Urban Hydrology

These examples mirror homework problems 6.19 and 6.20. They use the Rational Method and the area-weighted runoff coefficient:

$$Q_p = C\,i\,A \qquad \bar{C} = \frac{\sum C_i A_i}{\sum A_i}$$

Excel starter file: [Urban Hydrology Example Template.xlsx](Urban%20Hydrology%20Example%20Template.xlsx)

# Example A - Small Mixed-Use Basin (DCIA Check)

A 4.0-ac basin in Provo, Utah is to be developed into 1.5 ac of commercial frontage (C = 0.85) and 2.5 ac of public park / open space (C = 0.20). A 10-yr storm sewer inlet is being designed. Use the rational method Qp = C·i·A (k<sub>c</sub> ≈ 1 in U.S. customary units). Because the small commercial subarea is directly connected to the inlet and has a much shorter tc than the whole basin, both Q<sub>DCIA</sub> and Q<sub>total</sub> must be checked. The larger value governs the inlet design.

**Given:**

- Total area A = 4.0 ac
- Commercial: A = 1.5 ac, C = 0.85, tc = 5 min
- Park: A = 2.5 ac, C = 0.20
- Whole basin tc = 25 min

| Duration (min) | 5 | 10 | 15 | 20 | 25 | 30 |
|---|---|---|---|---|---|---|
| 10-yr i (in/hr) | 4.50 | 3.40 | 2.80 | 2.30 | 2.00 | 1.75 |

**Find:**

- C̄ (weighted) for the whole basin
- Qp for the DCIA (commercial) only
- Qp for the total area
- Design Qp at the inlet

# Example B - Subdivision: DCIA vs. Whole Basin

A 20-ac residential subdivision near Provo has been mapped. The Directly Connected Impervious Area (DCIA), meaning rooftops, driveways, streets, and sidewalks that drain directly to the storm sewer, totals 4.5 ac. The remaining 15.5 ac of pervious lawn behaves like "lawns, sandy soil, average slope."

Use high-end runoff coefficients from Table 6-5: C<sub>DCIA</sub> = 0.90 and C<sub>lawn</sub> = 0.15. The inlet time for the full overland flow path across the lawn is 60 min; the inlet time for just the DCIA is 10 min. Determine the 25-yr design discharge at the inlet using the rational method, checking both the DCIA-only flow and the whole-basin flow.

**Given:**

- A<sub>total</sub> = 20.0 ac, A<sub>DCIA</sub> = 4.5 ac
- C<sub>DCIA</sub> = 0.90, C<sub>lawn</sub> = 0.15
- tc (DCIA) = 10 min, tc (total) = 60 min
- 25-yr IDF (Provo): 10 min → 4.50 in/hr, 60 min → 1.50 in/hr

**Find:**

- C̄ for the whole subdivision
- Q<sub>DCIA</sub> and Q<sub>total</sub> (rational method)
- Design Q for the inlet

# Example C - Culvert Sizing with Manning's Equation

Continuing from Example B, the 18-cfs DCIA peak flow will be conveyed through a corrugated steel pipe (CSP) culvert (n = 0.024). The available pipe slope is S = 1% = 0.01. Standard U.S. CSP diameters come in 6-in. increments up to 60 in, then 12-in. increments.

Using Manning's equation for full-flow capacity

$$Q_f = \frac{1.49}{n} A R^{2/3} S^{1/2}$$

and the hydraulic radius for a circular pipe flowing full, R = D/4 (with A = πD²/4), find the smallest standard diameter D that conveys at least 18 cfs. Build a small trial table of candidate diameters and read off the first row where Q<sub>f</sub> ≥ 18 cfs.

**Find:**

- Trial table of Q<sub>f</sub> vs. D
- Smallest standard D with Q<sub>f</sub> ≥ Q<sub>design</sub>
